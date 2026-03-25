# Customer-Churn-Prediction-Model
Machine Learning model to predict customer churn using classification techniques.

# PROBLEM STATEMENT:
The objective of this project is to predict customer churn for a telecom company using historical customer data. By analyzing customer demographics, services, and billing information, the model aims to identify customers who are likely to leave, enabling the company to take proactive retention measures.

# DATASET DESCRIPTION:
The dataset used in this project is the Telco Customer Churn dataset, sourced from Kaggle. It contains information about a telecom company’s customers and whether they have churned (left the service) or not.

Number of records: 7,043 customers
Number of features: 21 columns

Key Features-

The dataset includes the following types of features:

# Customer Information
customerID: Unique identifier for each customer
gender: Male or Female
SeniorCitizen: Indicates if the customer is a senior citizen

# Account Information
tenure: Number of months the customer has stayed with the company
Contract: Type of contract (Monthly, One year, Two year)
PaperlessBilling: Whether the customer uses paperless billing
PaymentMethod: Mode of payment

# Service Information
PhoneService, MultipleLines
InternetService
OnlineSecurity, OnlineBackup
DeviceProtection, TechSupport
StreamingTV, StreamingMovies
Billing Information
MonthlyCharges: Monthly amount charged
TotalCharges: Total amount charged

# Target Variable
Churn: Indicates whether the customer left the service (Yes/No)

# APPROACH:

# Data Loading and Exploration
-Loaded the Telco Customer Churn dataset using Pandas
-Explored dataset shape, data types, and missing values
-Analyzed the distribution of the target variable (Churn)
-Performed initial exploratory data analysis (EDA) to understand customer behavior

# Data Cleaning and Preprocessing
-Handled missing or inconsistent values (especially in TotalCharges)
-Converted categorical variables into numerical format using encoding techniques
-Removed irrelevant features such as customerID
-Standardized/normalized numerical features where required

# Exploratory Data Analysis (EDA)
-Analyzed relationships between features and churn
-Identified important factors such as:
Tenure
Monthly Charges
Contract Type
-Used visualizations (count plots, bar charts, etc.) to detect patterns

# Feature Engineering
-Selected relevant features contributing to churn
-Transformed categorical variables using encoding (e.g., Label Encoding / One-Hot Encoding)
-Prepared the dataset for model training

# Model Selection
-Initially evaluated three classification models:
Decision Tree Classifier
Random Forest Classifier
XGBoost Classifier
- Used cross-validation scores with default parameters to compare model performance
- Selected Random Forest Classifier as it achieved the highest cross-validation score

# Model Training
- Trained the selected Random Forest model on the prepared dataset
- Used default hyperparameters for initial implementation

# Model Evaluation
Evaluated model performance using:
Accuracy Score → overall prediction correctness
Confusion Matrix → understanding true positives, false positives, etc.
Classification Report → precision, recall, and F1-score


# RESULTS :
- Model Accuracy - 77.8%
- Model Used - RandomForest Classifier

# INSIGHTS :
- Customers with month-to-month contracts have the highest churn rate, while long-term contract customers are more likely to stay.
- Customers with low tenure are more likely to churn, indicating higher risk in the early stages of the customer lifecycle.
- Higher monthly charges are associated with increased churn, suggesting pricing impacts customer retention.
- Customers who do not use value-added services like tech support or online security tend to churn more frequently.
- Electronic check users show a higher tendency to churn compared to other payment methods.
- Senior citizens have a slightly higher churn rate, indicating the need for better customer support for this segment.
