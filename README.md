# ❤️ Arrhythmia Prediction using Hybrid ML–DL

A hybrid Machine Learning and Deep Learning pipeline for detecting cardiac arrhythmias from ECG signals using the MIT-BIH dataset. This project focuses on signal preprocessing, feature engineering, and comparative modeling.

---

## 📌 Problem Statement

Cardiac arrhythmias are irregular heart rhythms that can lead to severe health complications if not detected early. ECG signal analysis is critical, but manual interpretation is time-consuming and error-prone.

This project aims to:

* Automate arrhythmia detection
* Compare ML vs Deep Learning performance
* Build a structured ECG processing pipeline

---

## 🧠 Approach

### 🔹 Data Source

* MIT-BIH Arrhythmia Dataset (PhysioNet)

---

### 🔹 Pipeline

1. **ECG Preprocessing**

   * Noise filtering
   * Signal normalization
   * Beat segmentation

2. **Feature Engineering (ML)**

   * Statistical features
   * Temporal characteristics

3. **Modeling**

* **Machine Learning Model**

  * Feature-based approach
  * Achieved ~97% accuracy

* **Deep Learning Model (1D CNN)**

  * Raw ECG input
  * Achieved ~93% accuracy

---

## 📊 Key Insights

* ML outperformed CNN due to strong feature engineering
* CNN provides better scalability for larger datasets
* Feature quality is critical in medical signal processing

---

## 📁 Repository Structure

```bash
Arrhythmia-Prediction/
│
├── code.ipynb                # Main pipeline
├── model_cnn.ipynb           # CNN model
├── model_mlbased.ipynb       # ML model
├── testing.ipynb             # Testing & evaluation
├── wavelate.ipynb            # Signal processing / wavelet work
├── best_ecg_1dcnn_balanced.pth   # Trained CNN model
├── README.md
```

---

## ⚙️ Tech Stack

* Python
* NumPy, Pandas
* Scikit-learn
* PyTorch
* Matplotlib

---

## 🚀 How to Run

1. Clone the repo:

```bash
git clone https://github.com/addy12bag/Arrhythmia-Prediction-.git
cd Arrhythmia-Prediction-
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open notebooks:

```bash
jupyter notebook
```

---

## ⚠️ Limitations

* No real-time prediction system
* No deployment/UI yet
* Dataset not included due to size constraints

---

## 🔮 Future Work

* Add ECG signal visualization
* Build real-time prediction system
* Add explainability (SHAP / Grad-CAM)
* Develop a web interface for usability

---

## 👤 Author

**Sayantan Bag**
M.Tech (Robotics)
Interested in AI, ML, and real-world intelligent systems

GitHub: https://github.com/addy12bag

---

## 🚨 Note

This project focuses on modeling and signal processing.
Future versions aim to convert it into a deployable healthcare application.

---
