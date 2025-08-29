#AI Assistant Usage in Student's Life

This repository contains a machine learning project that predicts student's effect on the ussage of AI and other outcomes using session features, the AI itself and other engagement metrics. The project demonstrates handling a dataset and model evaluation using multiple classification algorithms.


## **Project Overview**

The goal of this project is to **predict a binary outcome** for student sessions, such as:

- Whether the student completed the session successfully  
- Or whether the student engaged/returned in the future  

The dataset contains numeric features, encoded categorical variables, and derived metrics. Special attention was given to **handling class imbalance** using techniques like SMOTE and class weighting.

---

## **Dataset Description**

The dataset consists of the following columns:

| Column Name             | Description |
|-------------------------|-------------|
| `SessionLengthMin`      | Duration of the session in minutes |
| `TotalPrompts`          | Number of prompts/questions per session |
| `AI_AssistanceLevel`    | Level of AI assistance during the session (integer) |
| `StudentLevel_encoded`  | Encoded student level (novice, intermediate, advanced) |
| `SatisfactionRating`    | Student-reported satisfaction (float) |
| `Year`, `Month`, `Day`  | Date of the session |
| `PromptsPerMinute`      | Derived metric: prompts per minute |
| `Outcome`               | Target variable (binary: True/False) |

**Notes:**

- The dataset is **imbalanced**: the majority class (`True`) dominates (~70% of data).  
- Duplicate columns were removed during preprocessing.  

---

## **Preprocessing**

Key preprocessing steps:

1. **Remove duplicate columns**  
2. **Encode categorical features** (student level already encoded)  
3. **Scale numeric features** (optional for some models)  
4. **Handle class imbalance**:  
   - Using **SMOTE** to oversample the minority class  
   - Or using **class weights** in models like Logistic Regression or XGBoost  

---

## **Models Used**

The following machine learning models were trained and evaluated:

- **Logistic Regression**  
- **Decision Tree**  
- **Random Forest**  
- **Gradient Boosting**  
- **XGBoost**  
- **Stacking Classifier** (ensemble of multiple models)  

**Observations:**

- Accuracy alone can be misleading due to imbalance.  
- Models tend to predict the majority class if imbalance is not addressed.  
- SMOTE or class weights improve **minority class recall and F1-score**.

---

## **Evaluation Metrics**

Metrics used to evaluate models:

- **Accuracy** – Overall correct predictions  
- **Precision** – Correct positive predictions / total predicted positives  
- **Recall** – Correct positive predictions / total actual positives  
- **F1-Score** – Harmonic mean of precision and recall  
- **Support** – Number of samples in each class  

**Tip:** On imbalanced datasets, **F1-score for the minority class** and **macro-average metrics** are more informative than accuracy.

---

## **Usage**

Clone the repository:

```bash
git clone https://github.com/yourusername/student-session-prediction.git
cd student-session-prediction
