---
type: Post
title: Cách thêm code component (PCF) vào Power Apps để mở rộng tính năng
description: >-
  Hướng dẫn chi tiết cách kích hoạt, import và sử dụng code component (PCF) trong Power Apps nhằm mở rộng tính năng cho ứng dụng canvas.
date: '2025-07-06'
---
Power Apps custom components, hay Power Apps Component Framework (PCF), là các thành phần được phát triển từ code truyền thống, chuyên biệt dùng để nâng cao chức năng cho ứng dụng của bạn. Mặc định Power Apps đã cung cấp nhiều control hữu ích, tuy nhiên đôi khi có các yêu cầu nghiệp vụ nâng cao sẽ vượt ra ngoài khả năng của các thành phần đó, vì thế PCF ra đời để bổ sung, tuỳ chỉnh Power Apps với TypeScript.

Gọi đúng là custom code component, nhưng cứ gọi chung là PCF cho ngắn hen. Giờ mình sẽ chỉ các bạn cách dùng PCF, từng bước:



---

## Bước 1: Cho phép dùng PCF trong Admin Center

1. Truy cập Power Platform Admin Center.  
2. Vào **Environments**, chọn môi trường mong muốn.  
3. Nhấn **Settings**.  
4. Trong mục **Product**, chọn **Features**.  
5. Tìm mục **Power Apps component framework for canvas apps** và bật nó lên.

Bạn cũng có thể truy cập trực tiếp bằng đường link này với ID môi trường của bạn:  
`https://admin.powerplatform.microsoft.com/manage/environments/{YOUR-ENVIRONMENT-ID}/settings/Features`

<img width="1600" height="450" alt="image" src="https://github.com/user-attachments/assets/434db719-50eb-4307-a1e8-f681619d323c" />

Nếu bạn không làm được, có thể bạn đang không được cấp quyền để thao tác. Hãy liên hệ phòng IT hoặc Admin/người chịu trách nhiệm Power Platform trong công ty của bạn để được giúp đỡ.

---

## Bước 2: Import PCF vào môi trường

Tải file ZIP chứa PCF rồi upload vào môi trường của bạn.

<img width="1600" height="662" alt="image" src="https://github.com/user-attachments/assets/6eb29876-b328-4fc9-bc49-db496d3fb9b3" />


---

## Bước 3: Bật PCF trong App

1. Mở **Insert panel** trong Power Apps Studio.  
2. Chọn phần **Import component**.  
3. Chuyển sang tab **Code component**.  
4. Chọn PCF bạn đã nhập ở bước 2.

<img width="1600" height="726" alt="image" src="https://github.com/user-attachments/assets/1d96c67f-08a9-4515-9cc7-411cf94848dc" />

---

## Bước 4: Chèn PCF vào màn hình và cấu hình nó

1. Sau khi nhập, PCF sẽ hiển thị trong mục **Code Component** của Insert pane.  
2. Kéo thả PCF vào màn hình canvas app.  
3. Chọn PCF bạn vừa thêm vào.  
4. Trong thanh **Properties**, cấu hình các thuộc tính hoặc input cần thiết cho PCF này.

<img width="1600" height="785" alt="image" src="https://github.com/user-attachments/assets/ccf12a73-42f6-4883-9dd4-c4e81f9b0b32" />

---

## Bước 5: Kiểm tra PCF xem đã chạy ngọt chưa

1. Nhấn nút **Play** góc trên bên phải để xem trước app.  
2. Kiểm tra hoạt động của component, đảm bảo nó chạy đúng chức năng và thực hiện các điều chỉnh nếu cần.

---

Vậy là bạn đã thêm thành công một custom component vào ứng dụng canvas Power Apps rồi đó :V
