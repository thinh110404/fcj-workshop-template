---
title: "Worklog Tuần 12"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Tích hợp và kiểm thử toàn bộ module Event Management (frontend + backend).
* Thống nhất EventDto và Status với Tâm cho module Registration và Auth.
* Ghi nhận kết quả, chụp ảnh/quay video demo cho workshop report.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------- |
| 2   | - Rà soát toàn bộ luồng Event List → Event Detail → Admin Create/Update/Delete <br> - Kiểm tra tính nhất quán dữ liệu giữa Frontend, Lambda và EventTable                                                                  | 06/07/2026   | 06/07/2026      |  https://cloudjourney.awsstudygroup.com/               |
| 3   | - Họp thống nhất với Tâm về EventId, EventDto và Status (Draft/Active/Ended/Cancelled) để module Registration đọc đúng AvailableSlots <br> - Thống nhất cơ chế phân quyền Admin với module Auth                           | 07/07/2026   | 07/07/2026      |   https://cloudjourney.awsstudygroup.com/              |
| 4   | - Sửa lỗi phát sinh sau khi thống nhất (nếu có thay đổi field/format) <br> - **Thực hành:** Test lại toàn bộ API và giao diện sau khi chỉnh sửa                                                                            | 08/07/2026   | 08/07/2026      |   https://cloudjourney.awsstudygroup.com/              |
| 5   | - Kiểm thử end-to-end: tạo sự kiện → hiển thị public → sửa/hủy → kiểm tra cập nhật real-time trên frontend <br> - Kiểm tra upload/hiển thị banner trên cả trang public và admin                                            | 09/07/2026   | 09/07/2026      |    https://cloudjourney.awsstudygroup.com/             |
| 6   | - Chụp ảnh màn hình các chức năng chính <br> - Quay video demo ngắn: Event List, Event Detail, Admin tạo/sửa/hủy sự kiện <br> - Tổng hợp báo cáo kết quả module Event Management cho workshop report                       | 10/07/2026   | 10/07/2026      |     https://cloudjourney.awsstudygroup.com/            |

### Kết quả đạt được tuần 12:

* Hoàn thành tích hợp toàn bộ module Event Management: Frontend (public + admin) hoạt động ổn định với Backend Lambda và EventTable.

* Thống nhất thành công EventId, EventDto và Status với Tâm, đảm bảo module Registration đọc đúng AvailableSlots và chỉ cho đăng ký với event Active.

* Thống nhất cơ chế phân quyền Admin với module Auth, đảm bảo bảo mật cho các API tạo/sửa/xóa.

* Event List và Event Detail chạy ổn định trên frontend với dữ liệu thực từ EventTable.

* Admin có thể tạo/sửa/hủy sự kiện thành công, dữ liệu đồng bộ chính xác vào EventTable và banner/poster lưu đúng trên S3.

* Hoàn thành ảnh chụp màn hình và video demo ngắn cho các chức năng chính của module.

* Bàn giao đầy đủ kết quả module Event Management cho workshop report.
