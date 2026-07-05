---
title: "Worklog Tuần 11"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Xây dựng giao diện Admin - Tạo sự kiện.
* Xây dựng giao diện Admin - Sửa/Hủy sự kiện.
* Xử lý validate form, upload banner, loading/error state và thông báo kết quả.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------- |
| 2   | - Thiết kế wireframe cho form Admin tạo sự kiện <br> - Xác định các field: Title, Description, Location, StartTime, EndTime, TotalSlots, Status, banner upload                                                             | 29/06/2026   | 29/06/2026      | https://cloudjourney.awsstudygroup.com/                |
| 3   | - Dựng form tạo sự kiện <br> - Viết logic validate form (bắt buộc nhập, StartTime < EndTime, TotalSlots > 0) <br> - Xử lý chọn/preview ảnh banner trước khi upload                                                        | 30/06/2026   | 30/06/2026      |     https://cloudjourney.awsstudygroup.com/            |
| 4   | - Kết nối form với API POST /events <br> - Xử lý upload banner kèm request tạo event <br> - **Thực hành:** Test tạo sự kiện thành công/thất bại, hiển thị thông báo                                                       | 01/07/2026   | 01/07/2026      |https://cloudjourney.awsstudygroup.com/|
| 5   | - Dựng giao diện Admin - Sửa sự kiện: load dữ liệu cũ vào form, cho phép cập nhật thông tin và đổi banner <br> - Viết logic đổi trạng thái Draft/Active/Ended/Cancelled                                                    | 02/07/2026   | 02/07/2026      |        https://cloudjourney.awsstudygroup.com/         |
| 6   | - Kết nối với API PUT /events/{id} và DELETE /events/{id} <br> - **Thực hành:** <br>&emsp; + Test cập nhật, đổi trạng thái, hủy sự kiện <br>&emsp; + Xử lý loading/error/thông báo thành công cho toàn bộ form Admin        | 03/07/2026   | 03/07/2026      |     https://cloudjourney.awsstudygroup.com/            |

### Kết quả đạt được tuần 11:

* Hoàn thành giao diện Admin - Tạo sự kiện: nhập đầy đủ thông tin, upload banner/poster, validate form đầy đủ trước khi gửi.

* Hoàn thành giao diện Admin - Sửa/Hủy sự kiện: cập nhật thông tin, đổi trạng thái Draft/Active/Ended/Cancelled.

* Kết nối thành công với API POST /events, PUT /events/{id}, DELETE /events/{id}.

* Xử lý đầy đủ trạng thái loading, lỗi API, validate form và thông báo tạo/sửa/hủy thành công.

* Admin có thể quản lý toàn bộ vòng đời sự kiện từ giao diện, dữ liệu đồng bộ đúng với EventTable và S3.

* Hoàn tất phần giao diện Admin của module Event Management.
