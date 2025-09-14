# 🔋 Predicting Remaining Useful Life (RUL) of Batteries

## 📌 Overview
This project focuses on predicting the **Remaining Useful Life (RUL)** of batteries using machine learning techniques.  
By analyzing battery cycle data and health parameters, we can forecast how many cycles a battery will last before reaching its end-of-life — a crucial task for **predictive maintenance** in EVs, IoT devices, and energy storage systems.

---

## 📊 Dataset

- **Source:** [Kaggle - Battery Remaining Useful Life (RUL)](https://www.kaggle.com/datasets/ignaciovinuales/battery-remaining-useful-life-rul)
- **Size:** 15,064 rows × 9 columns  
- **Features include:**
  - `Cycle_Index` – Cycle number  
  - `Discharge Time (s)` – Discharge duration  
  - `Decrement 3.6-3.4V (s)` – Time spent between 3.6V to 3.4V  
  - `Max./Min. Voltage` – Battery charge/discharge voltage limits  
  - `Time at 4.15V (s)` – Duration battery stayed at 4.15V  
  - `Charging time (s)` – Total charge time  
  - `RUL` – Remaining Useful Life (Target Variable)

---

## 🧠 Methodology

### 🔧 Preprocessing
- Handled missing data (none found ✅)
- Normalized and scaled input features
- Created `RUL_Class` → Categorized RUL into:
  - **0:** Critical (RUL ≤ 400)
  - **1:** Moderate (400 < RUL ≤ 800)
  - **2:** Healthy (RUL > 800)

### 📈 Models Implemented
| Model                  | Accuracy |
|-----------------------|---------|
| **Decision Tree** 🌟 | **99.6%** |
| Logistic Regression   | 97.3% |
| Linear SVM (RBF)      | 93.2% |
| Gaussian Naïve Bayes  | 76.8% |
| Non-linear SVM (Poly) | 36.9% |

---

## 📊 Results & Visualizations

### 🔹 Distribution of Battery Parameters(Voltage)
![Voltage Distribution](https://github.com/Shubham230305/Predicting-Remaining-Useful-Life-of-Battery/blob/main/Images/voltage_distribution.png)

### 🔹 Confusion Matrix (Logistic Regression)
![Confusion Matrix](https://github.com/Shubham230305/Predicting-Remaining-Useful-Life-of-Battery/blob/main/Images/logistic_cm.png)

### 🔹 Model Accuracy Comparison
![Model Accuracy](https://github.com/Shubham230305/Predicting-Remaining-Useful-Life-of-Battery/blob/main/Images/model_comparison.png)

---

## 🚀 Key Insights
- **Decision Tree Classifier** gave the highest accuracy (**99.6%**), making it ideal for predicting RUL.
- Logistic Regression also performed well and is a good choice for a simpler model.
- SVM (Polynomial) performed poorly — not recommended for this dataset.

---

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn
- **Tools:** Jupyter Notebook, GitHub

---

## 📌 Future Work
- Integrate **LSTM / GRU models** for sequence-based RUL prediction.
- Deploy a **web dashboard** for real-time RUL monitoring.
- Test on **real-world streaming battery data**.

---

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---
