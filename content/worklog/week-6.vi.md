### Mục tiêu tuần 6:

* Xây dựng hệ thống tiện ích nhận và nén ảnh (image compression utilities).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Cài đặt hàm tiện ích Resize ảnh dung lượng lớn từ người dùng đẩy lên | 09/02/2026   | 09/02/2026      | Python Pillow Docs |
| 3   | - Xử lý lỗi thư viện báo sai định dạng màu `RGBA` / `P` mode palette | 10/02/2026   | 10/02/2026      |
| 4   | - Quản lý cách server lưu lại ảnh tạm (temp files) khi users gửi request hình ảnh phân tích | 11/02/2026   | 11/02/2026      |
| 5   | - Bổ sung logic tự dọn dẹp các tệp hình ảnh tạm thời để tránh tràn bộ nhớ server | 12/02/2026   | 12/02/2026      |
| 6   | - Review lại quy trình nén và kiểm thử tính ổn định của luồng xử lý media | 13/02/2026   | 13/02/2026      |

### Kết quả đạt được tuần 6:

* Code thành công cơ chế tiếp nhận và nén ảnh dùng Pillow, bắt được triệt để lỗi khi user tải lên các định dạng ảnh có palette màu giới hạn (P-mode).
* Xây dựng luồng tải ảnh an toàn, giải thiểu tốn kém bộ nhớ khi xử lý inference.
* Tự động hóa quá trình thu dọn file tạm sau khi đẩy quá model, duy trì tải trọng siêu việt cho server.