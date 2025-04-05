# 📜 Evaluating Encoder-Decoder Models for Persian Legal Text Simplification  
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
| **mlongT5** | 27.94%    | 1.77%    | 11.22%    | 64.89%         |   
| **parsT5**  | **38.08%**    | **15.83%**    | **19.41%**    | **73.71%**         |  
| **[PersianLlaMA-13B](https://huggingface.co/ViraIntelligentDataMining/PersianLLaMA-13B)**  | 28.64%    | 9.81%    | 13.67%  | 70.80%  | 
| **[AVA Llama_3_V2](https://huggingface.co/MehdiHosseiniMoghadam/AVA-Llama-3-V2)**  | 30.07%   | 10.33%    | 16.39%    | 70.87%      |

---
🌐 Model Hosted on Hugging Face
You can access and use this model directly via the Hugging Face Hub:

Link: https://huggingface.co/Moryjj/FineTuned-parsT5-Simplification

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

📧 Email: your-email@example.com


🔗 LinkedIn: Mohammadreza Joneidi Jafari
