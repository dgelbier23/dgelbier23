<div align="center">

<!-- Dynamic header banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Building%20AI%20that%20matters.&fontSize=38&fontColor=ffffff&fontAlignY=38&desc=MSc%20AI%20%E2%80%A2%20Medical%20AI%20%E2%80%A2%203D%20Deep%20Learning%20%E2%80%A2%20Computer%20Vision%20%E2%80%A2%20LLMs&descAlignY=58&descSize=16&descColor=c9b8f5" width="100%" />

</div>

---

## Hey, I'm Dylan 👋

I design and build AI systems with a focus on real-world constraints — not just benchmark performance.

My work focuses on making modern AI systems — particularly 3D, vision and language models — **reliable, measurable and usable in high-stakes domains like healthcare**.

My background sits at the intersection of **machine learning**, **computer vision**, and **healthcare AI**. I've shipped production systems at BMW Group (MINI Oxford), where I worked on everything from robotic vision pipelines to NLP-driven OCR tools. I've since completed an MSc in Artificial Intelligence at Loughborough University, where my dissertation asked a question I think medical AI needs to ask more often: **when a model gives an answer, how do we know we can trust it?**

---

## 🎯 Focus Areas

- **Reliable AI for healthcare:** evaluation beyond a single score (consistency, robustness, failure modes)
- **3D deep learning:** point clouds, meshes and multi-view representations of anatomy (intra-oral scans, dental models)
- **Medical imaging:** classification, localisation and interpretability (Grad-CAM)
- **LLMs for clinical question answering:** parameter-efficient fine-tuning, retrieval and trustworthy evaluation
- **Research to real systems:** reproducible, tested pipelines and real-time perception on embedded hardware

---

## 🔭 What I'm Working On

