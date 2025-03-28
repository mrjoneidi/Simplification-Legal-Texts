# 📜 Evaluating Encoder-Decoder Models for Persian Legal Text Simplification  
**Bachelor's Project** · *Mohammadreza Joneidi* · **Supervisor:** Prof. Nikoofard  

![Persian Legal Text Simplification Pipeline](assets/pipeline.png) 

## 🔍 Introduction  
This project evaluates **encoder-decoder models** (`mlongT5` and `parsT5`) for simplifying complex Persian legal texts into plain language. We compared these 2 tuned models with 2 Persian LLM model based on Llama. Key contributions:  
- **Optimizer Comparison**: AdamW vs. LAMB vs. SGD (AdamW achieved best performance).  
- **Unlimiformer Integration**: Handles long legal documents effectively.  
- **Rigorous Metrics**: ROUGE, BERTScore, and custom readability scores.  

---

## 🏆 Key Results  

### Model Comparison (AdamW Optimizer)  
| Model       | ROUGE-1 | ROUGE-2 | ROUGE-L | BERTScore-f1 |
|-------------|---------|---------|---------|--------------| 
| **mlongT5** | 0.75    | 0.58    | 0.72    | 0.82         |   
| **parsT5**  | 0.78    | 0.61    | 0.74    | 0.85         |  
| **[PersianLlaMA-13B](https://huggingface.co/ViraIntelligentDataMining/PersianLLaMA-13B)**  | 0.78    | 0.61    | 0.74  | 0.85  | 
| **AVA Llama_3_V2**  | 0.78    | 0.61    | 0.74    | 0.85      |

*`parsT5` (Persian-optimized) slightly outperformed `mlongT5` across all metrics.*  

---

## 🛠️ Technologies  
### Models & Training  
- **Models**: `mlongT5` (12-block), `parsT5` (12-block), `Unlimiformer` (long-context).  
- **Optimizers**: AdamW (best), LAMB, SGD.  
- **Framework**: PyTorch + HuggingFace `transformers`.  
- **Hardware**: (Specify GPUs/TPUs if applicable).  

### Dataset  
- **6,000+ Persian legal texts** (decision texts, dates).  
- **Split**: 85% train, 5% validation, 10% test.  
- **Preprocessing**: Scraping, manual labeling for simplification.  

---

## 📂 Repository Structure  
