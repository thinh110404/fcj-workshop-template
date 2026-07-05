---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Thiết kế cấu trúc dữ liệu cho module Event Management (EventTable trên DynamoDB).
* Khởi tạo hạ tầng lưu trữ ảnh banner/poster sự kiện (S3 Bucket).
* Chuẩn bị khung project cho Event-CRUD-Lambda.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                       | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Phân tích yêu cầu module Event Management <br> - Xác định các thuộc tính cần thiết cho EventTable: EventId, Title, Description, Location, StartTime, EndTime, TotalSlots, AvailableSlots, BannerUrl, Status, CreatedAt, UpdatedAt | 01/06/2026   | 01/06/2026      | https://cloudjourney.awsstudygroup.com/                |
| 3   | - Tìm hiểu DynamoDB: Partition Key, Sort Key, Data Types <br> - Thiết kế schema EventTable trên DynamoDB <br> - Xác định các trạng thái Status: Draft/Active/Ended/Cancelled                                                | 02/06/2026   | 02/06/2026      | <https://docs.aws.amazon.com/dynamodb/> |
| 4   | - **Thực hành:** Tạo bảng EventTable trên AWS Console <br>&emsp; + Cấu hình Partition Key = EventId <br>&emsp; + Cấu hình capacity mode (On-demand) <br> - Nhập thử dữ liệu mẫu để kiểm tra schema                          | 03/06/2026   | 03/06/2026      | <https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/> |
| 5   | - Tìm hiểu Amazon S3: Bucket, Object, Permission, Presigned URL <br> - Thiết kế cấu trúc lưu trữ banner/poster (naming convention, folder theo EventId)                                                                     | 04/06/2026   | 04/06/2026      | <https://docs.aws.amazon.com/s3/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo S3 Bucket "event-assets" <br>&emsp; + Cấu hình quyền truy cập (Bucket Policy, CORS) <br>&emsp; + Upload thử ảnh test và lấy public URL <br> - Ghi chú lại cấu trúc dữ liệu để thống nhất với nhóm (EventDto) | 05/06/2026   | 05/06/2026      | <https://docs.aws.amazon.com/s3/> |

### Kết quả đạt được tuần 7:

* Hoàn thành thiết kế schema EventTable trên DynamoDB với đầy đủ các thuộc tính:
  * EventId (Partition Key)
  * Title, Description, Location
  * StartTime, EndTime
  * TotalSlots, AvailableSlots
  * BannerUrl
  * Status (Draft/Active/Ended/Cancelled)
  * CreatedAt, UpdatedAt

* Đã tạo thành công EventTable trên AWS DynamoDB và kiểm tra được việc đọc/ghi dữ liệu mẫu.

* Đã tạo S3 Bucket riêng để lưu trữ banner/poster sự kiện, cấu hình quyền truy cập và CORS phù hợp cho việc upload từ frontend.

* Xác định được quy tắc: khi tạo event, AvailableSlots khởi tạo bằng TotalSlots.

* Chuẩn bị được cấu trúc EventDto (dữ liệu trả về cho frontend/module khác) để thống nhất với Tâm cho module Registration và Auth.

* Dựng khung project ban đầu cho Event-CRUD-Lambda, sẵn sàng cho việc viết logic API ở tuần tiếp theo.
