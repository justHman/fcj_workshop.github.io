### Mục tiêu tuần 12:

* Nâng tầm ứng dụng nhắm tới hệ sinh thái bảo mật nghiêm ngặt của Amazon AWS (Triển khai Serverless với ECS Fargate).
* Tăng cường độ mượt và khả năng chịu tải thông qua các tiến trình Async ngầm, đồng thời bảo mật tuyệt đối các Route trước khi kết thúc thực tập.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Setup kho bãi ECR (Elastic Container Registry) để cất giữ Image bảo mật tại AWS cloud | 23/03/2026   | 23/03/2026      | AWS ECR Guide |
| 3   | - Chạy thử nghiệm triển khai lên cụm máy ảo AWS ECS Fargate <br> - Fixed bug đọc IP sức khỏe (Healthcheck) khi giao tiếp container bị nhốt trong các dải Private Subnet | 24/03/2026   | 24/03/2026      | AWS ECS Developer Guide |
| 4   | - Kết nối lưu trữ Cache qua AWS S3 thay thế cho Volume cũ <br> - Tinh chỉnh tính phí rẻ theo Capacity Provider `FARGATE_SPOT` để ứng biến cắt giảm hóa đơn AWS | 25/03/2026   | 25/03/2026      |
| 5   | - Khởi tạo luồng xử lý bất đồng bộ (Async queue/Threadpool) giúp load API mượt mà không làm treo các tính năng khác khi chạy ngầm | 26/03/2026   | 26/03/2026      | 
| 6   | - Thiết lập cơ chế bảo vệ cổng Web API với JSON Web Token (JWT) qua thư viện `jose` <br> - Cấu trúc lại Docker build thêm bản gỡ lỗi (debug images) và chốt tài liệu hoàn thiện khóa thực tập | 27/03/2026   | 27/03/2026      | 

### Kết quả đạt được tuần 12:

* Dựng vươn tầm kiến trúc hệ thống bằng việc trỏ deploy tới lõi Serverless khổng lồ của AWS đó là ECS Fargate mang độ uy tín bảo mật chuẩn doanh nghiệp.
* Ép được giá thành vận hành hệ thống xuống mức rất thấp nhờ khéo léo cài cắm cơ chế Fargate Spot chạy xen kẽ, tối ưu chi tiêu hạ tầng đám mây.
* Đánh gục những bug cốt tử nhất bao gồm việc nhận diện sai địa chỉ IP do mạng riêng ảo (VPC) của AWS ép hay những pha đụng độ quyền hệ thống (IAM permission) ngăn chặn đọc ghi file đệm S3.
* Vượt qua bài kiểm tra quản lý luồng xử lý song song (Concurrency Threadpool và Asynchronous Background Task) làm mượt mà hiệu suất API, chấm dứt hoàn toàn tình trạng treo máy khi user gửi ảnh quá khủng đòi hỏi LLM mất nhiều phút giải mã.
* Niêm phong chỉn chu toàn bộ lối vào API bằng quy chuẩn bảo mật token thế giới JWT, khóa triệt để cổng rò rỉ trước thềm tổng kết khóa đào tạo thực tập FCJ.