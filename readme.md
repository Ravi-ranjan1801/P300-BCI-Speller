# 🧠 P300 Speller using CNN (BCI)

This project implements a **P300-based Brain–Computer Interface (BCI) speller** using EEG signals and a Convolutional Neural Network (CNN).  
The system detects P300 event-related potentials and decodes characters using the classical **row–column speller paradigm**.

---

## 🎯 Objective

- Detect P300 responses from multi-channel EEG
- Train a CNN to classify target vs non-target flashes
- Decode characters and words from stimulus probabilities
- Demonstrate a pseudo-online P300 speller

---

## 🧠 Dataset

- **BCI Competition II – P300 Speller**
- Sampling rate: **240 Hz**
- Channels: **64 EEG channels**
- Binary labels: target (1), non-target (0)

---

## 📁 Project Structure

```text
P300_BCI_Project/
├── data/                       # EEG data & test splits
├── models/                     # Trained CNN model (.keras)
├── notebooks/
│   ├── 01_load_and_explore_data.ipynb
│   ├── 02_preprocessing_and_training.ipynb
│   └── 03_demo_p300_speller.ipynb
└── README.md

---

## 🔬 Method Overview

1. **Load & explore EEG data**
2. **Preprocess and epoch signals** (800 ms post-stimulus)
3. **Train CNN** for P300 classification (offline)
4. **Save trained model**
5. **Decode characters and words** (pseudo-online demo)

---

## 📈 Results

- Test Accuracy: **~98%**
- ROC-AUC: **~0.99**
- Stable convergence with minimal overfitting

---

## ▶️ Usage

Run notebooks **in order**:

1. `01_load_and_explore_data.ipynb`
2. `02_preprocessing_and_training.ipynb`
3. `03_demo_p300_speller.ipynb` (loads pretrained model)

---

## 🧪 Demo

- Accumulates classifier probabilities
- Performs row–column decoding
- Prints decoded characters sequentially

---

## 👤 Author

**Ravi Ranjan**  
B.Tech CSE — BCI Lab Project

---

## 📜 Note

This is an **offline-trained, pseudo-online** P300 speller intended for academic use and future extension to real EEG hardware.
