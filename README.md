<div align="center">

<!-- Dynamic header banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Building%20AI%20that%20matters.&fontSize=38&fontColor=ffffff&fontAlignY=38&desc=MSc%20AI%20%E2%80%A2%20Computer%20Vision%20%E2%80%A2%20Medical%20AI%20%E2%80%A2%20LLMs&descAlignY=58&descSize=16&descColor=c9b8f5" width="100%" />

</div>

---

## Hey, I'm Dylan 👋

I design and build AI systems with a focus on real-world constraints — not just benchmark performance.

My work focuses on making modern AI systems — particularly LLMs and vision models — **reliable, efficient, and usable in high-stakes domains like healthcare**.

My background sits at the intersection of **machine learning**, **computer vision**, and **healthcare AI**. I've shipped production systems at BMW Group (MINI Oxford), where I worked on everything from robotic vision pipelines to NLP-driven OCR tools. Now I'm focused on where I think the most important problems are: **medical AI** and **LLM-powered clinical tools**.

I care about systems that are reliable, explainable, and actually deployed — not just impressive in a notebook.

---

## 🔭 What I'm Working On

- **3D Medical Image Analysis** — segmentation and classification on volumetric data (CT/MRI)
- **Clinical RAG Systems** — LLM pipelines grounded in medical literature for safer, more accurate outputs
- **Model Optimisation** — quantisation, fine-tuning, and efficient inference for resource-constrained environments
- **Multimodal AI** — combining vision and language for richer medical understanding

---
## 🎯 Selected Focus Areas

- Reliable AI systems in high-stakes environments  
- Efficient adaptation of large models (LLMs, multimodal systems)  
- Bridging research prototypes → usable systems  
- Evaluation beyond benchmarks (robustness, failure modes, bias)  

---
## 🛠 Technical Stack

**Core Languages**

