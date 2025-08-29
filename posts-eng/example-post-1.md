---
type: Post
title: How to Add a Custom Component to Your Power Apps
description: >-
  Learn how to enhance your Power Apps by adding custom components, enabling reusable UI elements and improved app functionality.
date: '2025-01-06'
---
Power Apps custom components, aka Power Apps Component Framework (PCF) components, are specialized building blocks created to enhance the functionality of your apps beyond the standard prebuilt controls provided by Microsoft. While Power Apps includes many useful built-in controls, custom components let you integrate advanced features tailored to your specific business needs.

## Step 1: Allow custom components in Admin Center

Before adding your component, make sure custom components are enabled in your environment and you have enough permission to turn on the setting below:

1. Navigate to the Power Platform Admin Center.  
2. Go to **Environments** and select the environment you want to configure.  
3. Click **Settings**.  
4. Under **Product**, select **Features**.  
5. Find **Power Apps component framework for canvas apps** and enable it.

Or you can access using your environment ID:

https://admin.powerplatform.microsoft.com/manage/environments/{YOUR-EVIRONMENT-ID}/settings/Features

If you don’t know or can’t turn on this feature, ask your Power Platform Admin.

---

## Step 2: Import the custom component to your environment

Follow the image (omitted here) and upload the ZIP file into your environment.

---

## Step 3: Enable the component in your App

1. Open the **Insert** panel.  
2. Navigate to the **Import Component** section.  
3. Switch to the **Code component** tab.  
4. Choose the custom component that you imported in Step 2.

---

## Step 5: Insert the custom component into screen and configure

1. Once imported, your component will appear under the **Custom** category in the Insert pane.  
2. Drag and drop the component onto your desired screen within the Canvas app.  
3. Click on the component you’ve just added.  
4. In the **Properties** pane on the right, set the required properties or inputs as needed for your component.

---

## Step 7: Test the component

Always test your component to ensure it’s functioning correctly:

1. Press **Play** in the top-right corner to preview your app.  
2. Verify that the component works as expected, making adjustments if necessary.

---

That’s it! You’ve successfully added a custom component to your canvas app.