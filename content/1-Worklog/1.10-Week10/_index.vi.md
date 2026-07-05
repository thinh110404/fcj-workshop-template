---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Xây dựng giao diện Trang chủ/Danh sách sự kiện công khai.
* Xây dựng giao diện Trang chi tiết sự kiện.
* Kết nối frontend với API GET /events và GET /events/{id}.
* Tham gia event FCAJ Community Day

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------- |
| 2   | - Thiết kế wireframe/layout cho Trang danh sách sự kiện <br> - Xác định các thành phần hiển thị: tên sự kiện, trạng thái, số slot còn lại                                                                                 | 22/06/2026   | 22/06/2026      |   https://cloudjourney.awsstudygroup.com/              |
| 3   | - Dựng component EventCard, EventList <br> - Gọi API GET /events, xử lý loading state <br> - Hiển thị danh sách sự kiện, ưu tiên sự kiện Active                                                                            | 23/06/2026   | 23/06/2026      |       https://cloudjourney.awsstudygroup.com/          |
| 4   | - Xử lý trường hợp lỗi API (network error, empty data) <br> - Thêm bộ lọc/hiển thị trạng thái sự kiện (badge Draft/Active/Ended/Cancelled) <br> - **Thực hành:** Test hiển thị với nhiều dữ liệu mẫu                       | 24/06/2026   | 24/06/2026      |       https://cloudjourney.awsstudygroup.com/          |
| 5   | - Thiết kế và dựng giao diện Trang chi tiết sự kiện: tiêu đề, mô tả, thời gian, địa điểm, banner, tổng slot/slot còn lại <br> - Gọi API GET /events/{id} theo route param                                                  | 25/06/2026   | 25/06/2026      |    https://cloudjourney.awsstudygroup.com/             |
| 6   | - **Thực hành:** <br>&emsp; + Xử lý loading/error cho trang chi tiết <br>&emsp; + Responsive giao diện cho mobile/desktop <br>&emsp; + Test luồng chuyển từ danh sách sang chi tiết sự kiện                               | 26/06/2026   | 26/06/2026      |      https://cloudjourney.awsstudygroup.com/           |
| 7   | - Tham gia event FCAJ Community Day                              | 27/06/2026   | 27/06/2026      |                |

### Kết quả đạt được tuần 10:

* Hoàn thành giao diện Trang chủ/Danh sách sự kiện: hiển thị đúng các sự kiện đang mở đăng ký, trạng thái và số slot còn lại.

* Hoàn thành giao diện Trang chi tiết sự kiện: hiển thị đầy đủ tiêu đề, mô tả, thời gian, địa điểm, banner/poster, tổng slot và slot còn lại.

* Kết nối thành công frontend với API GET /events và GET /events/{id}.

* Xử lý được các trạng thái loading, lỗi API và trường hợp không có dữ liệu.

* Giao diện responsive, hiển thị tốt trên cả desktop và mobile.

* Hoàn tất phần giao diện public của module Event Management, sẵn sàng chuyển sang xây dựng giao diện Admin.
