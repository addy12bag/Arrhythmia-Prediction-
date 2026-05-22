# ❤️ ArrhythmiaScan AI

  Hybrid ML–DL Pipeline for Precision Cardiac Arrhythmia Detection

  ArrhythmiaScan AI is a high-performance diagnostic pipeline designed to detect cardiac arrhythmias from ECG signals using the MIT-BIH dataset. By combining expert-driven feature
  engineering with automated deep learning feature extraction, the system provides a robust and comparative framework for cardiovascular health assessment.

  ![License: MIT (https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
  ![Python 3.10+ (https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)](https://www.python.org/)
  ![PyTorch (https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)](https://pytorch.org/)
  ![Scikit-Learn (https://img.shields.io/badge/Scikit--Learn-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
  ![Jupyter (https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter&logoColor=white)](https://jupyter.org/)

  Features (#-features) • Approach (#-approach) • Insights (#-key-insights) • Installation (#-installation) • Contact (#-contact)

  ---

  📋 Table of Contents

   - Overview (#-overview)
   - Features (#-features)
   - Technology Stack (#-technology-stack)
   - Project Pipeline (#-project-pipeline)
   - Project Structure (#-project-structure)
   - Installation (#-installation)
   - Usage (#-usage)
   - Machine Learning Models (#-machine-learning-models)
   - Key Insights (#-key-insights)
   - Roadmap (#-roadmap)
   - Author (#-author)
   - License (#-license)

  ---

  🎯 Overview

  ArrhythmiaScan AI addresses the critical need for automated and accurate ECG interpretation. Cardiac arrhythmias are irregular heart rhythms that can lead to severe complications if
  undetected. This project automates the detection process by bridging traditional signal processing with modern deep learning.

  The Challenge
  Manual interpretation of ECG signals by clinicians is time-consuming and susceptible to human error, especially during long-term monitoring. 

  Our Solution
  ArrhythmiaScan AI implements a dual-stream architecture:
   - Feature-Engineered ML: Leverages statistical and temporal characteristics for high precision.
   - Deep 1D-CNN: Utilizes raw signal data for automated hierarchical feature extraction.
   - Comparative Analysis: Provides a rigorous benchmark between traditional ML and modern DL approaches.

  ---

  ✨ Features

  🔬 Signal Processing & Preprocessing
   - Noise Filtering: Advanced techniques to remove artifacts from raw ECG signals.
   - Beat Segmentation: Precise extraction of individual heartbeats for focused analysis.
   - Normalization: Standardizing signals across different patient records for model stability.

  🧠 Hybrid Modeling
   - Machine Learning: Expert-driven feature engineering (Statistical & Temporal).
   - Deep Learning: 1D Convolutional Neural Network (CNN) for raw signal processing.
   - High Accuracy: Achieved 97% accuracy with ML and 93% with Deep Learning.

  📊 Evaluation & Visualization
   - Comprehensive Metrics: Accuracy, Precision, Recall, and F1-score evaluation.
   - Wavelet Analysis: Signal decomposition for deeper temporal-frequency insights.
   - Comparative Benchmarking: Direct performance comparison between ML and DL streams.

  ---

  🛠️ Technology Stack

  ┌───────────────────┬─────────────────────────────┐
  │ Layer             │ Technology                  │
  ├───────────────────┼─────────────────────────────┤
  │ Core Language     │ Python 3.10+                │
  │ Deep Learning     │ PyTorch                     │
  │ Machine Learning  │ Scikit-learn, NumPy, Pandas │
  │ Signal Processing │ Scipy, Wavelet Transforms   │
  │ Visualization     │ Matplotlib, Seaborn         │
  │ Environment       │ Jupyter Notebooks           │
  └───────────────────┴─────────────────────────────┘
  ---

  🏗️ Project Pipeline

  Data Source
   - MIT-BIH Arrhythmia Dataset: The gold standard database from PhysioNet.

  Workflow

    1 ┌─────────────────┐
    2 │ ECG Raw Input   │  MIT-BIH Signal Records
    3 └────────┬────────┘
    4          │
    5          ▼
    6 ┌─────────────────┐
    7 │ Preprocessing   │  Noise Filtering & Segmentation
    8 └────────┬────────┘
    9          │
   10     ┌────┴────┐
   11     ▼         ▼
   12 ┌─────────┐ ┌───────────┐
   13 │ ML Path │ │ DL Path   │
   14 │(Feature)│ │ (1D-CNN)  │
   15 └────┬────┘ └─────┬─────┘
   16      │            │
   17      └─────┬──────┘
   18            ▼
   19 ┌─────────────────┐
   20 │ Evaluation      │  Accuracy: ML (97%) vs CNN (93%)
   21 └─────────────────┘

   1 ArrhythmiaScanAI/
   2 ├── code.ipynb                # Core end-to-end pipeline
   3 ├── model_cnn.ipynb           # Deep Learning (1D-CNN) implementation
   4 ├── model_mlbased.ipynb       # Feature-based Machine Learning work
   5 ├── testing.ipynb             # Model evaluation & metrics
   6 ├── wavelate.ipynb            # Wavelet signal processing experiments
   7 ├── best_ecg_1dcnn_balanced.pth # Pre-trained CNN weights
   8 └── README.md                 # Documentation

  ---

  🚀 Installation

  Prerequisites
   - Python 3.10 or higher
   - Pip package manager

  Step 1: Clone Repository

   1 git clone https://github.com/addy12bag/Arrhythmia-Prediction-.git
   2 cd Arrhythmia-Prediction-

  Step 2: Environment Setup

   1 # Recommended: Create a virtual environment
   2 python -m venv venv
   3 source venv/bin/activate  # Windows: .\venv\Scripts\activate
   4
   5 # Install dependencies
   6 pip install -r requirements.txt

  ---

  💻 Usage

   1. Launch Jupyter:
   1    jupyter notebook
   2. Execute Pipeline: Open code.ipynb to run the full preprocessing and modeling workflow.
   3. Analyze Models: Explore model_cnn.ipynb and model_mlbased.ipynb for specific architecture details.

  ---

  🧠 Machine Learning Models

  Traditional ML Stream
   - Features: 18+ Statistical and temporal features per beat.
   - Performance: 97% Accuracy. 
   - Verdict: Superior performance due to highly targeted feature engineering on the MIT-BIH dataset.

  Deep Learning Stream
   - Architecture: 1D Convolutional Neural Network (1D-CNN).
   - Input: Raw segmented ECG waveform.
   - Performance: 93% Accuracy.
   - Verdict: High potential for scalability and generalization to larger, more diverse datasets.

  ---

  📊 Key Insights

   1. Expert Knowledge: In medical signal processing, handcrafted features (ML) currently outperform raw signal learning (CNN) for specific datasets like MIT-BIH.
   2. Scalability: While CNNs have slightly lower accuracy here, they eliminate the need for manual feature engineering, making them better for "big data" healthcare.
   3. Signal Quality: Proper noise filtering is the most critical step in achieving high diagnostic accuracy.

  ---

  🗺️ Roadmap

   - [ ] Real-time Monitoring: Integrate with live ECG sensor data.
   - [ ] Explainable AI (XAI): Implement SHAP/Grad-CAM to highlight arrhythmia triggers in the signal.
   - [ ] Web Dashboard: Build a React-based interface for clinician visualization.
   - [ ] Multi-Dataset Training: Expand to PTB-XL and other global ECG databases.

  ---

  👤 Author

  Sayantan Bag  
  M.Tech (Robotics)  
  Specializing in AI, Machine Learning, and Intelligent Systems.

   - 📧 Email: sayantan.bag@example.com (mailto:sayantan.bag@example.com)
   - 💼 GitHub: @addy12bag (https://github.com/addy12bag)

  ---

  📄 License

  This project is licensed under the MIT License.

  Copyright (c) 2026 Sayantan Bag.

  ---

  <div align="center">

  Developed with ❤️ for Intelligent Healthcare

  </div>
