
# Credit Card Fraud Detection Project

## **Overview**
This project focuses on building a robust machine learning system to detect fraudulent credit card transactions using a highly imbalanced dataset. By leveraging advanced data exploration, feature engineering, and machine learning models, we successfully identified key patterns and developed a high-performing fraud detection system.

---

## **Dataset**
- **Source**: Kaggle Credit Card Fraud Detection Dataset.
- **Transactions**: 284,807 over two days.
- **Imbalance**: Only 0.172% of transactions are fraudulent.
- **Features**:
  - `V1` to `V28`: PCA-transformed features (numerical, confidential).
  - `Time`: Seconds elapsed since the first transaction.
  - `Amount`: Transaction value.
  - `Class`: Target variable (0 = Non-Fraud, 1 = Fraud).

---

## **Project Workflow**
### **1. Data Exploration**
- Examined class imbalance, feature distributions, and transaction patterns over time.
- Identified differences in fraud and non-fraud behaviors for amount and transaction timing.

### **2. Preprocessing**
- Applied **SMOTE** (Synthetic Minority Oversampling Technique) to address class imbalance.
- Dropped irrelevant features (`Time`, `Amount`) after normalization and exploration.
- Engineered features:
  - `Normalized_Amount`: Standardized transaction amounts.
  - `Off_Peak`: Indicator for off-peak transaction timings.

### **3. Models Used**
- **Logistic Regression**: Baseline model for interpretability and speed.
- **Random Forest**: Captured feature interactions and non-linear relationships.
- **XGBoost**: Gradient boosting model for handling complex feature interactions.

---

## **Evaluation**
### Metrics:
- **Precision-Recall Curve** (PR Curve): Emphasizes the trade-off between precision and recall for imbalanced datasets.
- **AUC Score**: Evaluates overall model performance.

### Results:
- **Logistic Regression**: AUPRC: 0.72, AUC: 0.93.
- **Random Forest**: AUPRC: 0.87, AUC: 0.92.
- **XGBoost**: AUPRC: 0.87, AUC: 0.92.

---

## **Feature Importance**
- Top contributing features: `V14`, `V10`, `V12`, `V4`.
- PCA-transformed features dominated importance, while engineered features like `Normalized_Amount` provided additional context.

---

## **Conclusion**
- **Key Achievement**: Built a fraud detection system achieving high performance (AUPRC: 0.87, AUC: 0.92).
- **Impact**: Enhanced understanding of fraud patterns and demonstrated effective handling of imbalanced datasets.
- **Recommendations**:
  - Deploy models like Random Forest or XGBoost for real-time fraud detection.
  - Continuously monitor and adapt the system to evolving transaction behaviors.

---

## **Technologies and Tools**
- **Languages**: Python
- **Libraries**: Pandas, NumPy, Scikit-learn, XGBoost, Seaborn, Matplotlib
- **Preprocessing**: SMOTE for class balancing
- **Models**: Logistic Regression, Random Forest, XGBoost

---

## **How to Run**
1. Clone this repository:  
   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```
2. Install required dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook for full implementation and analysis.

---

## **Contact**
For further details, reach out via [brandonsiuwong@gmail.com].
