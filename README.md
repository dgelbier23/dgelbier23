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
🔗 [Repository](https://github.com/dgelbier23/lung-disease-classification-localisation.git) • 📄 [Report](https://github.com/dgelbier23/lung-disease-classification-localisation/blob/main/reports/lung_disease_classification_report.pdf) • 🎥 [Demo](https://github.com/dgelbier23/lung-disease-classification-localisation/blob/main/figures/gradcam/localisation_gradcam_ex.png)

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

### 🤖 Perception-Driven Human Following Robot

🔗 [Repository](https://github.com/dgelbier23/perception-driven-human-following-robot) • 📄 [Report](https://github.com/dgelbier23/perception-driven-human-following-robot/blob/main/reports/perception-driven-human-following-robot_report.pdf) • 🎥 [Demo](https://github.com/dgelbier23/perception-driven-human-following-robot/blob/main/docs/demo-gif.gif)

> A real-time, closed-loop human-following system built on embedded hardware, integrating YOLO-based detection, DeepSORT tracking, and RGB-D depth estimation. The system enforces a strict safety constraint: no verified perception signal results in no motor output.
> Detections are passed into a Kalman-filter-based tracker with ReID embeddings to maintain identity through occlusions. The system prioritises the oldest confirmed track to prevent ID switching in multi-person environments.
> Depth estimation is performed via sparse RGB-D sampling within the target bounding box, with statistical outlier rejection. This produces stable lateral offset (X) and distance (Z) estimates, which feed into a PID controller with angular correction derived from `arctan(X/Z)`.
> The architecture evolved from a detection-only baseline that failed under crowding and occlusion. The final design separates perception and control, with strict inter-stage validation and fail-safe gating to ensure predictable degradation and safe operation.

- **YOLO + DeepSORT pipeline** — Real-time person detection with Kalman prediction and ReID-based identity tracking  
- **Occlusion robustness** — Oldest-track selection and motion prediction maintain stable identity without ID switching  
- **RGB-D depth estimation** — Sparse sampling with outlier rejection for reliable (X, Z) spatial estimation  
- **PID control system** — Independent distance and angular control loops with deadband and smoothing for stability  
- **Embedded deployment** — Optimised for real-time inference on Jetson/ARM hardware under strict latency constraints  
- **Systematic evaluation** — Tested across multi-person scenes, occlusion events, and sensor noise; evaluated using ID switches, tracking stability, and RMS error  

**Why it matters**  
Robust human-following in real-world conditions requires more than accurate models — it demands careful system design across perception, tracking, and control. This project demonstrates how architectural decisions and failure handling enable reliable behaviour in crowded, dynamic environments.

`Python` `PyTorch` `Computer Vision` `Robotics` `YOLO` `DeepSORT` `RGB-D` `PID Control` `Embedded AI`

---

### 🧠 Adapting AlexNet for 3D Object Classification, Using a View-Based Approach for Orthodontics Classification

🔗 [Repository](https://github.com/dgelbier23/multi-view-3d-dataset-cnn) • 📄 [Notebook](https://github.com/dgelbier23/multi-view-3d-dataset-cnn/blob/main/notebooks/main_notebook.ipynb) • 🌐 [HTML View](https://github.com/dgelbier23/multi-view-3d-dataset-cnn/blob/main/notebooks/main_notebook.html)

> An end-to-end deep learning pipeline for 3D object classification, transforming raw 3D models into a structured multi-view dataset and training a CNN to distinguish between upper and lower jaw structures.
> The system begins with a preprocessing stage that converts 3D `.obj` files into multiple 2D projections captured from different viewpoints, forming a multi-view representation that preserves spatial information while enabling efficient learning.
> These views are aggregated into structured tensors and passed through a convolutional neural network adapted to process non-standard inputs, learning features across perspectives rather than single images.
> The project emphasises pipeline design under real-world constraints, demonstrating how data representation, model architecture, and training strategy interact to produce a robust classification system without relying on bundled datasets.

- **3D → multi-view dataset generation** — Converts 3D objects into structured 2D projections for CNN compatibility  
- **Multi-view representation learning** — Captures spatial features across perspectives rather than single-image inputs  
- **CNN-based classification** — Adapted architecture processes multi-view tensors for anatomical classification  
- **End-to-end pipeline design** — Integrates data generation, preprocessing, and training into a unified workflow  
- **Reproducible notebook implementation** — Fully contained `.ipynb` with HTML export for accessible review  
- **Constraint-aware engineering** — Designed without bundled datasets, focusing on methodology and adaptability  

**Why it matters**  
3D data is inherently complex and difficult to process efficiently. This project demonstrates how transforming 3D structures into multi-view representations enables the use of standard deep learning techniques while preserving spatial information. By integrating dataset generation with model training, it highlights the importance of representation design and pipeline architecture in building effective AI systems under practical constraints.

`Python` `PyTorch` `3D Data` `Computer Vision` `Deep Learning` `Multi-View Learning` `Medical AI`

---
### 🏥 Optimising Large Language Models for Medical Question Answering & Clinical Decision Support
[PROJECT NOT YET PUT ON GITHUB]
🔗 [Repository](#) • 📄 [Dissertation](#) • 📊 [Evaluation](#)

> A research-driven exploration into adapting and optimising large language models (LLMs) for medical question answering and clinical decision support. The project investigates how LLMs can be enhanced to provide accurate, reliable, and context-aware responses within healthcare settings.
> The system explores multiple adaptation strategies, including parameter-efficient fine-tuning, prompt engineering, and retrieval-based augmentation, aiming to improve domain-specific performance without relying on full-scale retraining.
> A key focus is placed on evaluation beyond standard benchmarks, introducing more rigorous and clinically relevant assessment methods to better capture model reliability, reasoning quality, and real-world applicability.
> The work takes a comparative approach to optimisation, analysing how different techniques impact performance, generalisation, and trustworthiness in medical contexts.

- **LLM adaptation strategies** — Explores fine-tuning, prompt engineering, and retrieval-augmented approaches for domain-specific performance  
- **Comparative optimisation study** — Systematic evaluation of multiple techniques to identify effective configurations for medical QA  
- **Advanced evaluation framework** — Moves beyond standard benchmarks to assess reasoning quality, consistency, and clinical relevance  
- **Medical question answering system** — Designed to support knowledge retrieval and assist clinical decision-making processes  
- **Trust and reliability focus** — Emphasises robustness, hallucination mitigation, and safe deployment considerations in healthcare  
- **Research-oriented implementation** — Combines experimental design, analysis, and engineering within a structured dissertation project  

**Why it matters**  
Applying large language models in healthcare requires more than raw performance — it demands reliability, interpretability, and domain alignment. This project demonstrates how careful optimisation and evaluation design can significantly improve the usefulness of LLMs in clinical contexts, contributing to safer and more effective AI-assisted decision support systems.

`Python` `PyTorch` `Transformers` `LLMs` `Medical AI` `NLP` `Prompt Engineering` `PEFT`

---

### 🧠 3D Medical Segmentation Pipeline
> End-to-end pipeline for volumetric organ segmentation on CT/MRI data. Includes preprocessing, training with nnU-Net variants, and a lightweight inference API.
`PyTorch` `MONAI` `SimpleITK` `FastAPI` `Docker`

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
