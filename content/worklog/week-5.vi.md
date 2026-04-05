### Mục tiêu tuần 5:

* Thiết lập nền tảng backend sử dụng FastAPI.
* Viết các class Python (wrappers) để gọi các API lấy dữ liệu bên ngoài.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Cài đặt framework FastAPI và thư viện `uvicorn` <br> - Phân bổ cấu trúc routing cho backend trong `app/api` | 02/02/2026   | 02/02/2026      | FastAPI Documentation |
| 3   | - Code class wrapper giao tiếp với endpoint của USDA <br> - Triển khai bộ HTTP client tĩnh | 03/02/2026   | 03/02/2026      |
| 4   | - Viết module wrapper giao tiếp với OpenFoodFacts <br> - Dịch JSON trả về dựa trên barcode thực tế kiểm tra lỗi | 04/02/2026   | 04/02/2026      |
| 5   | - Chuẩn hóa kịch bản phát sinh xử lý Mock Data (Dữ liệu giả lập fallback) khi không cung cấp API tokens | 05/02/2026   | 05/02/2026      |
| 6   | - Tích hợp các bộ API rời rạc vào luồng chạy chính `api.py` <br> - Mở server local và quan sát, test endpoint thông qua màn hình tự động `/docs` Swagger UI | 06/02/2026   | 06/02/2026      | Swagger UI Docs |

### Kết quả đạt được tuần 5:

* Khởi tạo thành công server backend chạy trên FastAPI có khả năng mở rộng tốt.
* Tích hợp thành công client giao tiếp gọi dữ liệu USDA API kèm theo cơ cấu parse dữ liệu.
* Tích hợp thành công client thu thập dữ liệu barcode quét trên OpenFoodFacts.
* Thiết lập được chức năng Mock data trả về dữ liệu giả lập dự phòng an toàn, giúp developer test app kể cả khi thiếu API keys thực.
* Nghiệm thu vận hành hệ thống thông qua giao diện trực quan Swagger UI một cách hoàn chỉnh.