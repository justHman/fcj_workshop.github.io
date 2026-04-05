### Mục tiêu tuần 8:

* Trình bày ứng dụng thông qua Giao diện người dùng đồ họa trực quan (Gradio).
* Trưởng thành hóa kiến trúc LLM bằng cách chuyển sang kỹ thuật "Tool Calling" định dạng ép chuẩn (JSON format) và giải quyết tính toán đồng thời nhiều món ăn.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Đồng bộ mã nguồn chính thức đầu tiên lên Github lưu trữ <br> - Xây dựng file `.env` chuẩn | 23/02/2026   | 23/02/2026      | Github Commit History |
| 3   | - Mở rộng code tính toán cho trường hợp một ảnh chứa rất nhiều loại thực phẩm <br> - Fix bug khi logic không tìm thấy gì (no items) và ngược lại | 24/02/2026   | 24/02/2026      |
| 4   | - Xây dựng kỹ thuật LLM Tool Calling để bẻ luồng Model chỉ được phép nói JSON thay vì chat văn xuôi thông thường <br> - Bắt đầu đưa biến theo dõi Token và Giá tiền vào code | 25/02/2026   | 25/02/2026      |
| 5   | - Vượt qua kiểm thử Regression cho API test với hàng loạt đồ vật (multiple items) <br> - Xử lý làm tròn số thập phân dư thừa trả về từ việc tính tổng JSON tool | 26/02/2026   | 26/02/2026      |
| 6   | - Lập trình màn hình UI demo Web trực tiếp sử dụng framework Gradio <br> - Đồng bộ luồng Test logic qua `test_all.ipynb` và API tự động | 27/02/2026   | 27/02/2026      | Gradio Library Docs |

### Kết quả đạt được tuần 8:

* Đã chính thức đẩy (commit) kết quả khởi tạo và kiến trúc lõi ứng dụng lên Repository, bảo vệ hoàn toàn lịch sử source file.
* Chuyển đổi thành công kiến trúc trò chuyện hội thoại AI thông thường sang hình thức gọi hàm ép cứng lập trình (Tool Calling), điều này giúp Backend LLM trả đối tượng JSON tiêu chuẩn thay vì các mảng text phi cấu trúc.
* Giải quyết triệt để rào cản nhận diện giới hạn, ứng dụng hiện nay đã phân tách và tra cứu dinh dưỡng được hàng loạt đồ vật phức tạp nằm chung trên 1 tấm hình (Multiple foods pipeline).
* Hoàn thiện và cấp phát Web UI demo qua Gradio, cải thiện tốc độ kiểm thử đầu-cuối (end-to-end) thay cho việc gọi từng HTTP requests khô khan bằng Postman.
* Xử lý trót lọt toàn bộ biên lỗi (edge cases), từ việc phát hiện ảnh rác không có đồ ăn nào cho tới kiểm soát dung lượng bytes hình ảnh.