# Nền tảng NutriTrack
## Giải pháp AWS Serverless toàn diện cho Theo dõi Dinh dưỡng tích hợp AI

### 1. Tóm tắt Dự án (Executive Summary)
Nền tảng NutriTrack được thiết kế cho [Đối tượng mục tiêu / Nhóm người dùng] nhằm nâng cao khả năng quản lý sức khỏe cá nhân và theo dõi dữ liệu dinh dưỡng. Nền tảng hỗ trợ [Quy mô người dùng, ví dụ: 5.000+ người dùng hoạt động], sử dụng giao diện di động đa nền tảng (React Native/Expo) để thu thập và phân tích dữ liệu chế độ ăn uống. Nền tảng tận dụng các dịch vụ AWS Serverless (AWS Amplify Gen 2, AppSync, Lambda) và Generative AI (Amazon Bedrock, Google Gemini) để cung cấp khả năng theo dõi dinh dưỡng thời gian thực, tự động tạo dữ liệu món ăn bằng AI dự đoán ("Gen Food") và tối ưu chi phí, với quyền truy cập được bảo mật qua [Dịch vụ Xác thực, ví dụ: Amazon Cognito].

### 2. Tuyên bố Vấn đề (Problem Statement)
**Vấn đề là gì?**
Các ứng dụng theo dõi dinh dưỡng hiện tại đòi hỏi người dùng phải nhập liệu thủ công một cách tẻ nhạt và thường thiếu các cơ sở dữ liệu món ăn cá nhân hóa phong phú. Chưa có một hệ thống thông minh, tập trung nào tích hợp AI theo thời gian thực để tạo ra các hồ sơ món ăn bị thiếu. Các API của bên thứ ba hiện có có thể đắt đỏ và quá cứng nhắc đối với các nhu cầu ăn kiêng năng động.

**Giải pháp**
Nền tảng sử dụng AWS AppSync GraphQL API để tiếp nhận dữ liệu ăn uống của người dùng, AWS Lambda để xử lý logic backend, Amazon DynamoDB để lưu trữ có khả năng mở rộng, và Amazon Bedrock/Google Gemini cho luồng AI "Gen Food" nhằm tạo dữ liệu dinh dưỡng bị hụt ngay lập tức. AWS Amplify Gen 2 kết hợp với React Native/Expo cung cấp giao diện người dùng. Các tính năng chính bao gồm dashboard trực quan theo thời gian thực (hiển thị đạm, carbs, chất béo, calo), phân tích xu hướng và dịch vụ tìm kiếm món ăn bằng AI.

**Lợi ích và Tỷ suất Hoàn vốn (ROI)**
Giải pháp này thiết lập một hệ sinh thái nền tảng cốt lõi giúp người dùng theo dõi sức khỏe và giúp đội ngũ phát triển mở rộng quy mô một ứng dụng sức khỏe tích hợp AI. Nó giảm bớt rào cản khi nhập liệu thủ công nhờ vào luồng "Gen Food", đơn giản hóa trải nghiệm người dùng và cải thiện độ tin cậy của dữ liệu. Chi phí vận hành hàng tháng được duy trì ở mức tối thiểu thông qua mô hình serverless (dùng bao nhiêu trả bấy nhiêu). Thời gian hoàn vốn ước tính khoảng [Khoảng thời gian, ví dụ: 6-12 tháng], đạt được thông qua [Mô hình Doanh thu, ví dụ: phí đăng ký của người dùng hoặc sự tiết kiệm đáng kể thời gian, công sức].

### 3. Kiến trúc Giải pháp
Nền tảng sử dụng kiến trúc serverless của AWS để quản lý dữ liệu người dùng và các phản hồi từ AI một cách mượt mà. Dữ liệu được xử lý qua GraphQL API (AppSync), lưu trữ trong DynamoDB và làm phong phú thêm thông qua các hàm Lambda kết nối với Bedrock/Gemini. Ứng dụng di động được lưu trữ và triển khai bởi AWS Amplify.