![Python](https://img.shields.io/badge/Python-14161A?style=flat-square&logo=python&logoColor=3776AB)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://shields.io/badge/JavaScript-F7DF1E?logo=JavaScript&logoColor=000&style=flat-square)
![HTML](https://shields.io/badge/HTML-f06529?logo=html5&logoColor=white&labelColor=f06529)
![CSS](https://img.shields.io/badge/CSS-gray?style=flat-square&logo=CSS&logoSize=auto)
![SQL](https://img.shields.io/badge/SQL-14161A?style=flat-square&logo=postgresql&logoColor=4169E1)

**ML & AI**

![PyTorch](https://img.shields.io/badge/PyTorch-14161A?style=flat-square&logo=pytorch&logoColor=EE4C2C)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=TensorFlow&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-14161A?style=flat-square&logo=huggingface&logoColor=FFD21E)
![scikit--learn](https://img.shields.io/badge/scikit--learn-14161A?style=flat-square&logo=scikit-learn&logoColor=F7931E)
![OpenCV](https://img.shields.io/badge/OpenCV-14161A?style=flat-square&logo=opencv&logoColor=5C3EE8)
![LangChain](https://img.shields.io/badge/LangChain-14161A?style=flat-square&logo=langchain&logoColor=white)

**Deployment & Tooling**

![Streamlit](https://img.shields.io/badge/Streamlit-14161A?style=flat-square&logo=streamlit&logoColor=FF4B4B)
![Docker](https://img.shields.io/badge/Docker-14161A?style=flat-square&logo=docker&logoColor=2496ED)
![FastAPI](https://img.shields.io/badge/FastAPI-14161A?style=flat-square&logo=fastapi&logoColor=009688)
![Git](https://img.shields.io/badge/Git-14161A?style=flat-square&logo=git&logoColor=F05032)

**Domains**

| Area | Experience |
|---|---|
| Computer Vision | Object detection, segmentation, OCR, stereo vision |
| NLP | Transformers, RAG, document understanding, chatbots |
| Time Series | Forecasting, anomaly detection, sensor data |
| Medical AI | 3D segmentation, clinical NLP, imaging pipelines |
| MLOps | Model serving, monitoring, fine-tuning workflows |

---

## 🚀 Featured Projects

### 🫁 Transfer Learning for Lung Disease Classification & Localisation from Chest X-Rays  
🔗 [Repository](https://github.com/dgelbier23/lung-disease-classification-localisation.git) • 📄 [Report](https://github.com/dgelbier23/lung-disease-classification-localisation/reports/lung_disease_classification_report.pdf) • 🎥 [Demo](https://github.com/dgelbier23/lung-disease-classification-localisation/figures/gradcam/localisation_gradcam_ex.png)

> Deep learning pipeline for multi-class classification and visual localisation of pulmonary disease from chest X-rays (Healthy, Pneumonia, COVID-19). Built around a controlled transfer learning framework using an ImageNet-pretrained Xception backbone, the project prioritises clinically meaningful evaluation (recall, macro-F1) under class imbalance and subtle inter-class overlap.  
> The system combines robust preprocessing, weighted optimisation, and Grad-CAM interpretability to produce both predictions and spatial insight into model decision-making.

- Transfer learning with **Xception backbone + lightweight classification head**, balancing representational power with overfitting control  
- Structured experimentation across **learning rate, optimiser choice, and layer unfreezing strategies**, ensuring causal performance attribution  
- **Class imbalance handled via weighted loss**, avoiding synthetic data risks in sensitive medical domains  
- Evaluation beyond accuracy: **macro F1 (~0.99), per-class recall, precision-recall curves, calibration analysis, confusion matrix**  
- Integrated **Grad-CAM visualisation** for localisation, highlighting clinically relevant lung regions influencing predictions  
- Dataset: ~15k chest X-ray images, **stratified 70/15/15 split**, minimal augmentation to preserve diagnostic fidelity  

**Why it matters:**  
Reliable automated screening tools must prioritise **missed diagnosis risk (false negatives)** over raw accuracy. This project reflects real clinical constraints—imbalanced data, ambiguous imaging, and the need for interpretability—while demonstrating how careful transfer learning design can produce robust, explainable models.

`Python` `TensorFlow` `Keras` `Deep Learning` `Computer Vision` `Medical Imaging` `Transfer Learning` `Xception` `Grad-CAM` `Model Evaluation`

---

### 🏥 MedRAG — Clinical Question Answering with RAG
> LLM-powered system that answers clinical questions grounded in indexed medical literature. Combines dense retrieval with a fine-tuned reader model to reduce hallucination in high-stakes contexts.
`PyTorch` `LangChain` `HuggingFace` `FAISS` `Streamlit`

---

### 🧠 3D Medical Segmentation Pipeline
> End-to-end pipeline for volumetric organ segmentation on CT/MRI data. Includes preprocessing, training with nnU-Net variants, and a lightweight inference API.
`PyTorch` `MONAI` `SimpleITK` `FastAPI` `Docker`

---

### 🤖 Vision-Guided Error Detection System *(BMW Group)*
> Computer vision system developed for a robotics assembly environment at MINI Oxford, focused on real-time defect detection under production constraints.
`OpenCV` `PyTorch` `ONNX` `C++`

---

### 📈 Time Series Forecasting for Manufacturing Operations
> Multivariate forecasting system for predicting production bottlenecks and maintenance windows. Evaluated LSTM, Temporal Fusion Transformers, and classical baselines.
`PyTorch` `Prophet` `scikit-learn` `Pandas`

---

### 📄 OCR + NLP Document Processing Pipeline
> Automated extraction and structuring of information from scanned engineering and compliance documents. Combined Tesseract OCR with custom NLP post-processing to achieve high accuracy on domain-specific formats.
`Tesseract` `spaCy` `HuggingFace` `Python`

---

## 📊 GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=dgelbier23&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" />
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=dgelbier23&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />

</div>

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=dgelbier23&theme=tokyo-night&hide_border=true&area=true" width="95%" />

</div>

---

## 🎓 Background

- **MSc Artificial Intelligence** — *Loughborough University*
- **BSc Artificial Intelligence and Computer Science** — *Loughborough University* — **1st**
- **AI/ML Engineer** — BMW Group (MINI Oxford Plant)

---

## 📄 Publications

- **Artificial Intelligence and the Research and Reporting of Dental History**
  → Explores the application of AI in analysing and structuring historical dental research data
  
  → https://scholar.google.com/citations?user=K_mGkm8AAAAJ

---

## 🧩 How I Approach Problems

- Start from the real-world constraint, not the model  
- Prefer simple, robust systems over complex, fragile ones  
- Treat evaluation as seriously as modelling

---

## 📬 Let's Connect

I'm open to research collaborations, interesting problems in medical AI, and roles where the work actually ships.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/dylangelbier)
[![Google Scholar](https://img.shields.io/badge/Scholar-4285F4?style=flat-square&logo=googlescholar&logoColor=white)](https://scholar.google.com/citations?view_op=list_works&hl=en&authuser=2&hl=en&user=K_mGkm8AAAAJ&authuser=2)

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=100&section=footer" width="100%" />

</div>
