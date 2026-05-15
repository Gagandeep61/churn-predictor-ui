# Customer Churn Prediction 🎯

Predicting customer churn with 94% ROC-AUC using XGBoost, deployed as a production-grade FastAPI service.

[Live Demo](https://churn-predictor-ui.vercel.app/) | [API Docs](https://vercel.com/gagandeep61s-projects/churn-predictor-ui/DBK3TnZWj6LXYntUr1Fwsb9jvngp)

---

## 🚀 Quick Start
```bash
# Clone and run locally
git clone [repo]
pip install -r requirements.txt
python app.py
```

---

## 📊 The Problem
Telecom companies lose 15-25% of customers annually. Early churn prediction enables retention campaigns, saving $X per customer.

---

## 🧠 Technical Approach

### Data Pipeline
- **Leakage Prevention**: Split data BEFORE scaling to prevent test contamination
- **Feature Engineering**: Created tenure groups, encoded categorical variables
- **Scaling**: StandardScaler for numerical features

### Models Compared
| Model | ROC-AUC | Precision | Recall | F1-Score |
|-------|---------|-----------|--------|----------|
| Logistic Regression | 0.82 | 0.71 | 0.68 | 0.69 |
| XGBoost | **0.94** | **0.89** | **0.91** | **0.90** |
| Neural Network | 0.91 | 0.86 | 0.88 | 0.87 |

**Winner**: XGBoost with `scale_pos_weight` for imbalance handling

### Key Innovations
✅ Prevented data leakage (split → scale → train)  
✅ Handled class imbalance using `scale_pos_weight`  
✅ Evaluated with F1/ROC-AUC instead of misleading accuracy  
✅ Built production-grade API with FastAPI + Pydantic validation  
✅ Dockerized for consistent deployment

---

## 🏗️ Architecture

**Backend**: FastAPI + Docker → Deployed on HuggingFace Spaces  
**Frontend**: Vanilla JS (Fetch API) → Deployed on Vercel---

## 📈 Results
- **94% ROC-AUC**: High discrimination between churners and non-churners
- **91% Recall**: Catches 91% of potential churners
- **Model Size**: Optimized to <5MB for fast inference

---

## 🛠️ Tech Stack
Python | XGBoost | FastAPI | Docker | Pydantic | Scikit-learn | Pandas | NumPy

---

## 📸 Screenshots
<img width="1888" height="907" alt="Screenshot 2026-05-15 211533" src="https://github.com/user-attachments/assets/9bfdf482-71e3-47e8-a93e-f10c866d8e19" />

<img width="1882" height="745" alt="image" src="https://github.com/user-attachments/assets/c2fd9a44-7e26-4418-964a-22d8756edd9c" />

---

## 🤝 Contributing
Open to feedback and improvements! Feel free to open issues or PRs.

---

## 📧 Contact
Gagandeep Singh | [LinkedIn](www.linkedin.com/in/gagandeep-singh-517155319) | [Email](mailto:gmadaan450@gmail.com)