*Kiến trúc Ứng dụng Di động NutriTrack*
*[Placeholder cho Sơ đồ Kiến trúc]*

*Kiến trúc Nền tảng NutriTrack*
*[Placeholder cho Sơ đồ Kiến trúc]*

**Các dịch vụ AWS được sử dụng**
* **AWS Amplify Gen 2:** Điều phối triển khai và lưu trữ môi trường backend.
* **AWS AppSync:** Hỗ trợ giao tiếp GraphQL API bảo mật giữa ứng dụng React Native và backend.
* **AWS Lambda:** Xử lý logic nghiệp vụ và kích hoạt gọi API của Bedrock/Gemini (ví dụ: các handler `ask-bedrock`).
* **Amazon DynamoDB:** Lưu trữ hồ sơ người dùng, nhật ký và mô hình dữ liệu dinh dưỡng ở định dạng noSQL có khả năng mở rộng cao.
* **Amazon Bedrock / Google Gemini:** Cung cấp sức mạnh cho tính năng "Gen Food" bằng AI để tạo động các hồ sơ vi chất (macronutrient).
* **Amazon Cognito:** Bảo mật truy cập và quản lý token JWT định danh cho việc xác thực người dùng.

**Thiết kế Thành phần**
* **Thiết bị Khách (Client):** Ứng dụng di động React Native/Expo thu thập đầu vào của người dùng và trực quan hóa dữ liệu dinh dưỡng (sử dụng các UI component như Hexagon Radar hoặc Concentric Rings).
* **Tiếp nhận Dữ liệu:** AppSync nhận các truy vấn/sửa đổi (GraphQL mutations/queries) từ ứng dụng di động.
* **Lưu trữ Dữ liệu:** Các bảng DynamoDB quản lý an toàn nhật ký ăn uống và dữ liệu dinh dưỡng.
* **Xử lý AI:** Các hàm Lambda định dạng yêu cầu (ví dụ: `gen_food_prompt.py`) và giao tiếp với API của Bedrock/Gemini.
* **Quản lý Người dùng:** Cognito xử lý đăng ký, đăng nhập và quản lý kiểm soát truy cập định danh.

### 4. Triển khai Kỹ thuật
**Các Giai đoạn Triển khai** 
Dự án này tuân theo 4 giai đoạn:
1. **Xây dựng Nền tảng và Thiết kế Kiến trúc:** Nghiên cứu cấu hình React Native/Expo với AWS Amplify Gen 2 và thiết kế kiến trúc serverless bao gồm cấu hình tích hợp AI Bedrock (Tháng 0).
2. **Tính toán Chi phí và Kiểm tra Tính khả thi:** Sử dụng AWS Pricing Calculator để ước tính chi phí (gọi Lambda, lượng token Bedrock, dung lượng DynamoDB) và điều chỉnh kiến trúc nếu cần (Tháng 1).
3. **Phát triển, Kiểm thử, và Triển khai:** Lập trình UI React Native, backend AWS với TypeScript/CDK, triển khai các handler `ask-bedrock` Lambda, và giải quyết các luồng xác thực token. Kiểm thử và đưa lên môi trường Production (Tháng 2-3).
4. **Tinh chỉnh và Tối ưu hóa:** Audit đánh giá UX/UI, cải thiện biểu đồ dữ liệu vĩ mô và sửa lỗi tích hợp (ví dụ: lỗi token JWT định danh) (Sau khi Launch).

**Yêu cầu Kỹ thuật**
* **Frontend:** React Native, Expo, TypeScript. Yêu cầu thiết kế kiểu dáng động phức tạp (Linear Dashboard/Rings). 
* **Backend:** Có kỹ năng thực tế về AWS Amplify Gen 2, Lambda, AppSync (GraphQL), DynamoDB và Cognito.
* **Tích hợp AI:** Kinh nghiệm với Amazon Bedrock API, Google Gemini, và các thức prompt engineering hiệu quả.

