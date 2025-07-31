# 📜 Persian Legal Text Simplification Leveraging Transformer-Based Models  
**Bachelor's Project** · *Mohammadreza Joneidi Jafari* · **Supervisor:** Prof. Nikoofard  


## 🔍 Introduction  
This project evaluates **encoder-decoder models** (`mlongT5` and `parsT5`) for simplifying complex Persian legal texts into plain language. We compared these 2 tuned models with 2 Persian LLM models based on Llama. Key contributions:  
- **Optimizer Comparison**: AdamW vs. LAMB vs. SGD (AdamW achieved best performance).  
- **Unlimiformer Integration**: Handles long legal documents effectively for parsT5 model.
- **Rigorous Metrics**: ROUGE, BERTScore, and custom readability scores.  

---

## 🏆 Key Results  

### Model Comparison (AdamW Optimizer)  
| Model       | ROUGE-1 | ROUGE-2 | ROUGE-L | BERTScore-f1 |
|-------------|---------|---------|---------|--------------| 
| **ParsT5 (1 Block)** | <ins>38.08%</ins>    | **15.83%**    | <ins>19.41%</ins>    | <ins>73.71%</ins>         |   
| **ParsT5 (3 Blocks)**  | **38.4%**    | <ins>15.61%</ins>    | **23.18%**    | **75.13%**         |  
| **mlongT5 (1 Blocks)**  | 27.94%    | 1.77%   | 11.22%    | 64.89%         | 
| **mlongT5 (3 Blocks)**  | 25.36%    | 1.23%   | 10.81%    | 49.46%         | 
| **[PersianLlaMA-13B](https://huggingface.co/ViraIntelligentDataMining/PersianLLaMA-13B)**  | 28.64%    | 9.81%    | 13.67%  | 70.80%  | 
| **[AVA Llama_3_V2](https://huggingface.co/MehdiHosseiniMoghadam/AVA-Llama-3-V2)**  | 30.07%   | 10.33%    | 16.39%    | 70.87%      |

---
🌐 Model Hosted on Hugging Face
You can access and use this model directly via the Hugging Face Hub:

Link: [simplification-legal-text](https://huggingface.co/Moryjj/simplification-legal-text)

---
## 🛠️ Technologies  
### Models & Training  
- **Models**: `mlongT5` (12-block), `parsT5` (12-block), `Unlimiformer` (long-context).  
- **Optimizers**: AdamW (best), LAMB, SGD.  
- **Framework**: PyTorch + HuggingFace `transformers`.  
- **Hardware**: (Specify GPUs/TPUs if applicable).

  
---


## 🔗 Links

- **[mlongT5](https://huggingface.co/agemagician/mlong-t5-tglobal-base)**
- **[parsT5](https://huggingface.co/Ahmad/parsT5-base)**
- **[Unlimiformer](https://github.com/abertsch72/unlimiformer)**

---


## Dataset  
- **5,000+ Persian legal texts** (decision texts, dates)  
- **Split**: 85% train, 5% validation, 10% test.  
- **Preprocessing**: Scraping, manual labeling for simplification.  

---

## Contact
For questions, collaborations, or access to the full dataset, feel free to reach out:

📧 Email: m.r.joneidi.02@gmail.com


🔗 LinkedIn: Mohammadreza Joneidi Jafari
