---
type: Post
title: Giữ Kích Thước Phông Chữ Nhất Quán Giữa Modern và Classic Control Trong Power Apps
description: >-
  Hướng dẫn cách đồng bộ kích thước phông chữ giữa modern control và classic control cũ trong Power Apps
date: '2024-05-22'
---
Khi tạo ứng dụng canvas sử dụng kết hợp các **modern control** và **classic control**, bạn có thể nhận thấy rằng văn bản trong các modern control có vẻ nhỏ hơn so với các control cũ.  
Để duy trì tính nhất quán về mặt hình thức, chúng ta cần giữ kích thước phông chữ nhất quán trên tất cả các control của ứng dụng.

---

## Sự Khác Biệt

Sự khác biệt xuất phát từ **đơn vị kích thước phông chữ**:  
- Modern control sử dụng **pixel (px)**  
- Classic control sử dụng **point (pt)**  

---

## Chuyển Đổi Giữa Pixel và Point

- Từ **pixel (modern control)** → **point (classic control)**: Chia giá trị kích thước phông chữ cho `0.75`  
- Từ **point (classic control)** → **pixel (modern control)**: Nhân giá trị kích thước phông chữ với `0.75`  

<img width="1024" height="332" alt="Font-Size-Consistency-1024x332 (1)" src="https://github.com/user-attachments/assets/a8b5c888-dbbf-481b-85ff-82e5d4a858e9" />

---

## Sử Dụng Biến Để Duy Trì Tính Nhất Quán

Để duy trì kích thước phông chữ nhất quán trên toàn bộ ứng dụng, bạn có thể khai báo biến trong thuộc tính **Formulas** của ứng dụng:

```csharp
varFontSizeClassic = 13; 
varFontSizeModern = varFontSizeClassic * 0.75;
```

### Cách Dùng

- Khi thêm một **modern control** mới, đặt kích thước phông chữ thành `varFontSizeModern` để văn bản khớp với kích thước mặc định (13 pt) của classic control.  
- Khi thay đổi kích thước phông chữ của **classic control**, hãy đặt nó thành `varFontSizeClassic` và cập nhật giá trị biến trong thuộc tính Formulas.  

---

**Happy Coding!**  

