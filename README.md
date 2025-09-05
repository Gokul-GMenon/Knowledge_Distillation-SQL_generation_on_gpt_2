# 🧠 Natural Language to SQL using Knowledge Distillation  

This project explores how **Knowledge Distillation (KD)** can be applied to the **Text-to-SQL** problem — enabling anyone to query a database using natural language, without needing advanced SQL knowledge or heavy reliance on large models.  

---

## 🚀 Problem Statement  
- Non-technical users struggle to query organizational databases.  
- Traditional solutions depend on **large LLMs** → costly 💰 and raise data privacy risks 🔒.  
- The goal: make database querying **lightweight, affordable, and private**.  

---

## 🔑 What is Knowledge Distillation (KD)?  
**Knowledge Distillation** is a technique where a **large model (teacher)** trains a **smaller model (student)**.  
The student learns to:  
- Mimic the teacher’s outputs (predictions).  
- Learn internal representations (via hidden states).  

👉 Result: A small, fast model that performs well without the heavy resource requirements.  

---

## 🛠️ My Approach  

- **Teacher Model** 🧑‍🏫: [Qwen2-7B](https://huggingface.co/Qwen) (run on Colab due to resource limits).  
- **Student Model** 🎓: [GPT-2](https://huggingface.co/openai-community/gpt2) (lightweight).  
- **Dataset**: Custom schema with paired **natural language queries ↔ SQL queries**.  

### ⚙️ Training Setup  
- Teacher predicts SQL given natural language queries + schema.  
- Student trained with **dual loss**:  
  - 🟢 Cross-Entropy (generate correct SQL) – 75%  
  - 🔵 MSE (imitate teacher’s hidden states) – 25%  
- **Training**: 20 epochs on Google Colab GPU.  

---

## ✅ Benefits of This Approach  
- 💡 **Democratizes data access** → anyone can query databases in plain English.  
- 💸 **Cost-efficient** → runs locally without huge infra bills.  
- 🔐 **Privacy-friendly** → avoids dependence on cloud-only LLM APIs.  
- ⚡ **Lightweight** → GPT-2 can serve as a practical **on-prem solution**.  

---

## 📊 Visuals  

### 1. Database Schema  
<img width="3719" height="3840" alt="db_schema_mermaid" src="https://github.com/user-attachments/assets/1536c725-9343-4df7-b486-ae74d1b0431b" />


### 2. Knowledge Distillation Architecture  
<img width="2729" height="3840" alt="mermaid_architecture_diagram" src="https://github.com/user-attachments/assets/17596f1f-00a2-4fca-b562-bdeebddea7df" />


### 3. Sample Outputs (Natural Language → SQL)  
<img width="1315" height="551" alt="outputsKD" src="https://github.com/user-attachments/assets/a24b5a6a-d964-4db0-863c-f5e25e74d3aa" />
  

---

## 🏁 Conclusion  
This project shows how **large-to-small model distillation** can power practical **Text-to-SQL systems** — helping organizations scale **data accessibility** without the cost and privacy concerns of massive LLMs.  

Would love feedback, contributions, or ideas on how to extend this further 🚀  

---

## 🔖 Tags  
`#KnowledgeDistillation` `#TextToSQL` `#LLM` `#MachineLearning` `#NLP` `#DataScience` `#AIApplications`  
