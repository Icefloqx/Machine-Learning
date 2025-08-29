## Student's prediction  Project


## **Project Overview**
 
-This project analyze a dataset on how AI usage in a student's life can be predicted using different models.
-The project predicts;

- Whether the student completed the session successfully.
- How time affected the sessions of the students.
- Perform correlation analysis.

*The dataset contains numeric features and also use of classification models.*


## **Dataset**

The dataset consists of the following columns:
 
 *'SessionLengthMin`: Duration of the session in minutes 
 
 *'TotalPrompts`: Number of prompts.
 
 *'AI_AssistanceLevel`: Level of AI assistance during the session.
 
 *`SatisfactionRating': Student-reported satisfaction.
 
 *'Year','Month`,`Day`: Date of the session. 
 
 *`PromptsPerMinute':Derived metric: prompts per minute.
 

**Something to note**

- The dataset is **imbalanced**: the majority class (`True`) dominates (~70% of data). 

## **Models Used**

The following are some of the  machine learning models  that were tarined:

- **Logistic Regression**  
- **Decision Tree**  
- **Random Forest**  
- **Gradient Boosting**  
- **XGBoost**  

**Observations:**

- Accuracy alone can be misleading due to imbalance.  
- Models tend to predict the majority class if imbalance is not addressed.

## **Evaluation Metrics**

Metrics used to evaluate models:

- **Accuracy** – Overall correct predictions  
- **Precision** – Total predicted positives
- **Recall** – Correct positive predictions
- **F1-Score** – Balanced mean of precision and recall  
- **Support** – Number of samples in each class

##**Technologies used**

-Python(Pandas,Matplotlib,Seaborn,Regression,Ensembles,Classification)

-Jupyter Notebook.

-Git Bash & Github.

