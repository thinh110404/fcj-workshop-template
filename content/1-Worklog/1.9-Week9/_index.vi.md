---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Triển khai các API ghi dữ liệu: POST /events, PUT /events/{id}, DELETE /events/{id}.
* Xây dựng logic upload banner/poster sự kiện lên S3 và lưu BannerUrl vào EventTable.
* Kiểm tra và áp dụng phân quyền Admin cho các API tạo/sửa/xóa sự kiện.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------- |
| 2   | - Viết logic API POST /events: <br>&emsp; + Validate dữ liệu đầu vào (Title, StartTime, EndTime, TotalSlots...) <br>&emsp; + Khởi tạo AvailableSlots = TotalSlots <br>&emsp; + Gán CreatedAt/UpdatedAt tự động            | 15/06/2026   | 15/06/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 3   | - Viết logic API PUT /events/{id}: <br>&emsp; + Cập nhật thông tin sự kiện <br>&emsp; + Cho phép đổi Status: Draft/Active/Ended/Cancelled <br>&emsp; + Cập nhật UpdatedAt                                                 | 16/06/2026   | 16/06/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 4   | - Viết logic API DELETE /events/{id}: <br>&emsp; + Xóa cứng hoặc chuyển Status sang Cancelled (soft delete) <br> - **Thực hành:** Test 3 API bằng Postman với các trường hợp hợp lệ/không hợp lệ                          | 17/06/2026   | 17/06/2026      | <https://docs.aws.amazon.com/apigateway/> |
| 5   | - Tìm hiểu upload file lên S3 từ Lambda (base64 hoặc Presigned URL) <br> - Viết logic xử lý banner/poster: upload ảnh lên S3 Bucket, lấy URL và lưu vào trường BannerUrl trong EventTable                                 | 18/06/2026   | 18/06/2026      | <https://docs.aws.amazon.com/s3/> |
| 6   | - Tìm hiểu Cognito/JWT: cách xác thực token, decode claims <br> - **Thực hành:** <br>&emsp; + Viết middleware kiểm tra JWT và role Admin <br>&emsp; + Áp dụng middleware cho POST/PUT/DELETE <br>&emsp; + Test trường hợp không có quyền (401/403) | 19/06/2026   | 19/06/2026      | <https://docs.aws.amazon.com/cognito/latest/developerguide/> |

### Kết quả đạt được tuần 9:

* Triển khai thành công API POST /events: tạo sự kiện mới, tự động khởi tạo AvailableSlots bằng TotalSlots, dữ liệu lưu đúng vào EventTable.

* Triển khai thành công API PUT /events/{id}: cập nhật thông tin sự kiện, cho phép thay đổi Status theo đúng vòng đời Draft → Active → Ended/Cancelled.

* Triển khai thành công API DELETE /events/{id}: xử lý xóa hoặc chuyển trạng thái sự kiện sang Cancelled.

* Hoàn thành logic upload banner/poster lên S3 Event Assets Bucket và lưu chính xác BannerUrl vào EventTable.

* Áp dụng thành công cơ chế kiểm tra quyền Admin (JWT/Cognito) cho các API tạo/sửa/xóa, chặn được các request không hợp lệ.

* Kiểm thử toàn bộ 5 API (GET, GET/{id}, POST, PUT, DELETE) qua Postman, đảm bảo hoạt động đúng nghiệp vụ.

* Hoàn tất phần Backend/Lambda của module Event Management, sẵn sàng cho việc xây dựng giao diện Frontend.
