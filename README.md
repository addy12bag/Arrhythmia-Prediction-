# ❤️ ArrhythmiaScan AI
### Hybrid ML–DL Pipeline for Precision Cardiac Arrhythmia Detection

ArrhythmiaScan AI is a high-performance diagnostic pipeline that detects cardiac arrhythmias from ECG signals using the MIT-BIH dataset. By combining expert-driven feature engineering with automated deep learning feature extraction, it offers a robust and comparative framework for cardiovascular health assessment.

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Python 3.10+](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter&logoColor=white)

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Technology Stack](#-technology-stack)
- [Project Pipeline](#-project-pipeline)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Machine Learning Models](#-machine-learning-models)
- [Key Insights](#-key-insights)
- [Roadmap](#-roadmap)
- [Author](#-author)
- [License](#-license)

---

## 🎯 Overview

ArrhythmiaScan AI addresses the critical need for automated and accurate ECG interpretation. Cardiac arrhythmias — irregular heart rhythms — can lead to severe complications if left undetected. This project automates the detection process by bridging traditional signal processing with modern deep learning.

**The Challenge**

Manual ECG interpretation by clinicians is time-consuming and prone to error, particularly during long-term monitoring.

**Our Solution**

ArrhythmiaScan AI implements a dual-stream architecture:

- **Feature-Engineered ML** — leverages statistical and temporal characteristics for high precision.
- **Deep 1D-CNN** — processes raw signal data for automated hierarchical feature extraction.
- **Comparative Analysis** — provides a rigorous benchmark between traditional ML and modern DL approaches.

---

## ✨ Features

### 🔬 Signal Processing & Preprocessing
- **Noise Filtering** — advanced techniques to remove artifacts from raw ECG signals.
- **Beat Segmentation** — precise extraction of individual heartbeats for focused analysis.
- **Normalization** — standardizes signals across patient records for model stability.

### 🧠 Hybrid Modeling
- **Machine Learning** — expert-driven feature engineering using statistical and temporal descriptors.
- **Deep Learning** — 1D Convolutional Neural Network (CNN) for end-to-end raw signal processing.
- **High Accuracy** — 97% accuracy with ML and 93% with the deep learning stream.

### 📊 Evaluation & Visualization
- **Comprehensive Metrics** — accuracy, precision, recall, and F1-score across all classes.
- **Wavelet Analysis** — signal decomposition for temporal-frequency insights.
- **Comparative Benchmarking** — direct performance comparison between ML and DL streams.

---

## 🛠️ Technology Stack

| Layer              | Technology                          |
|--------------------|-------------------------------------|
| Core Language      | Python 3.10+                        |
| Deep Learning      | PyTorch                             |
| Machine Learning   | Scikit-learn, NumPy, Pandas         |
| Signal Processing  | SciPy, Wavelet Transforms           |
| Visualization      | Matplotlib, Seaborn                 |
| Environment        | Jupyter Notebooks                   |

---

## 🏗️ Project Pipeline

**Data Source:** MIT-BIH Arrhythmia Dataset (PhysioNet)

```
┌─────────────────┐
│  ECG Raw Input  │  MIT-BIH Signal Records
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Preprocessing  │  Noise Filtering & Beat Segmentation
└────────┬────────┘
         │
    ┌────┴────┐
    ▼         ▼
┌─────────┐ ┌───────────┐
│ ML Path │ │  DL Path  │
│(Feature)│ │ (1D-CNN)  │
└────┬────┘ └─────┬─────┘
     │             │
     └──────┬──────┘
            ▼
┌─────────────────────────────────┐
│           Evaluation            │
│  ML Accuracy: 97% | CNN: 93%    │
└─────────────────────────────────┘
```

---

## 📁 Project Structure

```
ArrhythmiaScanAI/
├── code.ipynb                     # Core end-to-end pipeline
├── model_cnn.ipynb                # Deep Learning (1D-CNN) implementation
├── model_mlbased.ipynb            # Feature-based Machine Learning workflow
├── testing.ipynb                  # Model evaluation & metrics
├── wavelate.ipynb                 # Wavelet signal processing experiments
├── best_ecg_1dcnn_balanced.pth    # Pre-trained CNN weights
└── README.md                      # Documentation
```

---

## 🚀 Installation

**Prerequisites**
- Python 3.10 or higher
- pip package manager

**Step 1 — Clone the Repository**

```bash
git clone https://github.com/addy12bag/Arrhythmia-Prediction-.git
cd Arrhythmia-Prediction-
```

**Step 2 — Set Up the Environment**

```bash
# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: .\venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## 💻 Usage

1. **Launch Jupyter:**
   ```bash
   jupyter notebook
   ```

2. **Run the Full Pipeline:** Open `code.ipynb` to execute preprocessing and modeling end-to-end.

3. **Explore Individual Models:** Open `model_cnn.ipynb` or `model_mlbased.ipynb` for architecture-specific details.

---

## 🧠 Machine Learning Models

### Traditional ML Stream
- **Features:** 18+ statistical and temporal descriptors per beat.
- **Accuracy:** 97%
- **Verdict:** Superior performance due to highly targeted feature engineering on the MIT-BIH dataset.

### Deep Learning Stream
- **Architecture:** 1D Convolutional Neural Network (1D-CNN)
- **Input:** Raw segmented ECG waveform
- **Accuracy:** 93%
- **Verdict:** Strong scalability potential — eliminates manual feature engineering, making it well-suited for larger, more diverse datasets.

---

## 📊 Key Insights

1. **Expert Knowledge Wins (for now)** — on focused datasets like MIT-BIH, handcrafted features outperform raw signal learning. Domain expertise still matters.

2. **CNNs Scale Better** — while slightly less accurate here, 1D-CNNs generalize more readily to large, heterogeneous healthcare data without manual feature design.

3. **Preprocessing is Everything** — proper noise filtering is the single most critical step in achieving high diagnostic accuracy across both streams.

---

## 🗺️ Roadmap

- [ ] **Real-time Monitoring** — integrate with live ECG sensor feeds.
- [ ] **Explainable AI (XAI)** — implement SHAP/Grad-CAM to highlight arrhythmia triggers in signals.
- [ ] **Web Dashboard** — build a React-based interface for clinician-facing visualization.
- [ ] **Multi-Dataset Training** — expand to PTB-XL and other global ECG databases.

---

## 👤 Author

**Sayantan Bag**
M.Tech (Robotics) — Specializing in AI, Machine Learning, and Intelligent Systems

- 📧 Email: [sayantan.bag@example.com](mailto:sayantan.bag@example.com)
- 💼 GitHub: [@addy12bag](https://github.com/addy12bag)

---

## 📄 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
Copyright © 2026 Sayantan Bag.

---

<div align="center">
  Developed with ❤️ for Intelligent Healthcare
</div>
