### Mục tiêu tuần 7:

* Tích hợp Amazon Bedrock (các mô hình ngôn ngữ lớn) để bắt đầu nhận diện món ăn từ hình ảnh.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Khởi tạo Boto3 client giao tiếp với AWS Bedrock API | 16/02/2026   | 16/02/2026      | Boto3 Bedrock Docs |
| 3   | - Thực hiện inference test với các model Claude 3 qua Bedrock <br> - Đẩy thử nghiệm luồng ảnh đã được hàm nén (tuần 6) xử lý lên VLM endpoint | 17/02/2026   | 17/02/2026      |
| 4   | - Thiết kế Prompt (Prompt Engineering) định hướng AI: "Nhận dạng tất cả thức ăn trong hình" | 18/02/2026   | 18/02/2026      | Prompt templates |
| 5   | - Thử ghép kết quả LLM trả về với logic Mock Data đã viết ở tuần 5 | 19/02/2026   | 19/02/2026      |
| 6   | - Refactor lại cấu trúc Model trên backend để ẩn logic LLM đi <br> - Bổ sung check định dạng Token môi trường | 20/02/2026   | 20/02/2026      |

### Kết quả đạt được tuần 7:

* Ủy quyền thành công thông tin đăng nhập AWS để gửi request an toàn lấy inference từ dịch vụ Amazon Bedrock qua `boto3`.
* Hoàn thiện kết nối Cầu nối phân tích Ảnh (Image-to-text) thông qua việc gửi ảnh người dùng lên Cloud LLM và nhận lại danh sách các món ăn được phân loại.
* Thiết lập được các chỉ thị lệnh Prompt Engineering ban đầu giúp thu hẹp phạm vi ảo giác (hallucinations) của AI, ép model chỉ xuất chuỗi JSON định lượng dinh dưỡng.