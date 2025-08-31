# In-Context Learning Project

This repository contains the notebook and outputs for my MSc dissertation project:  
**“Context Matters: Evaluating the Role of Retrieval in Large Language Models.”**

The project investigates whether providing retrieved passages as context improves the accuracy of Large Language Models (LLMs) in question answering compared to answering from memory alone.

---

## 📂 Repository Contents

- **incontext-3.ipynb**  
  The main Colab notebook that runs the full pipeline:
  1. Load and prepare the SQuAD dataset.
  2. Retrieve top-3 passages per question using BM25 (PyTerrier).
  3. Generate answers from LLMs in two modes:  
     - *No Context* → only the question.  
     - *With Context* → question + retrieved passages.  
  4. Evaluate answers using ROUGE-L and BLEU.

- **Outputs**  
  CSV/JSON files generated during experiments, such as:  
  - `answers_with_context.csv`  
  - `answers_no_context.csv`  
  - `answers_compare.csv`  
  - `metrics_summary.json`  
  - `model_metrics.csv`  

---

## 🚀 How to Run

1. Open the notebook **[incontext-3.ipynb](./incontext-3.ipynb)** in [Google Colab](https://colab.research.google.com/).  
2. Make a copy to your own Google Drive (`File` → `Save a copy in Drive`).  
3. Get a Groq API key:  
   - Sign up at [Groq Console](https://console.groq.com/).  
   - Generate a new API key under your account settings.  
4. In the notebook, add your key at the top like this:  

   ```python
   import os
   os.environ["GROQ_API_KEY"] = "put_your_api_key_here"
