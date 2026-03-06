# 🔬 Breast Cancer Predictor

> An interactive ML web app for breast tumor classification using K-Nearest Neighbors on the Wisconsin Breast Cancer Dataset.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-MyBinder-blue?style=for-the-badge)](https://mybinder.org/v2/gh/YOUR-USERNAME/breast-cancer-predictor/main?urlpath=voila/render/breast_cancer_voila.ipynb)
[![Python](https://img.shields.io/badge/Python-3.9+-yellow?style=for-the-badge&logo=python)](https://python.org)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange?style=for-the-badge)](https://scikit-learn.org)
[![Voilà](https://img.shields.io/badge/Voil%C3%A0-0.4-green?style=for-the-badge)](https://voila.readthedocs.io)

---

## 📌 Overview

This project transforms a Jupyter notebook into a fully interactive web application that predicts whether a breast tumor is **Benign** or **Malignant** based on 30 clinical features extracted from digitized images of fine needle aspirate (FNA) biopsies.

The app uses a **KNN classifier (k=2)** with **StandardScaler** preprocessing, achieving **94.7% accuracy** on the Wisconsin Breast Cancer Dataset.

---

## 🖥️ Live Demo

🔗 **[Launch the app on MyBinder](https://mybinder.org/v2/gh/YOUR-USERNAME/breast-cancer-predictor/main?urlpath=voila/render/breast_cancer_voila.ipynb)**

> ⚠️ First load may take 2–3 minutes while the environment builds.

---

## ✨ Features

- **Interactive feature editor** — modify all 30 clinical features directly in the UI
- **3 feature groups** — Mean, Standard Error (SE), and Worst values
- **Real-time prediction** — KNN model runs instantly on click
- **Confidence score** — visual confidence bar with probability breakdown
- **Top 3 influential features** — z-score based feature importance per prediction
- **Model metrics** — Accuracy, F1-score, Recall displayed in the header

---

## 📊 Model Performance

| Metric | Value |
|---|---|
| Accuracy | 94.7% |
| F1-Score (Malignant) | 0.923 |
| Recall (Benign) | 1.000 |
| Train Samples | 455 |
| Test Samples | 114 |

**Confusion Matrix:**
```
              Benign   Malignant
Benign          72         0
Malignant        6        36
```

---

## 🗂️ Dataset

**Wisconsin Breast Cancer Dataset** — 569 samples, 30 features, binary classification.

| Label | Count | Description |
|---|---|---|
| Benign (B → 0) | 357 | Non-cancerous tumor |
| Malignant (M → 1) | 212 | Cancerous tumor |

Features are computed from digitized images of FNA biopsies and describe characteristics of cell nuclei:
- **Mean** — average value per image
- **Standard Error (SE)** — variability across the image
- **Worst** — mean of the 3 largest values

---

## 🚀 Run Locally

### Prerequisites
```bash
pip install voila ipywidgets scikit-learn pandas numpy ipykernel
python -m ipykernel install --user --name python3
```

### Launch
```bash
git clone https://github.com/YOUR-USERNAME/breast-cancer-predictor.git
cd breast-cancer-predictor
python -m voila breast_cancer_voila.ipynb
```

Opens at `http://localhost:8866`

---

## 📁 Project Structure

```
breast-cancer-predictor/
├── breast_cancer_voila.ipynb   # Main app notebook
├── breast-cancer.csv           # Wisconsin dataset
├── requirements.txt            # Python dependencies
└── README.md
```

---

## 🛠️ Tech Stack

| Tool | Role |
|---|---|
| Python 3.9+ | Core language |
| scikit-learn | KNN model + StandardScaler pipeline |
| pandas / numpy | Data processing |
| ipywidgets | Interactive UI components |
| Voilà | Notebook → Web app conversion |
| MyBinder | Free cloud hosting |

---

## ⚠️ Disclaimer

This tool is built for **educational and portfolio purposes only**. It is **not** a clinical diagnostic tool and should not be used for medical decisions.

---

## 📄 License

MIT License — feel free to fork and adapt.
