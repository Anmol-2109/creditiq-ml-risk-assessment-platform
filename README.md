
# CreditIQ – Explainable Credit Risk Assessment Platform

AI-powered Credit Risk Assessment Platform built using **XGBoost, SHAP, FastAPI, and React**. The platform predicts borrower default risk, explains predictions using Explainable AI, evaluates fairness across demographic groups, and provides interactive analytics dashboards for model monitoring and decision support.

---

## 🚀 Live Demo

### Frontend
https://creditiq-ml-risk-assessment-platfor.vercel.app/

### Backend API
https://creditiq-backend-ot5n.onrender.com/

### GitHub Repository
https://github.com/Anmol-2109/creditiq-ml-risk-assessment-platform

---

# 📌 Project Overview

CreditIQ is a full-stack Machine Learning platform designed to perform intelligent credit risk assessment using supervised learning and Explainable AI.

The system not only predicts whether a borrower is likely to default but also provides transparent explanations behind every prediction, making the model interpretable and suitable for financial decision-making workflows.

Key capabilities include:

- Credit risk prediction
- Explainable AI using SHAP
- Fairness analysis
- Batch prediction
- Real-time inference
- Interactive dashboards
- Cloud deployment

---

# 🏗️ System Architecture

```text
                 React Frontend
                        |
                        |
                    FastAPI
                        |
       --------------------------------
       |              |              |
    XGBoost       SHAP Engine    Metrics
     Model                         API
       |
       |
 Feature Engineering
       |
       |
 Credit Risk Dataset
```

---

# 🧠 Machine Learning Concepts Used

### Supervised Learning

- Binary Classification
- Probability-Based Prediction
- Risk Scoring

### Data Processing

- Data Cleaning
- Outlier Handling
- Feature Engineering
- Feature Transformation

### Model Development

- Stratified Train-Test Split
- 5-Fold Cross Validation
- Hyperparameter Optimization
- Threshold Tuning

### Explainable AI

- SHAP (SHapley Additive Explanations)
- Global Feature Importance
- Local Prediction Explanations

### Responsible AI

- Fairness Analysis
- Bias Detection
- Disparate Impact Measurement

---

# ⚙️ Technology Stack

## Machine Learning

- Python
- Scikit-Learn
- XGBoost
- SHAP
- NumPy
- Pandas

## Backend

- FastAPI
- Uvicorn
- Pydantic

## Frontend

- React
- Vite
- Axios
- Recharts

## Deployment

- Render
- Vercel
- GitHub

---

# 📊 Feature Engineering

The project creates several custom predictive features:

### Log Income

```python
log_income = log1p(monthly_income)
```

### Income-to-Debt Ratio

```python
income_to_debt
```

### Credit per Age

```python
credit_per_age
```

### Delinquency Score

Weighted score using:

- 30-59 day late payments
- 60-89 day late payments
- 90+ day late payments

### High Utilization Flag

```python
high_util = rev_util > 0.8
```

---

# 🤖 Model Training

CreditIQ uses:

## XGBoost Classifier

Training pipeline includes:

- Stratified Train-Test Split
- 5-Fold Cross Validation
- Probability Estimation
- Threshold Optimization

### Training Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- KS Statistic
- Gini Coefficient

---

# 📈 Model Evaluation

The system evaluates model performance using industry-standard credit risk metrics.

| Metric | Purpose |
|----------|----------|
| Accuracy | Overall correctness |
| Precision | Positive prediction quality |
| Recall | Default detection capability |
| F1 Score | Precision-Recall balance |
| ROC-AUC | Ranking performance |
| KS Statistic | Credit score separation power |
| Gini Coefficient | Credit scoring effectiveness |

---

# 🔍 Explainable AI (SHAP)

The platform uses SHAP TreeExplainer to provide:

### Local Explanations

Explains:

- Why a borrower was classified as risky
- Which features contributed most

### Global Explanations

Provides:

- Feature importance ranking
- Overall model behavior

Benefits:

- Transparency
- Interpretability
- Regulatory compliance support

---

# ⚖️ Fairness Analysis

The system performs fairness evaluation across age groups.

Metrics include:

- Group Accuracy
- Prediction Rate
- Actual Default Rate
- Average Risk Probability
- Disparate Impact Ratio

This helps identify potential bias and supports Responsible AI practices.

---

# 🌐 Frontend Features

## Credit Risk Prediction

- Real-time inference
- Risk probability score
- Risk category prediction

## Explainability Dashboard

- SHAP explanations
- Top contributing factors
- Feature impact analysis

## Metrics Dashboard

Displays:

- ROC-AUC
- Accuracy
- Precision
- Recall
- F1 Score
- KS Statistic
- Gini

## Fairness Dashboard

Displays:

- Fairness metrics
- Bias analysis
- Age-group comparisons

## Batch Prediction

Supports:

- CSV Upload
- Bulk Risk Assessment
- Prediction Summary

---

# 🔗 API Endpoints

## Health Check

```http
GET /health
```

## Single Prediction

```http
POST /predict
```

## Batch Prediction

```http
POST /predict/batch
```

## Model Metrics

```http
GET /metrics
```

## Global SHAP Analysis

```http
GET /global-shap
```

## Fairness Analysis

```http
GET /fairness
```

---

# 📁 Project Structure

```text
creditiq-ml-risk-assessment-platform
│
├── backend
│   ├── app.py
│   ├── artifacts
│   │   ├── xgb_model.pkl
│   │   ├── explainer.pkl
│   │   ├── metrics.json
│   │   └── fairness.json
│   │
│   ├── model
│   │   ├── preprocess.py
│   │   ├── feature_engineering.py
│   │   ├── train.py
│   │   └── evaluate.py
│   │
│   ├── data
│   └── requirements.txt
│
├── frontend
│   ├── src
│   │   ├── components
│   │   ├── pages
│   │   ├── services
│   │   └── assets
│   │
│   ├── public
│   ├── package.json
│   └── vite.config.js
│
└── README.md
```

---

# 💻 Local Setup

## Clone Repository

```bash
git clone https://github.com/Anmol-2109/creditiq-ml-risk-assessment-platform.git

cd creditiq-ml-risk-assessment-platform
```

---

## Backend Setup

```bash
cd backend

pip install -r requirements.txt

uvicorn app:app --reload
```

Backend:

```text
http://localhost:8000
```

---

## Frontend Setup

```bash
cd frontend

npm install

npm run dev
```

Frontend:

```text
http://localhost:5173
```

---

# ☁️ Deployment

## Backend (Render)

```text
https://creditiq-backend-ot5n.onrender.com/
```

## Frontend (Vercel)

```text
https://creditiq-ml-risk-assessment-platform-6mvz-mkalu9klx.vercel.app/
```

---

# 🎯 Learning Outcomes

This project demonstrates:

- Supervised Machine Learning
- Binary Classification
- Feature Engineering
- Explainable AI
- SHAP Analysis
- Fairness-Aware Machine Learning
- Model Evaluation
- FastAPI Development
- React Development
- REST APIs
- Cloud Deployment
- Production ML Systems

---

# 🚀 Future Enhancements

- Model Drift Detection
- User Authentication
- Monitoring Dashboard
- Experiment Tracking
- Model Registry
- Docker Containerization
- CI/CD Pipeline
- Kubernetes Deployment
- Real-Time Monitoring

---

# 👨‍💻 Author

**Anmol Kumar**

B.Tech Computer Science Engineering

Aspiring Software Engineer | Machine Learning Engineer

GitHub:
https://github.com/Anmol-2109
