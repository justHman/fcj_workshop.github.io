### Week 3 Objectives:

* Understand the foundation of modern Large Language Models (LLMs).
* Master the Transformer architecture and GPT's operational mechanisms.
* Practice building a tokenizer and preparing data for LLMs.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Understand Transformer architecture: <br>&emsp; + Encoder-Decoder mechanism <br>&emsp; + Self-Attention mechanism <br>&emsp; + BERT vs GPT comparison <br> - Differentiate Transformer vs LLM <br> - Understand the foundation of all modern language models | 19/01/2026   | 19/01/2026      | Lecture 4: What are transformers? |
| 3   | - Investigate GPT-3's operational mechanism: <br>&emsp; + Decoder-only architecture <br>&emsp; + Auto-regressive & Unsupervised learning <br>&emsp; + Zero-shot vs Few-shot learning <br> - Roadmap for building LLM from scratch: <br>&emsp; + Building Blocks (Tokenization, Attention) <br>&emsp; + Pre-training & Fine-tuning stages | 20/01/2026   | 20/01/2026      | Lecture 5 & 6: GPT-3 & LLM Roadmap |
| 4   | - Build an LLM Tokenizer from scratch with Python: <br>&emsp; + Understand the basic tokenization process <br>&emsp; + Split words and build vocabulary <br>&emsp; + Handle special tokens (unk, endoftext) <br> - **Practice:** <br>&emsp; + Code SimpleTokenizer class <br>&emsp; + Implement encode/decode methods | 21/01/2026   | 21/01/2026      | Lecture 7: Code LLM Tokenizer |
| 5   | - Explore GPT Tokenizer & Byte Pair Encoding (BPE): <br>&emsp; + Compare tokenization methods <br>&emsp; + Understand BPE operational mechanism <br>&emsp; + Advantages of subword tokenization <br> - **Practice:** <br>&emsp; + Use tiktoken library <br>&emsp; + Encode/decode text with BPE | 22/01/2026   | 22/01/2026      | Lecture 8: GPT Tokenizer |
| 6   | - Create Input-Target data pairs for LLM: <br>&emsp; + Next-word prediction mechanism <br>&emsp; + Sliding window technique <br>&emsp; + Build GPTDatasetV1 class <br> - **Practice:** <br>&emsp; + Code PyTorch Dataset & DataLoader <br>&emsp; + Batching and shuffling data | 23/01/2026   | 23/01/2026      | Lecture: Data Preparation with DataLoader |


### Week 3 Achievements:

* Mastered the Transformer architecture - the foundation of all modern LLMs:
  * Understood the Encoder-Decoder mechanism
  * Grasped the Self-Attention mechanism
  * Effectively distinguished BERT vs GPT architecture
  * Understood the difference between standard Transformers and LLMs

* Gained deep understanding of GPT-3's working mechanism:
  * Decoder-only architecture
  * Auto-regressive and Unsupervised learning implementations
  * Zero-shot vs Few-shot learning capabilities
  * Emergent behaviors and training cost implications

* Grasped the 3-stage roadmap for building an LLM from scratch:
  * Building Blocks (Tokenization, Attention)
  * Pre-training (creating Base Model)
  * Fine-tuning (creating specialized model)

* Practical implementation of LLM Tokenizer from scratch:
  * Coded SimpleTokenizer class with Python
  * Implemented encode/decode methods effectively
  * Handled special tokens (unk, endoftext)
  * Deeply understood the basic tokenization process

* Mastered GPT Tokenizer and Byte Pair Encoding (BPE):
  * Compared different tokenization methods comprehensively
  * Understood the mechanism and benefits of BPE
  * Proficiently operated the tiktoken library
  * Successfully encoded/decoded text using subword tokenization

* Prepared training data for LLMs:
  * Understood the next-word prediction mechanism
  * Applied the sliding window technique accurately
  * Built GPTDatasetV1 class relying on PyTorch
  * Utilized DataLoader for effective data batching and shuffling

* Established a solid foundation to proceed toward building and training complete LLM architectures.