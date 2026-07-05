---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Xây dựng Event-CRUD-Lambda để xử lý nghiệp vụ đọc dữ liệu sự kiện.
* Triển khai API GET /events (danh sách sự kiện công khai, ưu tiên Active).
* Triển khai API GET /events/{id} (chi tiết một sự kiện).
* Kết nối API Gateway với Lambda và kiểm thử qua Postman.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu AWS Lambda: runtime, handler, event object, context object <br> - Tìm hiểu cách Lambda kết nối với DynamoDB qua SDK (boto3/AWS SDK for JS)                                                                     | 08/06/2026   | 08/06/2026      | <https://docs.aws.amazon.com/lambda/> |
| 3   | - Khởi tạo project Event-CRUD-Lambda <br> - Cấu hình IAM Role cho Lambda (quyền đọc/ghi DynamoDB) <br> - Viết hàm scan/query lấy danh sách event từ EventTable                                                            | 09/06/2026   | 09/06/2026      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/> |
| 4   | - Viết logic API GET /events: <br>&emsp; + Lọc và ưu tiên trả về event có Status = Active <br>&emsp; + Format dữ liệu trả về theo EventDto <br> - **Thực hành:** Deploy Lambda và test bằng AWS Console (Test Event)      | 10/06/2026   | 10/06/2026      | <https://docs.aws.amazon.com/apigateway/> |
| 5   | - Viết logic API GET /events/{id}: <br>&emsp; + Lấy EventId từ path parameter <br>&emsp; + Query DynamoDB theo Partition Key <br>&emsp; + Xử lý trường hợp không tìm thấy event (404)                                    | 11/06/2026   | 11/06/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo API Gateway, cấu hình route GET /events và GET /events/{id} <br>&emsp; + Kết nối route với Lambda (Lambda Proxy Integration) <br>&emsp; + Test API qua Postman <br> - Ghi log lỗi và xử lý exception cơ bản | 12/06/2026   | 12/06/2026      | <https://docs.aws.amazon.com/apigateway/latest/developerguide/> |

### Kết quả đạt được tuần 8:

* Hoàn thành Event-CRUD-Lambda với khả năng kết nối và truy vấn dữ liệu từ EventTable.

* Triển khai thành công API GET /events:
  * Trả về danh sách sự kiện.
  * Ưu tiên hiển thị các sự kiện có Status = Active.
  * Dữ liệu trả về đúng định dạng EventDto đã thống nhất với nhóm.

* Triển khai thành công API GET /events/{id}:
  * Trả về đầy đủ thông tin chi tiết một sự kiện theo EventId.
  * Xử lý được trường hợp EventId không tồn tại (trả về lỗi 404 phù hợp).

* Cấu hình thành công API Gateway kết nối với Lambda theo mô hình Lambda Proxy Integration.

* Kiểm thử API GET /events và GET /events/{id} thành công qua Postman, dữ liệu trả về đúng như mong đợi.

* Nắm được cách xử lý lỗi cơ bản (try/catch, response status code) trong Lambda.

* Sẵn sàng cho việc triển khai các API ghi dữ liệu (POST/PUT/DELETE) ở tuần tiếp theo.
