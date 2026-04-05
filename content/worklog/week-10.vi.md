### Mục tiêu tuần 10:

* Hoàn thành đồng bộ dữ liệu chéo nhau giữa các API quét mã vạch (Barcode Pipelines).
* Tối ưu hóa tối đa các chỉ số Token của LLM, theo dõi tốc độ phản hồi máy chủ và kiểm soát bảng giá dịch vụ API AI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Mở rộng kiểm thử (Testing) cho cơ sở dữ liệu FDB bổ sung <br> - Đồng bộ Output định dạng Barcode cho 3 bộ Client liền lúc (USDA, OpenFoodFacts, FDB) | 09/03/2026   | 09/03/2026      |
| 3   | - Thiết lập crawler thu thập dữ liệu (data cache) chống gọi request lặp lại <br> - Xử lý logic ghi Log của console trên Amazon ECS môi trường sau này `LOG_TO_FILE` | 10/03/2026   | 10/03/2026      |
| 4   | - Thay máu toàn bộ cấu trúc câu lệnh Prompt gốc nhằm hạ thiểu Token-context bị ngốn vô ích <br> - Tinh chỉnh cơ chế hàm Clear tự động lọc rác text văn xuôi trước khi JSON decode | 11/03/2026   | 11/03/2026      |
| 5   | - Bổ sung các biến thống kê đếm số lượng Token Input (đầu vào), Token Output (đầu ra), tính toán ra thẳng Số tiền USD và Tốc độ giây chạy của 1 request | 12/03/2026   | 12/03/2026      |
| 6   | - Mang kinh nghiệm tối ưu Prompt ở luồng ảnh bình thường áp dụng mượt mà qua luồng đọc ảnh nhãn mác (Label Analysis) | 13/03/2026   | 13/03/2026      |

### Kết quả đạt được tuần 10:

* Giải quyết thành công rào cản đồng bộ dữ liệu trên diện rộng. Nhờ vậy, không cần biết Barcode bắn về từ kho dữ liệu nào trong 3 bộ Client (FDB, USDA, OpenFoodFacts), đầu ra backend luôn là một bản JSON định dạng khuôn mẫu tuyệt đối.
* Áp dụng hàng loạt kỹ thuật nhồi/tiết chế token đỉnh cao giúp giảm hao phí lượng context dư thừa đi vào quá trình gọi Amazon Bedrock, vừa tăng tính rẻ đỏ (cost margin) vừa tăng vọt tốc độ phản hồi dữ liệu (low latency).
* Viết thành công công cụ Crawl hỗ trợ Cache để giảm thiểu việc ping server ngoài liên tục tốn thời gian.
* Ra mắt bộ thống kê đo độ tiêu hao toàn cục trên Backend, ghi lại rõ ràng bao nhiêu tiền, bao nhiêu tokens, chạy mất mấy giây khi mỗi tấm hình phân tích bay qua server.