### Mục tiêu tuần 11:

* Đưa dự án tiến tới môi trường Production thực tế (Deploy lên hệ sinh thái trạm biên Fly.io).
* Tự động hóa triệt để dây chuyền tích hợp phân phối mã nguồn (CI/CD) qua Github Actions.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Hiện thực hóa quy chuẩn Hạ tầng dưới dạng Code (IaC) thiết lập dựa vào Terraform <br> - Khởi tạo kịch bản `.yml` xây CI/CD tự động bằng Github Actions | 16/03/2026   | 16/03/2026      | GitHub Actions Docs |
| 3   | - Quản lý và chặn rò rỉ mã Secret từ Github Action <br> - Code luồng tự động đẩy source qua các kịch bản lệnh SSH | 17/03/2026   | 17/03/2026      |
| 4   | - Thực nghiệm thả cấu trúc backend chạy trên môi trường Edge Network của Fly.io | 18/03/2026   | 18/03/2026      | Fly.io documentation |
| 5   | - Viết kịch bản truyền dẫn (SFTP) thu/phát cục Cache (upload/download) qua lại giữa Git Runner và Volume vật lý của Fly.io | 19/03/2026   | 19/03/2026      |
| 6   | - Fix bug nghiêm trọng luồng CI/CD Fly.io: Máy ảo bị chết (die VM) sập bất thình lình trước khi tiến trình truyền Cache kịp kết thúc | 20/03/2026   | 20/03/2026      |

### Kết quả đạt được tuần 11:

* Chinh phục toàn diện dây chuyền CI/CD Github Actions. Mọi commit giờ đây đều tự động kích hoạt tiến trình kiểm định trơn tru, đẩy (push) code tự động hoàn toàn thay cho sức người.
* Gỡ rối xuất sắc bài toán truyền dẫn Cache của nhà mạng đám mây Fly.io dựa trên khái thác luồng SFTP, di chuyển thành công hệ thống bộ nhớ từ máy Git lên máy ảo Cloud VM.
* Giải quyết triệt để rủi ro Sập Server giữa chừng (VM die) lúc đang truyền tải tệp năng thông qua việc tinh chỉnh cờ ping máu (Healthcheck delays) trong quy trình deploy ứng dụng.