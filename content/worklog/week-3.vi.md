### Mục tiêu tuần 3:

* Hiểu foundation của các mô hình ngôn ngữ lớn (LLM) hiện đại.
* Nắm vững kiến trúc Transformer và cơ chế hoạt động của GPT.
* Thực hành xây dựng tokenizer và chuẩn bị dữ liệu cho LLM.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu kiến trúc Transformer: <br>&emsp; + Cơ chế Encoder-Decoder <br>&emsp; + Self-Attention mechanism <br>&emsp; + So sánh BERT vs GPT <br> - Phân biệt Transformer vs LLM <br> - Hiểu foundation của tất cả mô hình ngôn ngữ hiện đại | 19/01/2026   | 19/01/2026      | Lecture 4: What are transformers? |
| 3   | - Tìm hiểu cơ chế hoạt động của GPT-3: <br>&emsp; + Kiến trúc Decoder-only <br>&emsp; + Auto-regressive & Unsupervised learning <br>&emsp; + Zero-shot vs Few-shot learning <br> - Lộ trình xây dựng LLM từ scratch: <br>&emsp; + Building Blocks (Tokenization, Attention) <br>&emsp; + Pre-training & Fine-tuning stages | 20/01/2026   | 20/01/2026      | Lecture 5 & 6: GPT-3 & LLM Roadmap |
| 4   | - Xây dựng LLM Tokenizer từ scratch với Python: <br>&emsp; + Tìm hiểu quy trình tokenization cơ bản <br>&emsp; + Tách từ và xây dựng vocabulary <br>&emsp; + Xử lý special tokens (unk, endoftext) <br> - **Thực hành:** <br>&emsp; + Code SimpleTokenizer class <br>&emsp; + Implement encode/decode methods | 21/01/2026   | 21/01/2026      | Lecture 7: Code LLM Tokenizer |
| 5   | - Tìm hiểu GPT Tokenizer & Byte Pair Encoding (BPE): <br>&emsp; + So sánh các phương pháp tokenization <br>&emsp; + Hiểu cơ chế hoạt động BPE <br>&emsp; + Ưu điểm của subword tokenization <br> - **Thực hành:** <br>&emsp; + Sử dụng tiktoken library <br>&emsp; + Encode/decode text với BPE | 22/01/2026   | 22/01/2026      | Lecture 8: GPT Tokenizer |
| 6   | - Tạo cặp dữ liệu Input-Target cho LLM: <br>&emsp; + Next-word prediction mechanism <br>&emsp; + Sliding window technique <br>&emsp; + Xây dựng GPTDatasetV1 class <br> - **Thực hành:** <br>&emsp; + Code PyTorch Dataset & DataLoader <br>&emsp; + Batching và shuffle dữ liệu | 23/01/2026   | 23/01/2026      | Lecture: Data Preparation with DataLoader |


### Kết quả đạt được tuần 3:

* Nắm vững kiến trúc Transformer - foundation của tất cả LLM hiện đại:
  * Hiểu cơ chế Encoder-Decoder
  * Nắm được Self-Attention mechanism
  * Phân biệt được BERT vs GPT architecture
  * Hiểu sự khác biệt giữa Transformer và LLM

* Hiểu sâu về cơ chế hoạt động của GPT-3:
  * Decoder-only architecture
  * Auto-regressive và Unsupervised learning
  * Zero-shot vs Few-shot learning capabilities
  * Emergent behaviors và chi phí huấn luyện

* Nắm được lộ trình 3 giai đoạn xây dựng LLM từ scratch:
  * Building Blocks (Tokenization, Attention)
  * Pre-training (tạo Base Model)
  * Fine-tuning (tạo specialized model)

* Thực hành xây dựng LLM Tokenizer từ con số 0:
  * Code SimpleTokenizer class với Python
  * Implement encode/decode methods
  * Xử lý special tokens (unk, endoftext)
  * Hiểu được quy trình tokenization cơ bản

* Làm chủ GPT Tokenizer và Byte Pair Encoding:
  * So sánh các phương pháp tokenization
  * Hiểu cơ chế và ưu điểm của BPE
  * Sử dụng thành thạo tiktoken library
  * Encode/decode text với subword tokenization

* Chuẩn bị dữ liệu huấn luyện cho LLM:
  * Hiểu cơ chế next-word prediction
  * Áp dụng sliding window technique
  * Xây dựng GPTDatasetV1 class với PyTorch
  * Sử dụng DataLoader để batching và shuffle dữ liệu

* Có nền tảng vững chắc để tiến đến việc xây dựng và huấn luyện mô hình LLM hoàn chỉnh.