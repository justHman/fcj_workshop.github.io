### Mục tiêu tuần 4:

* Khởi tạo dự án backend NutriTrack và thiết kế cấu trúc thư mục nền tảng.
* Khảo sát và thu thập tài liệu về các API dinh dưỡng từ bên thứ 3 (OpenFoodFacts, USDA).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Khởi tạo kho chứa (repository) NutriTrack <br> - Cài đặt môi trường ảo Python (`.venv`) <br> - Phân bổ thư mục code ban đầu (app, docs, third_apis) | 26/01/2026   | 26/01/2026      |
| 3   | - Phân tích tài liệu tích hợp API của USDA <br> - Đăng ký API Keys hợp lệ <br> - Thử nghiệm gọi request mẫu qua `curl` / Postman | 27/01/2026   | 27/01/2026      | USDA FDC API Docs |
| 4   | - Đánh giá OpenFoodFacts API để phục vụ quét mã vạch (barcode) <br> - Nghiên cứu định dạng dữ liệu JSON trả về <br> - So sánh chất lượng dữ liệu với USDA | 28/01/2026   | 28/01/2026      | OpenFoodFacts API Docs |
| 5   | - Thiết lập cơ chế cấu hình môi trường qua `.env` <br> - Viết note lại cấu trúc bảo mật API keys | 29/01/2026   | 29/01/2026      |
| 6   | - Lên danh sách các thuộc tính dữ liệu dinh dưỡng cốt lõi (Calories, đạm, béo, tinh bột) <br> - Vạch trước kiến trúc (wrapper) để bọc các API bên thứ 3 | 30/01/2026   | 30/01/2026      |

### Kết quả đạt được tuần 4:

* Thiết lập thành công cấu trúc dự án backend NutriTrack, cách ly môi trường thư viện an toàn với Python `.venv`.
* Xác thực kiểm thử endpoint mẫu của USDA API, sẵn sàng token kết nối cho bước lập trình tiếp theo.
* Khảo sát xong OpenFoodFacts và thống nhất chiến lược tận dụng cơ sở dữ liệu này cho tính năng barcode lookup.
* Chuẩn bị cơ chế quản lý file `.env` chuẩn mực nhằm tránh lộ lọt private keys khi sử dụng version control.
* Hình thành được sơ đồ lớp dữ liệu chuẩn (Mapping) để đồng bộ nội dung trả về khác nhau của các API bên thứ 3 thành một chuẩn duy nhất nội bộ.