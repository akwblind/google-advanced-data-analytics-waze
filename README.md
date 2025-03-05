# **GoogleAdvancedDataAnalyticsWazeProject**

## **Predictive Modeling Waze User Churn Project** 

### **Project Overview**
In this hypothetical scenario, I was part of Waze's data analytics team, working to reduce monthly user churn (users who uninstall or stop using the Waze app). The goal of this project was to develop a machine learning (ML) model that predicts churn, using a dataset provided as part of Google's Advanced Data Analytics course.

I explored multiple modeling techniques, including regression modeling, random forest, and XGBoost, to determine the best predictive approach. However, the results indicated that additional data is needed to improve model accuracy, particularly in capturing key behavioral drivers of churn.

---

### **Business Understanding**

#### **Stakeholders and Roles**

- **Data Team:**
  - **Harriet Hadzic** – Director of Data Analysis
  - **May Santner** – Data Analysis Manager
  - **Chidi Ga** – Senior Data Analyst
  - **Sylvester Esperanza** – Senior Project Manager

- **Other Key Roles:**
  - **Emrick Larson** – Finance and Administration Department Head
  - **Ursula Sayo** – Operations Manager

#### **Business Problem & Objective**
Waze's leadership team seeks a predictive model to identify users likely to churn, allowing them to implement targeted retention strategies. Our task is to develop a machine learning solution using available user data to provide actionable insights.

---

### **Data Understanding**
As part of Google's Advanced Data Analytics course, I worked with a provided dataset, "**waze_dataset.csv**," which contained 14,999 rows and 13 columns of synthetic data created in partnership with Waze.

#### **Data Limitations:**
- **Dataset Size**: The relatively small sample size limited the ability to train a highly accurate machine learning model.
- **Class Imbalance**: Approximately 80% of users did not churn, while 20% did, leading to an imbalanced target variable. This imbalance likely affected model performance, making it harder to predict churned users accurately.

---

### **Modeling and Evaluation**
For this project, I applied two machine learning models to predict user churn: **Random Forest** and **XGBoost**. The dataset was split into 80% training and 20% test data, and I split the training data into a 75/25 training/validation set. I also dropped 700 missing values from the 'label' column (binary variable: churned vs. unchurned).

#### **Model Performance Metrics:**

- **Random Forest:**
  - **Precision**: 0.457
  - **Recall**: 0.127
  - **F1-Score**: 0.198
  - **Accuracy**: 0.819

- **XGBoost:**
  - **Precision**: 0.426
  - **Recall**: 0.171
  - **F1-Score**: 0.244
  - **Accuracy**: 0.812
    
- **Confusion Matrix**
<img src="https://github.com/user-attachments/assets/acff2f12-91df-47ba-b5d9-b5fdc56da9f9" width="500"/>

#### **Analysis:**
Both models showed low recall, meaning they missed a significant portion of users who churned — this is critical since our goal is to accurately identify potential churners. The low precision and F1-scores indicate that both models struggle to predict churn events accurately. While accuracy was relatively high, it could be misleading given the class imbalance in the dataset, where 82% of users didn’t churn. Thus, a model that predicts "no churn" for most users would still appear accurate but fail to identify the churners. 

Of note, I did perform hyperparameter tuning and tested the model on the validation set to confirm the model didn't overfit the training data. Below you will find the variables that had the greatest effect on the models.

<img src="https://github.com/user-attachments/assets/14927932-456e-4e4e-b0b5-342a4d5382c4" width="600"/>

---

### **Conclusion**

The final analysis confirmed that the provided dataset is insufficient to build a reliable predictive model for user churn. I recommend gathering additional data, such as geographic locations and user interaction frequency, to enhance model accuracy. More comprehensive data is essential for developing a model that can consistently predict user churn with higher precision.
