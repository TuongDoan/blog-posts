---
type: Post
title: Display Images in Copilot Studio
description: >-
  A simple trick to display inline images in Copilot Studio, not via image URL.
date: '2025-08-01'
tag: Copilot Studio
---

I found a way to display images in **Copilot Studio**: using an inline **Base64-encoded image** with a data URI scheme.

### Steps

1. Add your base64-encoded image to a variable, e.g., `Base64`.

2. Compose an HTML `<img>` tag with that Base64 variable and save the whole tag to a new variable like this:

   ```csharp
   $"<img src='data:image/png;base64,{Topic.Base64}'/>"
   ```

3. Assign that variable to the **Send message** node.
4. 
![1751939866342](https://github.com/user-attachments/assets/e6bbe131-9d06-4bbc-a52e-4fb63d58fce5)


---

### Notes

- You **cannot** put an `<img>` tag directly into the **Send message** node; the system will sanitize it.
- With this trick, you can display any image as long as you can encode it in Base64 format.


