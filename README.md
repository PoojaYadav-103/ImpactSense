# 🌍 ImpactSense – Earthquake Impact Prediction System

ImpactSense is an **advanced machine learning–based earthquake alert classification system** developed as part of **Infosys Springboard 6.0**.
The system predicts earthquake impact levels (🟢 Green, 🟡 Yellow, 🟠 Orange, 🔴 Red) using seismic parameters to support disaster preparedness and emergency response.

> **Developed by:** Pooja Yadav  
> **Mentor:** Gopal Sir  
> **Program:** Infosys Springboard 6.0

---

## 🎯 Problem Statement

Earthquakes cause massive loss of life and property worldwide. Timely and accurate classification of earthquake impact is crucial for:

* Emergency preparedness
* Resource allocation
* Evacuation planning
* Public safety measures

### 💡 Solution

ImpactSense uses machine learning models to **classify earthquake alert levels in real time** based on seismic features, enabling actionable and early decision-making.

---

## 🚨 Alert Classification Levels

* 🟢 **Green Alert – Minimal Impact**
  Normal operations, low risk
* 🟡 **Yellow Alert – Low Impact**
  Stay alert, prepare emergency supplies
* 🟠 **Orange Alert – Moderate Impact**
  Activate response teams, evacuate vulnerable areas
* 🔴 **Red Alert – High Impact**
  Immediate evacuation, critical risk

---

## 📊 Dataset Overview

**Earthquake Alert Balanced Dataset**

| Feature      | Description                         | Range       |
| ------------ | ----------------------------------- | ----------- |
| Magnitude    | Earthquake strength (Richter scale) | 0.0 – 9.0   |
| Depth        | Distance below Earth's surface      | 0 – 1000 km |
| CDI          | Community Decimal Intensity         | 0.0 – 10.0  |
| MMI          | Modified Mercalli Intensity         | 0.0 – 10.0  |
| Significance | Overall impact score                | -300 – 1000 |

**Target Variable:** Alert Level (Green, Yellow, Orange, Red)

---

## 🛠️ Technology Stack

### Machine Learning & Data Science

* Python 3.x
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn

### Web Application

* Streamlit
* Plotly
* HTML / CSS

### Development Environment

* Google Colab
* Google Drive
* Pickle (Model Serialization)

---

## 🔬 Methodology

### 1️⃣ Data Preprocessing

* Missing value handling
* Outlier capping (preserving negative values)
* Feature scaling using StandardScaler

### 2️⃣ Feature Engineering

* **Impact Score** = Magnitude × Significance
* **Depth–Magnitude Ratio** = Depth / (Magnitude + 1)

### 3️⃣ Model Training

* Train–test split (80–20)
* Stratified sampling
* Multiple algorithms evaluated
* Hyperparameter tuning using GridSearchCV

### 4️⃣ Evaluation Metrics

* Accuracy
* Precision, Recall
* Confusion Matrix
* Feature Importance

---

## 🤖 Models Evaluated

| Model               | Baseline Accuracy | Tuned Accuracy |
| ------------------- | ----------------- | -------------- |
| Logistic Regression | ~70%              | —              |
| Decision Tree       | ~86%              | —              |
| Random Forest       | ~93%              | **93.08% ✅**   |
| Gradient Boosting   | ~90%              | ~91.54%        |
| XGBoost             | ~89.6%            | ~92.69%        |

**Best Model:** Random Forest Classifier (93.08% accuracy)

---

## 🏗️ Model Architecture

```
Random Forest Classifier
├─ n_estimators: 300
├─ max_depth: 20
├─ min_samples_split: 2
├─ min_samples_leaf: 1
├─ random_state: 42

Pipeline:
1. Data Loading
2. Preprocessing & Feature Engineering
3. Scaling
4. Model Training
5. Evaluation
6. Model Serialization (.pkl)
7. Deployment
```

---

## 🌐 Web Application

* Built using **Streamlit**
* Interactive input sliders
* Animated alert cards
* Confidence & probability visualization
* Emergency response recommendations

---

## 📁 Project Structure

```
ImpactSense/
│── app.py                  # Streamlit application
│── earthquake_model.pkl    # Trained ML model
│── requirements.txt        # Dependencies
│── README.md               # Documentation
```

---

## ⚙️ Installation & Run

```bash
git clone https://github.com/PoojaYadav-103/ImpactSense.git
cd ImpactSense
pip install -r requirements.txt
streamlit run app.py
```

---

## ☁️ Deployment

* Deployed on **Streamlit Cloud**
* Auto-updates on GitHub push
* Free & scalable hosting

---

## ⚠️ Challenges & Solutions

| Challenge                    | Solution                            |
| ---------------------------- | ----------------------------------- |
| Negative significance values | Custom outlier capping logic        |
| Class imbalance              | Balanced dataset + stratified split |
| Feature scaling issues       | Feature engineering before scaling  |
| Model selection              | Multi-model comparison & tuning     |

---

## 🚀 Future Enhancements

* Deep learning models (LSTM, CNN)
* Real-time seismic data (USGS API)
* Mobile app (Android / iOS)
* SMS & Email alert system
* Multi-language support

---

## 🌟 Real-World Impact

* Disaster management agencies
* Public alert systems
* Healthcare & infrastructure preparedness
* Community safety & resilience

---

## 👩‍💻 Author
**Pooja Yadav**

⭐ If you find this project useful, please give it a star!
