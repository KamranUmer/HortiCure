<div align="center">

# 🌿 HortiCure

**Detect plant leaf diseases from a photo and ask an AI assistant how to treat them.**

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow"> <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white" alt="Keras"> <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit"> <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain"> <img src="https://img.shields.io/badge/Groq%20%C2%B7%20Llama%203-F55036?style=for-the-badge" alt="Groq · Llama 3">

</div>

## 📌 Overview

Upload a photo of a leaf and HortiCure classifies it as **Healthy**, **Powdery mildew** or **Rust** with a convolutional neural network. A built-in chatbot (Llama 3 via Groq) then explains the disease and suggests treatments.

## ✨ Features

- Data augmentation and class-distribution analysis in `plant_disease.ipynb`
- Compares a simple dense network against a CNN; the CNN is exported as `model.h5`
- Streamlit app for image upload and prediction (`main.py`)
- LangChain chatbot with conversation memory (`chat_bot.py`)

## 📊 Results

| Metric | Value |
|---|---|
| Classes | Healthy · Powdery · Rust |
| CNN validation accuracy | 96.7% |

> From `model.evaluate` on the validation split in `plant_disease.ipynb`.

## 🚀 Getting Started

```bash
git clone https://github.com/KamranUmer/HortiCure.git
cd HortiCure
pip install -r requirements.txt
cp .env.example .env      # add GROQ_API_KEY (and GOOGLE_API_KEY if used)
streamlit run main.py
```

## 📁 Project Structure

```
HortiCure/
├── main.py              # Streamlit app
├── chat_bot.py          # Llama 3 treatment assistant
├── plant_disease.ipynb  # training and evaluation
├── model.h5             # trained CNN
└── requirements.txt     # dependencies
```

---

<div align="center">

Built by <a href="https://github.com/KamranUmer"><b>Kamran Umer</b></a> · ⭐ Star the repo if you find it useful

</div>
