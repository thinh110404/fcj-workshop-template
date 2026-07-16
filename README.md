# README - Tổng kết 12 tuần đã làm

## Mục tiêu

Tài liệu này tóm tắt những gì mình đã học và thực hiện trong 12 tuần trong chương trình AWS/FCAJ, tập trung vào nền tảng Cloud và xây dựng module Event Management.

---

## Tuần 1: Làm quen với AWS

- Làm quen với thành viên FCAJ và quy định làm việc.
- Hiểu khái niệm về AWS và điện toán đám mây.
- Tạo tài khoản AWS Free Tier.
- Làm quen với AWS Console và cài đặt AWS CLI.

## Tuần 2: Quản trị tài khoản và bảo mật cơ bản

- Học về IAM, root account, IAM user, IAM group và policy.
- Tạo admin user và admin group.
- Tìm hiểu AWS Support và AWS Budgets.
- Làm quen với khái niệm VPC và VPN.

## Tuần 3: Nền tảng mạng và phương pháp học Cloud

- Ôn lại các khái niệm IAM, Budgets, Support và VPC.
- Học sâu hơn về networking trên AWS.
- Rèn kỹ năng đọc tài liệu AWS và làm lab theo đúng quy trình.

## Tuần 4: Compute, Storage và Migration

- Học về EC2, AMI, instance type, key pair, security group và EBS.
- Tìm hiểu Amazon EFS, FSx và AWS MGN.
- Nắm được khái niệm Auto Scaling và khả năng tăng giảm tài nguyên tự động.

## Tuần 5: Thực hành EC2 và VPN

- Thực hành tạo và kết nối EC2.
- Tìm hiểu cách cấu hình Security Group và SSH.
- Học cách troubleshoot các lỗi thường gặp khi kết nối EC2.
- Làm quen với kết nối VPN.

## Tuần 6: Bảo mật trên AWS

- Học Shared Responsibility Model.
- Hiểu về AWS Organizations, Identity Center, KMS và encryption.
- Thực hành cấu hình IAM Policy và MFA.
- Tham gia sự kiện và củng cố kiến thức bảo mật.

---

## Tuần 7: Xây dựng dữ liệu cho module Event Management

- Thiết kế schema cho EventTable trên DynamoDB.
- Tạo bucket S3 để lưu ảnh banner/poster cho sự kiện.
- Chuẩn bị nền tảng ban đầu cho Event CRUD Lambda.

## Tuần 8: Xây dựng API Backend cho sự kiện

- Implement API GET /events để lấy danh sách sự kiện.
- Implement API GET /events/{id} để lấy chi tiết sự kiện.
- Kết nối Lambda với API Gateway và test bằng Postman.

## Tuần 9: Hoàn thiện API viết dữ liệu và phân quyền

- Implement API POST /events, PUT /events/{id}, DELETE /events/{id}.
- Xử lý upload banner/poster lên S3 và lưu URL vào DynamoDB.
- Áp dụng xác thực JWT/Cognito để kiểm soát quyền Admin.

## Tuần 10: Xây dựng giao diện người dùng công khai

- Thiết kế và xây dựng trang danh sách sự kiện.
- Xây dựng trang chi tiết sự kiện.
- Kết nối frontend với API GET /events và GET /events/{id}.
- Xử lý trạng thái loading, lỗi và dữ liệu rỗng.

## Tuần 11: Xây dựng giao diện Admin

- Xây dựng form tạo sự kiện mới.
- Xây dựng form chỉnh sửa và hủy sự kiện.
- Thực hiện validate form, upload banner và hiển thị thông báo.
- Kết nối frontend với POST/PUT/DELETE API.

## Tuần 12: Tích hợp và kiểm thử toàn bộ hệ thống

- Kiểm tra toàn bộ luồng từ danh sách sự kiện → chi tiết → admin tạo/sửa/hủy.
- Đồng bộ dữ liệu giữa frontend, Lambda, DynamoDB và S3.
- Họp với team để thống nhất EventDto, EventId và trạng thái sự kiện.
- Chụp ảnh và quay video demo cho báo cáo workshop.

---

## Kết quả cuối cùng

Sau 12 tuần, mình đã:

- Nắm được kiến thức nền tảng về AWS Cloud.
- Thực hành các dịch vụ AWS quan trọng như IAM, EC2, S3, Lambda, API Gateway, DynamoDB, Cognito.
- Xây dựng được module Event Management hoàn chỉnh gồm:
  - Public view: xem danh sách và chi tiết sự kiện.
  - Admin view: tạo, sửa, hủy sự kiện.
  - Backend API và lưu trữ dữ liệu trên AWS.
  - Upload ảnh banner/poster và phân quyền Admin.

---

## Công nghệ sử dụng

- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- Amazon S3
- Amazon Cognito
- Amazon CloudFront
- React / Frontend UI

---

## Kết luận

12 tuần vừa qua là một hành trình học tập và thực hành thực tế về Cloud Computing và xây dựng ứng dụng trên AWS. Đây là nền tảng quan trọng để mình tiếp tục phát triển kỹ năng Cloud và full-stack trong tương lai.
