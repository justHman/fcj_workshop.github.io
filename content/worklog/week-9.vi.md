### Mục tiêu tuần 9:

* Tiến hành đóng gói môi trường mã nguồn bằng công nghệ Container (Docker).
* Khởi tạo các module nền tảng hỗ trợ việc Phân tích và quét chữ trên nhãn mác dinh dưỡng (Label Analysis).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tổng hợp danh sách thư viện chuẩn `requirements.txt` <br> - Khởi tạo `Dockerfile` cơ bản để bọc (wrap) code Python vào | 02/03/2026   | 02/03/2026      | Docker Reference Docs |
| 3   | - Rà soát dọn dẹp mã nguồn thừa (trash files) <br> - Fix lại quy tắc `.gitignore` và đặc biệt là file `.dockerignore` | 03/03/2026   | 03/03/2026      |
| 4   | - Dọn sạch (Clear) bộ nhớ cache của Git để tống khứ các file rác từng lỡ tay đẩy lên repo | 04/03/2026   | 04/03/2026      |
| 5   | - Bẻ nhánh luồng xử lý ảnh LLM để phục vụ cho nhu cầu quét chữ nhãn mác vật lý <br> - Thiết kế Prompt chuyên biệt để đọc số liệu dinh dưỡng | 05/03/2026   | 05/03/2026      |
| 6   | - Tinh chỉnh hệ thống Analyze Label sao cho kết quả bóc tách từ nhãn vật lý tự động điền vào định dạng chuẩn của JSON hệ thống | 06/03/2026   | 06/03/2026      |

### Kết quả đạt được tuần 9:

* Đóng gói Docker hoàn chỉnh cho hệ thống backend, chia sẻ môi trường đồng bộ để mọi thành viên/ban bệ máy tính khác nhau đều có thể chạy bằng một lệnh cực kì gọn gàng.
* Giảm thiểu cấu trúc thừa tải cho source code nhờ việc viết lại tập hợp bỏ qua file `.dockerignore` khắt khe song song với `.gitignore`. Đẩy lùi hoàn toàn tài nguyên rác khỏi file Docker.
* Nâng trình độ AI của nền tảng lên một nấc bằng kịch bản xử lý (pipeline) Trích xuất thông tin Nhãn hiệu. AI giờ đã có thể quy chiếu chụp một bảng thành phần sau chai nước và tự parse ra thành biểu mẫu dữ liệu dinh dưỡng mà code đọc được.