# 🏦 LoanClassinator

![Python](https://img.shields.io/badge/Python-3.9+-0d1117?style=for-the-badge&logo=python&logoColor=00e5ff)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-0d1117?style=for-the-badge&logo=xgboost&logoColor=b900ff)
![Machine Learning](https://img.shields.io/badge/Machine_Learning-0d1117?style=for-the-badge&logo=scikit-learn&logoColor=00e5ff)

> An intelligent, ML-powered loan classification system that leverages 2.2 million Lending Club records to predict default risk and provides Context-Aware Agentic AI explanations for financial decisions.

## 📋 Overview
LoanClassinator moves beyond traditional binary "Approved/Denied" machine learning models. By combining a robust XGBoost predictive pipeline with K-Means customer segmentation, the system accurately assesses risk. More importantly, it integrates SHAP (SHapley Additive exPlanations) with an LLM-powered Agentic advisory layer to provide users with transparent, natural-language explanations of their specific financial standing and actionable paths to approval.

## 🏗️ Architecture Flow
1. **Frontend (Streamlit):** Users interact with a dark-themed, premium cinematic UI to input financial data or explore clustering dashboards.
2. **Preprocessing Layer:** Raw data is validated and transformed to match the training environment.
3. **ML Engine:** 
   - **XGBoost:** Calculates the probability of loan default.
   - **K-Means:** Groups the applicant into a specific financial cluster.
4. **Explainability (SHAP):** Extracts the top contributing features (positive and negative) for the specific prediction.
5. **AI Advisory Layer:** A contextual LLM agent consumes the SHAP values, risk scores, and cluster statistics to dynamically generate personalized financial advice and alternative loan suggestions.

## ✨ Key Features
* **High-Fidelity Predictions:** Trained on a massive 2.2M record dataset for robust default probability calculation.
* **Customer Segmentation:** Interactive dashboards visualizing where an applicant stands compared to broader financial clusters.
* **AI Financial Advisor:** Context-aware chat interfaces utilizing Large Language Models to answer specific questions about the user's loan decision.
* **Dynamic Alternatives:** Automated calculation of alternative loan terms if an applicant is initially denied.

## 🛠️ Tech Stack
* **Frontend:** Streamlit
* **Machine Learning:** XGBoost, Scikit-Learn, K-Means
* **Explainability:** SHAP
* **AI Integration:** LLM API / Python Wrappers (Agentic AI Workflow)
* **Data Manipulation:** Pandas, NumPy

## 🚀 Installation & Local Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/priyanshu-upadhyay-27/loanclassinator.git](https://github.com/priyanshu-upadhyay-27/loanclassinator.git)
   cd loanclassinator
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the application:**
   ```bash
   streamlit run streamlit_app.py
   ```

## 📁 Project Structure
```text
loanclassinator/
├── models/
│   ├── loan_xgb_model_pipeline.pkl
│   ├── loan_kmeans_model_pipeline.pkl
│   └── shap_explainer.pkl
├── pages/
│   ├── cluster.py
│   ├── eligibility.py
│   └── learn_more.py
├── utils/
│   ├── agents.py
│   ├── llm_handler.py
│   ├── prompts.py
│   ├── transformers.py
│   ├── validators.py
│   └── visualizations.py
├── custom_functions.py
├── resave_pickles.py
└── streamlit_app.py
```

---

## 🛡️ Creator & Copyright Identity

**Created and Maintained by Priyanshu Upadhyay**

This project is the original intellectual property of Priyanshu Upadhyay. It was independently architected and developed as a comprehensive showcase of end-to-end machine learning deployment and Agentic AI integration.

**About the Developer:**
* **Education:** 3rd-Year Computer Science and Engineering Undergraduate at KIET Group of Institutions, Ghaziabad.
* **Specialization:** Artificial Intelligence research, Retrieval-Augmented Generation (RAG), Large Language Model (LLM) integration, and scalable system architecture.

**Connect & Verification:**
* **GitHub:** [priyanshu-upadhyay-27](https://github.com/priyanshu-upadhyay-27)

*© 2026 Priyanshu Upadhyay. All rights reserved. Unauthorized claiming, copying, or redistribution of this specific architecture and codebase without explicit attribution is prohibited.*

---
**License:** MIT License