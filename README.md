
# 🩺 MedGuard – Early Symptom Checker (AI + Explainable ML)

MedGuard is an **AI-powered medical diagnosis assistant** that predicts possible diseases based on user symptoms.  
It uses **XGBoost**, **Flask**, and **SHAP** for transparent, explainable predictions.  
The app displays both the predicted diagnosis and a visual explanation of which symptoms influenced it.

---

## 🚀 Features

✅ **Interactive Web App** – Symptom-based disease prediction using Flask.  
✅ **Explainable AI** – Integrated SHAP plots for feature importance and local explanations.  
✅ **Machine Learning Engine** – XGBoost Booster model trained on medical datasets.  
✅ **Secure Session Handling** – Session-based user input flow.  
✅ **Automatic Visualization** – Saves and displays SHAP plots automatically.

---

## 🧠 Architecture Overview

User → Frontend (Flask UI)
     → Authentication Module
     → Backend ML Engine (XGBoost)
     → SHAP Explainability Module
     → Output: Diagnosis + Explanation

---

## 📁 Project Structure

MEDGUARD/
│
├── data/
│   └── Training.csv
│
├── static/
│   ├── shap_global_importance.png
│   ├── shap_local_explanation.png
│
├── Templates/
│   └── index.html
│
├── app.py                     # Flask web app
├── explain_medguard.py        # SHAP visualization script
├── train_medguard.py          # XGBoost training script
├── flask_test.py              # Flask test route
│
├── medguard_booster.json      # Trained XGBoost model
├── label_encoder.pkl          # Encoded disease labels
│
├── shap_feature_ranking.csv   # SHAP feature ranking
├── README.md
└── .gitignore

---

## ⚙️ Tech Stack

| Component | Technology | Purpose |
|------------|-------------|----------|
| **Frontend** | Flask, HTML, CSS | Web UI |
| **Backend** | Flask (Python) | Model API & logic |
| **Machine Learning** | XGBoost | Disease prediction |
| **Explainability** | SHAP | Visual model interpretation |
| **Data Handling** | Pandas, NumPy | Data cleaning & preprocessing |
| **Visualization** | Matplotlib | Plot generation |
| **Storage** | PKL, JSON, CSV | Model and feature persistence |

---

## 💻 Installation Instructions

### 1️⃣ Clone the Repository
git clone https://github.com/yourusername/MedGuard.git
cd MedGuard

### 2️⃣ Create Virtual Environment

Windows:
python -m venv venv
venv\Scripts\activate

Linux / macOS:
python3 -m venv venv
source venv/bin/activate

### 3️⃣ Install Dependencies

If you have a requirements.txt file:
pip install -r requirements.txt

Or install manually:
pip install flask xgboost shap pandas numpy joblib matplotlib

### 4️⃣ Train the Model
python train_medguard.py

This script:
- Cleans dataset  
- Trains the XGBoost model  
- Saves medguard_booster.json and label_encoder.pkl

### 5️⃣ Generate Explainability Visuals
python explain_medguard.py

This generates:
- shap_global_importance.png
- shap_local_explanation.png
- shap_feature_ranking.csv

### 6️⃣ Run the Flask Web App
python app.py

Then open in your browser:
http://127.0.0.1:5000/

---

## 📊 Example Output

Prediction: Diabetes  
Confidence: 94.3%  
Generated Files:
- shap_global_importance.png
- local_user_explanation.png

---

## 📈 Model Training Summary

| Step | Description |
|------|--------------|
| Data Cleaning | Removes unwanted columns |
| Augmentation | Adds realistic variations |
| Regularization | Dropout + Label noise |
| Model | XGBoost Classifier |
| Accuracy | 70–85% (balanced) |
| Output | Booster model + Label encoder |

---

## 🧩 SHAP Visuals

| Plot Type | Description |
|------------|-------------|
| **Global Importance** | Shows overall symptom influence |
| **Local Explanation** | Explains user’s prediction reason |

---

## 🧑‍💻 Author

**Shyam Ji Srivastava**  
AI Researcher & Developer – Explainable ML in Healthcare  
Version: v3.2 (Feature-Aligned + SHAP Safe)

---

## 🪪 License

This project is released under the MIT License.  
Feel free to use, modify, and share with proper credit.

---

## 🌱 Future Enhancements

- Database for user history  
- NLP-based symptom search  
- REST API for integration  
- Model comparison with RandomForest & SVM  
- Public deployment on Render / AWS

---

# 🧰 MedGuard Setup Instructions (All OS)

## Step 1: Clone Repository
git clone https://github.com/yourusername/MedGuard.git
cd MedGuard

## Step 2: Create Virtual Environment
Windows:
python -m venv venv
venv\Scripts\activate

Linux / macOS:
python3 -m venv venv
source venv/bin/activate

## Step 3: Install Dependencies
pip install flask xgboost shap pandas numpy joblib matplotlib

## Step 4: Train Model
python train_medguard.py

## Step 5: Generate Explainability Files
python explain_medguard.py

## Step 6: Run App
python app.py

Visit: http://127.0.0.1:5000/

---

✅ Your MedGuard web app is ready!

