# 🧠 Evaluating Encoder-Decoder Language Models for Simplifying Persian Legal Texts  

*A Bachelor's Project by Mohammadreza Joneidi*  
**Supervisor**: Prof. Nikoofard  

## 📌 Introduction  
This project evaluates the performance of **encoder-decoder language models** (e.g., T5 variants) in simplifying complex Persian legal texts into plain language for general audiences. Key challenges include preserving legal meaning while improving readability and leveraging limited labeled data.  

### Key Goals:  
- Compare models like `mlongT5` and `parsT5` for legal text simplification.  
- Incorporate **Unlimiformer** for handling long sequences.  
- Evaluate using readability scores, ROUGE, and BERTScore.  

---

## 🛠️ Technologies & Models  
### 🔧 Core Stack  
- **Models**:  
  - `mlongT5` (12-block encoder-decoder)  
  - `parsT5` (Persian-optimized T5)  
- **Libraries**: HuggingFace `transformers`, PyTorch  
- **Evaluation**: ROUGE, BERTScore, custom readability metrics  

### 🗃️ Dataset  
- **Source**: 5,000+ labeled Persian legal documents (decision texts, dates, etc.).  
- **Preprocessing**: Scraping, cleaning, and manual labeling for simplification.  
- **Split**: 85% train, 5% validation, 10% test.  

---

## 🚀 Implementation  
### Model Architectures  
- **Encoder**: Multi-head self-attention → Feed-forward → LayerNorm + Residual  
- **Decoder**: Masked self-attention → Feed-forward → Softmax  
- **Unlimiformer**: Extends context window for long legal texts.  

### Training  
- **Loss Plots**: Tracked for `mlongT5` and `parsT5` (include graphs in `docs/`).  
- **Hardware**: (Specify GPUs/TPUs if relevant).  

### Evaluation Metrics  
| Metric          | Purpose                          |  
|-----------------|----------------------------------|  
| **ROUGE**       | Text overlap with references     |  
| **BERTScore**   | Semantic similarity              |  
| **Readability** | Flesch-Kincaid-like scores       |  

*(Include a table of quantitative results if available)*  

---

## 📂 Repository Structure  
