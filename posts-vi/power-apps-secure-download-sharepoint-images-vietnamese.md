---
type: Post
title: Tải Xuống Hình Ảnh Từ Cột Hình Ảnh SharePoint Một Cách An Toàn Trong Power Apps
description: >-
  Hướng dẫn chi tiết cách sử dụng Power Automate và Power Apps để tạo URL mã hóa, đảm bảo việc tải xuống hình ảnh từ SharePoint luôn an toàn và kế thừa quyền truy cập từ người dùng.
date: '2024-05-26'
tag: Power Apps
---
Có nhiều cách để tải xuống hình ảnh được lưu trữ trong cột hình ảnh của SharePoint, nhưng ở đây mình sẽ chỉ cho bạn cách tải chúng **một cách an toàn** từ Power Apps.

---

## Cách Tiếp Cận

- Lấy URL của hình ảnh thực tế (không phải dữ liệu binary).  
- Khi nhấp vào một hình ảnh trong SharePoint List, hệ thống sẽ mở ra URL có dạng:  

```
https://MY_TENANT.sharepoint.com/sites/DEMO_PWAPP/_api/v2.1/sites(…)/lists(…)/attachments(‘Reserved_ImageAttachment_%5B11%5D_%5BSampleImage%5D…png‘)/thumbnails/0/c3000x2000/content?prefer=noredirect%2Cclosestavailablesize
```

📌 **Giải thích**:  
- `MY_TENANT`: Tên tenant (bạn sẽ có tên khác).  
- `DEMO_PWAPP`: Tên site SharePoint (bạn sẽ có tên khác).  
- `Site ID`: khác nhau cho mỗi site.  
- `List ID`: khác nhau cho mỗi list.  
- `Sample_Image`: cột hình ảnh (Image type).  

Phần cố định của URL là **đen**, phần thay đổi và được mã hóa hệ thống là **đỏ** (file name).  

Trong flow, mình sẽ gọi SharePoint API, phân tích JSON 2 lần để lấy file name, sau đó mã hóa lại, rồi gửi về Power Apps để tải xuống.

---

## Các Bước Thực Hiện

<img width="862" height="1004" alt="image" src="https://github.com/user-attachments/assets/4b56735f-e156-49a4-976a-7f786b9c6421" />


### 1. Trigger: Power Apps (V2)

<img width="1190" height="200" alt="image" src="https://github.com/user-attachments/assets/744294e4-a325-447d-bb87-28506d6c0661" />

- Tạo một tham số dạng **Number** để lưu ID của item cần tải xuống.  

### 2. Send an HTTP request to SharePoint

<img width="1190" height="480" alt="image" src="https://github.com/user-attachments/assets/29d98bef-1d7b-4964-8d7d-6768b31c2262" />

- Gọi API của SharePoint để lấy metadata của hình ảnh.  

### 3. Parse JSON

<img width="1232" height="696" alt="image" src="https://github.com/user-attachments/assets/02caf2df-10f8-452e-bcfe-83dca84fed6c" />

Sử dụng **Parse JSON** để phân tích dữ liệu trả về.  

Ví dụ JSON Schema:

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

<img width="1218" height="688" alt="image" src="https://github.com/user-attachments/assets/e28f64fb-4c9b-4d2e-94e2-0877f110ccf5" />

Từ kết quả `Parse JSON`, tiếp tục phân tích object **SampleImage** để lấy URL gốc:

```json
{
  "type": "object",
  "properties": {
    "fileName": { "type": "string" }
  }
}
```

### 5. Compose Encoded URL

<img width="1192" height="396" alt="image" src="https://github.com/user-attachments/assets/3626a590-ff09-43e8-8b76-2b890a293e58" />

Tạo expression để mã hóa tên file:  

```csharp
encodeUriComponent(body('Parse_JSON_1')?['fileName'])
```

💡 **Tip**: Có thể thay đổi tham số `c3000x2000` để điều chỉnh kích thước ảnh trả về.  

---

## Gửi URL Về Power Apps

<img width="1780" height="332" alt="image" src="https://github.com/user-attachments/assets/6b5c5468-e737-4434-803d-42a58c442dea" />

Trong flow, trả về URL bằng tham số **outputURL**.  
Sau đó trong Power Apps, sử dụng đoạn code sau ở **OnSelect**:  

```csharp
Download(Flow_Name.Run(ThisItem.ID).outputURL)
```

---

## Bảo Mật

- Không cần lo lắng về quyền hạn vì URL kế thừa quyền từ SharePoint row-level security.  
- URL được Power Automate gửi về **bắt buộc phải xác thực**. Nếu bị rò rỉ, người khác cũng không thể mở được hình ảnh.  


