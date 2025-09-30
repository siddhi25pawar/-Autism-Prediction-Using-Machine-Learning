🧠 Autism Spectrum Disorder (ASD) Prediction using Machine Learning
📌 Project Overview

This project implements a robust Machine Learning pipeline to predict the likelihood of Autism Spectrum Disorder (ASD).
Leveraging data from the AQ-10 screening questionnaire and key demographic features, the goal is to build a reliable, automated tool that can support clinicians and parents in early-stage preliminary assessments.

✅ Final Model Accuracy: ~85%
✅ Focus on Recall: Minimizing False Negatives (missed ASD cases)

🚀 Key Features & Methodology

Classification Task → Binary classification to predict ASD presence (1) or absence (0).

Data Preprocessing → Label Encoding for categorical features + handling missing values.

Class Imbalance Mitigation → Applied SMOTE (Synthetic Minority Over-sampling Technique).

Model Selection → Compared Decision Tree, Random Forest, and XGBoost.

Hyperparameter Tuning → Used RandomizedSearchCV for optimization.

Evaluation Metric → Prioritized Recall to ensure fewer missed ASD cases.

📊 Performance Summary

Best Model: Random Forest (after hyperparameter tuning)

Accuracy: ~85%

Recall (ASD class): High priority → correctly identifying ASD cases

Feature Importance:

AQ-10 scores (primary drivers)

Age and Family history (austim) strongly influence predictions

🔬 Domain Insights

High-Stakes Prediction → A False Negative (missed ASD case) is more critical than a False Positive, since professional diagnosis can correct the latter.

Feature Interpretation → AQ-10 binary responses + demographic context (gender, ethnicity, family relation) strengthen reliability.

⚙️ Installation & Setup

To reproduce results:

# Clone the repository
git clone https://github.com/your-username/Autism-Prediction.git

# Navigate to project folder
cd Autism-Prediction

# (Optional) Create virtual environment
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

# Install dependencies
pip install -r requirements.txt

Run the Jupyter Notebook
jupyter notebook


Open Autism_Prediction.ipynb and run all cells.

📂 Dataset

The project uses train.csv, which includes:

AQ-10 Screening Scores (binary responses)

Demographic Features (age, gender, ethnicity, relation)

Family History of Autism

Target Variable: ASD (0 = No, 1 = Yes)

🛠️ Technologies Used

Python 3

Pandas, NumPy → Data preprocessing & manipulation

Scikit-learn → ML models, RandomizedSearchCV

Imbalanced-learn (SMOTE) → Class balancing

XGBoost → High-performance gradient boosting

Matplotlib, Seaborn → Data visualization

🔮 Future Work

🌐 Deployment → Build a Streamlit/Gradio web app for live model testing

📊 Explainability → Use SHAP values for feature importance on individual predictions

📈 Extended Dataset → Improve generalization with larger, diverse datasets

⚠️ Disclaimer

This project is for educational and experimental purposes only.
It should not be used as a substitute for professional medical diagnosis. Always consult certified healthcare professionals for autism assessment.