### 5. Lịch trình & Cột mốc (Timeline & Milestones)
**Lịch trình Dự án**
* **Giai đoạn Tiền kỳ (Tháng 0):** 1 tháng cho thiết kế UI/UX, đánh giá phiên bản tài liệu cũ và phác thảo kiến trúc.
* **Triển khai (Tháng 1-3):** 3 tháng.
  * **Tháng 1:** Cài đặt môi trường AWS và xây dựng UI cơ bản của React Native.
  * **Tháng 2:** Kết nối AppSync API, tạo schema DynamoDB và tích hợp xác thực Cognito.
  * **Tháng 3:** Triển khai Lambda Bedrock AI "Gen Food", kiểm thử đầu cuối (E2E), sửa lỗi và phát hành.
* **Sau khi Phát hành (Post-Launch):** Tối ưu hóa liên tục và mở rộng quy mô người dùng trong vòng [Khoảng thời gian Cụ thể, ví dụ: 1 năm].

### 6. Ước tính Ngân sách
Bạn có thể tìm thấy ước tính ngân sách trên AWS Pricing Calculator.
Hoặc bạn có thể tải xuống Tệp Ước tính Ngân sách [Placeholder Liên kết].

**Chi phí Hạ tầng (Ước lượng)**
* **AWS Lambda:** $[Placeholder]/tháng (ví dụ: 1.000.000 yêu cầu, 512 MB lưu trữ).
* **Amazon DynamoDB:** $[Placeholder]/tháng (Lưu trữ, Năng lực đọc/ghi).
* **AWS AppSync:** $[Placeholder]/tháng (Truy vấn API).
* **Amazon Bedrock / Gemini APIs:** $[Placeholder]/tháng (Dựa trên khối lượng token đầu vào/đầu ra được xử lý).
* **AWS Amplify & Cognito:** $[Placeholder]/tháng.
* **Tổng ước lượng:** $[Placeholder]/tháng, $[Placeholder]/12 tháng.

**Chi phí Phần mềm/Bản quyền:** $[Placeholder] (ví dụ: Tài khoản nhà phát triển, công cụ CI/CD).

### 7. Đánh giá Rủi ro
**Ma trận Rủi ro**
* **Vượt quá ngân sách (AI APIs):** Tác động trung bình, xác suất trung bình.
* **Lỗi Xác thực (Cognito/JWT tokens):** Tác động cao, xác suất thấp.
* **Ảo giác AI (Dữ liệu món ăn không chính xác):** Tác động trung bình, xác suất trung bình.

**Chiến lược Giảm thiểu (Mitigation Strategies)**
* **Chi phí:** Thực hiện giới hạn API nghiêm ngặt (rate limiting), lưu cache kết quả trong DynamoDB, và cài đặt cảnh báo ngân sách AWS.
* **Xác thực:** Kiểm thử E2E toàn diện đối với luồng nhận dạng của Cognito; sử dụng các local session dự phòng.
* **Độ chính xác AI:** Tinh chỉnh prompt hệ thống (`gen_food_prompt.py`), yêu cầu định dạng JSON schema chặt chẽ cho output, và bổ sung các bước xác minh dữ liệu từ người dùng.

**Kế hoạch Dự phòng (Contingency Plans)**
* Trở lại tính năng nhập món ăn thủ công nếu AI hay Bedrock gặp sự cố.
* Sử dụng CloudFormation/Amplify để rollback khi backend bị lỗi.

### 8. Kết quả Mong đợi
**Cải tiến Kỹ thuật:**
* Thu thập dữ liệu dinh dưỡng tự động theo thời gian thực thay thế các quy trình thủ công vất vả nhờ có AI.
* Hệ thống backend serverless với khả năng mở rộng cao, có thể chịu tải [Ví dụ: 10.000+] người dùng hoạt động đồng thời.

**Giá trị Dài hạn**
* Thiết lập cơ sở dữ liệu món ăn mở rộng, uy tín được tạo hữu cơ từ người dùng và AI.
* Cung cấp các cấu trúc phát triển AI sinh chuẩn mẫu (reusable patterns) cho các tính năng và sản phẩm sức khỏe tương lai.