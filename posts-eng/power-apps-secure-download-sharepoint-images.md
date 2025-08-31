---
type: Post
title: Securely Download Images from SharePoint’s Image Column in Power Apps
description: >-
  A step-by-step guide on securely downloading images from SharePoint’s image column using Power Apps and Power Automate by reconstructing encoded URLs instead of relying on binary data.
date: '2024-05-26'
tag: Power Apps
---
There are several ways to download images stored in SharePoint’s image column, but this tutorial will show you how to download them securely from Power Apps.

My approach is to obtain the URL of the actual image, not the binary. When you go to the list and click on the image, you will get the encoded URL to the file, so I try to recreate that link in Power Automate.

---

## Why It’s Secure

We don’t need to worry about the security/permission aspect because it will be inherited from the row permission in SharePoint.  
The URL that Power Automate sends to Power Apps requires authentication. If the direct URL were somehow leaked, they still couldn’t open the image and would receive the error below:

```json
{
   "error": {
      "code": "unauthenticated",
      "message": "Unauthenticated"
   }
}
```

---

## Overview of the Flow

1. **Trigger**: Power Apps (V2)  
2. **Send an HTTP request to SharePoint**  
3. **Parse JSON**  
4. **Parse JSON 1**  
5. **Compose the encoded URL**  
6. **Respond to a PowerApp or flow**  
7. **Pass the URL to Power Apps**  

---

## Example of SharePoint Image URL

When you click on an image in the SharePoint list, it will open the image with a URL that looks like this:

```
https://MY_TENANT.sharepoint.com/sites/DEMO_PWAPP/_api/v2.1/sites(‘057f5fce-7a24-4f2d-bd1b-485b97fab9c2,d4645b07-89ba-4dbf-9e66-675dede90c17’)/lists(‘010df7ca-c15c-482c-a96d-cf32dd507d5b’)/attachments(‘Reserved_ImageAttachment_%5B11%5D_%5BSampleImage%5D%5B2%5D_%5Bbg%5D%5B1%5D_%5B8%5D.png‘)/thumbnails/0/c3000x2000/content?prefer=noredirect%2Cclosestavailablesize
```

- Tenant name: `MY_TENANT` (yours will be different)  
- SharePoint Site name: `DEMO_PWAPP` (yours will be different)  
- Site ID: `057f5fce-7a24-4f2d-bd1b-485b97fab9c2,...` (yours will be different)  
- List ID: `010df7ca-c15c-482c-a96d-cf32dd507d5b` (yours will be different)  
- Image type column: `Sample_Image`  

The **blue part** of the URL is consistent, but the **red part** (file name) changes and is encoded by the system. In the flow, we call the SharePoint API, parse JSON twice, and encode the file name. Then we construct the URL and send it back to Power Apps for download.

---
<img width="862" height="1004" alt="image" src="https://github.com/user-attachments/assets/8e6f82d0-1cad-4ce3-b965-fafbedb919bf" />

## Building the Flow

### 1. Trigger: Power Apps (V2)

<img width="1190" height="200" alt="image" src="https://github.com/user-attachments/assets/caea6604-15f3-4816-bcd6-116613e36bc8" />
At the trigger, create a **Number** type parameter to store the ID of the item that you want to download.

### 2. Send an HTTP request to SharePoint

<img width="1190" height="480" alt="image" src="https://github.com/user-attachments/assets/05930ace-e6b5-45a3-a58c-4a4e923bc2aa" />
Retrieve the details of the image field.

### 3. Parse JSON

<img width="1232" height="696" alt="image" src="https://github.com/user-attachments/assets/3a80b06a-7904-4c14-8984-966376cd771d" />
The Parse JSON action will give us the JSON object that contains the URL.

#### JSON Schema

```json
{
  "type": "object",
  "properties": {
    "id": { "type": "string" },
    "fields": {
      "type": "object",
      "properties": {
        "ID": { "type": "string" },
        "Title": { "type": "string" },
        "SampleImage": { "type": "string" }
      }
    }
  }
}
```

### 4. Parse JSON 1

<img width="1218" height="688" alt="image" src="https://github.com/user-attachments/assets/3f154cb0-dde6-4e2d-a801-558dd276d3a1" />
Parse the result object again to obtain the actual file name.

```json
{
  "type": "object",
  "properties": {
    "fileName": { "type": "string" }
  }
}
```

### 5. Compose the Encoded URL

<img width="1192" height="396" alt="image" src="https://github.com/user-attachments/assets/2e048d3a-66e3-4538-bb49-86dd2a6495a8" />
Use an expression to encode the file name:

```csharp
encodeUriComponent(
    body('Parse_JSON_1')?['fileName']
)
```

💡 **Tip**: You can control the dimensions of the output file by changing the `c3000x2000` parameter in the URL.

### 6. Respond to a PowerApp or Flow

<img width="1780" height="332" alt="image" src="https://github.com/user-attachments/assets/f07513d7-a46f-4d38-9e8f-9fba47267361" />
Create a **Text** parameter named `outputURL` to send the URL back to Power Apps.

### 7. Pass the URL to Power Apps

In Power Apps, trigger the flow and use the returned URL for downloading:

```csharp
Download(
    Flow_Name.Run(
        ThisItem.ID
    ).outputURL
)
```

---

## Best Practices

- Return the URL dynamically each time the user requests it.  
- Or save the generated URL in another column for faster retrieval later.  
- You can update the URL automatically whenever the item is modified.  

This approach minimizes system effort and improves performance.