- **[Reliable 3D Tooth Completion](https://github.com/dgelbier23/dental-3d-vae)** — building on my MSc dissertation: generative models that rebuild incomplete intra-oral scans, evaluated for both accuracy and consistency. Next: making the model robust to how a tooth is oriented, and testing results across multiple training seeds
- **Looking for my next role** — in medical AI research or AI engineering, where careful evaluation matters

---

## 🚀 Featured Projects

### 🦷 Reliable 3D Tooth Completion: Accuracy and Consistency of a β-VAE (MSc Dissertation)

🔗 [Repository](https://github.com/dgelbier23/dental-3d-vae) • 📊 [Results](https://github.com/dgelbier23/dental-3d-vae#results) • 🏷️ [Dissertation version](https://github.com/dgelbier23/dental-3d-vae/tree/v1.0-dissertation)

<p align="center">
  <img src="https://raw.githubusercontent.com/dgelbier23/dental-3d-vae/main/docs/figures/results/completion.gif" width="85%" alt="An upper first molar with 45 percent of it cut away, the model's reconstruction over it, and the reconstruction alone, rotating">
</p>

> Intra-oral 3D scans are often incomplete: the scanner cannot see behind neighbouring teeth, the patient moves, braces get in the way. This project trains a β-variational autoencoder on point clouds of real teeth (Teeth3DS+) to rebuild the missing geometry, and evaluates it on two questions: how *accurately* it completes a tooth, and how *consistently*, since a generative model can produce many plausible completions of the same input, and in clinical use there is no complete tooth to check against.
> The work spans a full pipeline from 300 clinical jaw scans to 4,038 segmented teeth and 32,304 controlled partial teeth, an architecture study, and per-tooth evaluation with four metrics, including region-specific errors and a stochastic consistency error defined in the project. The research code was then rebuilt into a tested Python package that reproduces every reported result exactly.

- **Full 3D pipeline on clinical data** — jaw scans → segmented teeth → normalised 2,048-point clouds → plane-cut and connected-patch partial teeth, seeded and reproducible
- **Architecture study** — 4 point-cloud encoders (PointNet, T-Net PointNet, PointNet++, DGCNN) × 3 decoders (MLP, FoldingNet, AtlasNet) and an 8-value KL-weight ablation; DGCNN + FoldingNet is **14% more accurate than an MLP decoder with 91% fewer parameters**
- **Evaluation beyond one number** — Chamfer distance, missing-region and observed-region errors, and stochastic consistency, broken down per tooth position on a dental chart
- **Key finding** — the model's consistency is only weakly correlated with its accuracy (r ≈ 0.2–0.3): a model agreeing with itself is not evidence that it is right
- **Verified, engineered rewrite** — all 16 trained models reproduce the original outputs; 98 automated tests; CPU-safe local development with GPU training on Colab

**Why it matters**
In clinical use there is no complete tooth to compare a completion against, so a model's reliability has to be measured, not assumed. This project shows that consistency can flag uncertainty but cannot certify accuracy, so trustworthy 3D completion needs both to be reported.

`Python` `PyTorch` `3D Point Clouds` `Generative Models` `β-VAE` `DGCNN` `FoldingNet` `Medical AI` `Dental Imaging` `Reliability` `Reproducibility`

---

### 🫁 Transfer Learning for Lung Disease Classification & Localisation from Chest X-Rays

🔗 [Repository](https://github.com/dgelbier23/lung-disease-classification-localisation) • 📄 [Report](https://github.com/dgelbier23/lung-disease-classification-localisation/blob/main/reports/lung_disease_classification_report.pdf) • 🖼️ [Grad-CAM example](https://github.com/dgelbier23/lung-disease-classification-localisation/blob/main/figures/gradcam/localisation_gradcam_ex.png)

> Deep learning pipeline for multi-class classification and visual localisation of pulmonary disease from chest X-rays (Healthy, Pneumonia, COVID-19). Built around a controlled transfer learning framework using an ImageNet-pretrained Xception backbone, the project prioritises clinically meaningful evaluation (recall, macro-F1) under class imbalance and subtle inter-class overlap.
> The system combines robust preprocessing, weighted optimisation, and Grad-CAM interpretability to produce both predictions and spatial insight into model decision-making.

- Transfer learning with **Xception backbone + lightweight classification head**, balancing representational power with overfitting control
- Structured experimentation across **learning rate, optimiser choice, and layer unfreezing strategies**, ensuring causal performance attribution
- **Class imbalance handled via weighted loss**, avoiding synthetic data risks in sensitive medical domains
- Evaluation beyond accuracy: **macro F1 (~0.99), per-class recall, precision-recall curves, calibration analysis, confusion matrix**
- Integrated **Grad-CAM visualisation** for localisation, highlighting clinically relevant lung regions influencing predictions
- Dataset: ~15k chest X-ray images, **stratified 70/15/15 split**, minimal augmentation to preserve diagnostic fidelity

**Why it matters**
Reliable automated screening tools must prioritise **missed diagnosis risk (false negatives)** over raw accuracy. This project reflects real clinical constraints—imbalanced data, ambiguous imaging, and the need for interpretability—while demonstrating how careful transfer learning design can produce robust, explainable models.

`Python` `TensorFlow` `Keras` `Deep Learning` `Computer Vision` `Medical Imaging` `Transfer Learning` `Xception` `Grad-CAM` `Model Evaluation`

---

### 🦷🧠 Adapting AlexNet for 3D Object Classification, Using a View-Based Approach for Orthodontics Classification

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

### 🏥 Optimising Large Language Models for Medical Question Answering & Clinical Decision Support

📦 *Repository coming soon*

> A research-driven exploration into adapting and optimising large language models (LLMs) for medical question answering and clinical decision support. The project investigates how LLMs can be enhanced to provide accurate, reliable, and context-aware responses within healthcare settings.
> The system explores multiple adaptation strategies, including parameter-efficient fine-tuning, prompt engineering, and retrieval-based augmentation, aiming to improve domain-specific performance without relying on full-scale retraining.
> A key focus is placed on evaluation beyond standard benchmarks, introducing more rigorous and clinically relevant assessment methods to better capture model reliability, reasoning quality, and real-world applicability.

- **LLM adaptation strategies** — Explores fine-tuning, prompt engineering, and retrieval-augmented approaches for domain-specific performance
- **Comparative optimisation study** — Systematic evaluation of multiple techniques to identify effective configurations for medical QA
- **Advanced evaluation framework** — Moves beyond standard benchmarks to assess reasoning quality, consistency, and clinical relevance
- **Trust and reliability focus** — Emphasises robustness, hallucination mitigation, and safe deployment considerations in healthcare

**Why it matters**
Applying large language models in healthcare requires more than raw performance — it demands reliability, interpretability, and domain alignment. This project explores how optimisation and evaluation design affect the usefulness of LLMs in clinical contexts.

`Python` `PyTorch` `Transformers` `LLMs` `Medical AI` `NLP` `Prompt Engineering` `PEFT`

---

## ✍️ Writing

- **[Synthetic Data in Medical Image Analysis: A Critical Evaluation](https://github.com/dgelbier23/medical-ai-writing/tree/main/synthetic-data-medical-imaging)**
  → A map of how synthetic data is generated, integrated and evaluated in medical imaging, and a critique of two influential studies (Gao et al., 2023; Al Khalil et al., 2023)

  → Argues that performance gains alone cannot establish clinical validity: the same principle behind my [3D tooth completion work](https://github.com/dgelbier23/dental-3d-vae), which measures consistency alongside accuracy

  → 📄 [Download as PDF](https://github.com/dgelbier23/medical-ai-writing/blob/main/synthetic-data-medical-imaging/Synthetic_Data_in_Medical_Image_Analysis.pdf) • 📊 [Summary slides](https://github.com/dgelbier23/medical-ai-writing/blob/main/synthetic-data-medical-imaging/Synthetic_Data_in_Medical_Image_Analysis_Summary_Slides.pdf)

📚 [All articles](https://github.com/dgelbier23/medical-ai-writing)

---

## 📄 Publications

- **Artificial Intelligence and the Research and Reporting of Dental History**
  → Explores the application of AI in analysing and structuring historical dental research data

  → [Google Scholar](https://scholar.google.com/citations?user=K_mGkm8AAAAJ)

---

## 🎓 Background

- **MSc Artificial Intelligence** — *Loughborough University* (2026) — dissertation: [Reliable 3D Tooth Completion](https://github.com/dgelbier23/dental-3d-vae)
- **BSc Artificial Intelligence and Computer Science** — *Loughborough University* — **1st**
- **AI/ML Engineer** — BMW Group (MINI Oxford Plant)

---

## 🛠 Technical Stack

**ML & AI**

![PyTorch](https://img.shields.io/badge/PyTorch-14161A?style=flat-square&logo=pytorch&logoColor=EE4C2C)
![TensorFlow](https://img.shields.io/badge/TensorFlow-14161A?style=flat-square&logo=tensorflow&logoColor=FF6F00)
![HuggingFace](https://img.shields.io/badge/HuggingFace-14161A?style=flat-square&logo=huggingface&logoColor=FFD21E)
![scikit--learn](https://img.shields.io/badge/scikit--learn-14161A?style=flat-square&logo=scikit-learn&logoColor=F7931E)
![OpenCV](https://img.shields.io/badge/OpenCV-14161A?style=flat-square&logo=opencv&logoColor=5C3EE8)
![LangChain](https://img.shields.io/badge/LangChain-14161A?style=flat-square&logo=langchain&logoColor=white)

**Languages**

![Python](https://img.shields.io/badge/Python-14161A?style=flat-square&logo=python&logoColor=3776AB)
![SQL](https://img.shields.io/badge/SQL-14161A?style=flat-square&logo=postgresql&logoColor=4169E1)
![Java](https://img.shields.io/badge/Java-14161A?style=flat-square&logo=openjdk&logoColor=ED8B00)
![JavaScript](https://img.shields.io/badge/JavaScript-14161A?style=flat-square&logo=javascript&logoColor=F7DF1E)
![HTML](https://img.shields.io/badge/HTML-14161A?style=flat-square&logo=html5&logoColor=E34F26)
![CSS](https://img.shields.io/badge/CSS-14161A?style=flat-square&logo=css&logoColor=663399)

**Deployment & Tooling**

![Docker](https://img.shields.io/badge/Docker-14161A?style=flat-square&logo=docker&logoColor=2496ED)
![FastAPI](https://img.shields.io/badge/FastAPI-14161A?style=flat-square&logo=fastapi&logoColor=009688)
![Streamlit](https://img.shields.io/badge/Streamlit-14161A?style=flat-square&logo=streamlit&logoColor=FF4B4B)
![pytest](https://img.shields.io/badge/pytest-14161A?style=flat-square&logo=pytest&logoColor=0A9EDC)
![Google Colab](https://img.shields.io/badge/Colab-14161A?style=flat-square&logo=googlecolab&logoColor=F9AB00)
![Git](https://img.shields.io/badge/Git-14161A?style=flat-square&logo=git&logoColor=F05032)

**Domains**

| Area | Experience |
|---|---|
| Medical AI | 3D tooth completion, chest X-ray classification & localisation, clinical question answering |
| 3D Deep Learning | Point clouds (PointNet, DGCNN), generative models (β-VAE), multi-view CNNs |
| Computer Vision | Object detection, tracking, segmentation, OCR, stereo vision |
| NLP | Transformers, RAG, document understanding, chatbots |
| Time Series | Forecasting, anomaly detection, sensor data |
| MLOps | Model serving, monitoring, fine-tuning workflows |

---

## 🧩 How I Approach Problems

- Start from the real-world constraint, not the model
- Prefer simple, robust systems over complex, fragile ones
- Treat evaluation as seriously as modelling: a single score is not evidence of reliability

---

## 📬 Let's Connect

I'm looking for **medical AI research and AI engineering roles**, and I'm always open to research collaborations and interesting problems in healthcare AI.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/dylangelbier)
[![Google Scholar](https://img.shields.io/badge/Scholar-4285F4?style=flat-square&logo=googlescholar&logoColor=white)](https://scholar.google.com/citations?user=K_mGkm8AAAAJ)

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=100&section=footer" width="100%" />

</div>
