# Hospital-Operations-and-Revenue-Analytics-with-SQL-Machine-Learning
📌 Project Overview

Healthcare institutions generate large amounts of operational and financial data. Extracting insights from this data can improve decision-making, financial planning, and operational efficiency.

This project analyzes hospital data and attempts to predict treatment costs and payment status using machine learning models.

The project demonstrates an end-to-end healthcare data analytics workflow, including:

SQL data integration

Data cleaning and feature engineering

Exploratory data analysis (EDA)

Machine learning modeling

Model evaluation and interpretation

Even though predictive models performed poorly due to dataset limitations, the project highlights practical healthcare analytics techniques and insights.

🎯 Business Objectives

Healthcare providers must manage operational costs while maintaining high-quality care. This project aims to:

Identify drivers of treatment costs

Analyze hospital financial performance

Understand payment patterns

Predict treatment costs

Predict payment status to reduce revenue leakage

🗂 Dataset Description

The dataset consists of multiple relational tables representing hospital operations.

Patients Table

Patient ID

Gender

Date of Birth

Insurance Provider

Registration Date

Treatments Table

Treatment ID

Treatment Type

Treatment Cost

Treatment Date

Appointments Table

Appointment Date

Appointment Time

Reason for Visit

Status

Doctors Table

Doctor Name

Specialization

Years of Experience

Hospital Branch

Billing Table

Bill Date

Payment Method

Payment Status

Amount

🛠 Tools & Technologies
Languages

SQL

Python

Environment

Visual Studio Code

Libraries

Pandas

NumPy

Scikit-learn

Matplotlib

Seaborn

🔗 Data Integration (SQL)

Multiple datasets were merged using LEFT JOINs to create a comprehensive dataset.

SELECT *
FROM treatments t
LEFT JOIN appointments a
ON t.appointment_id = a.appointment_id
LEFT JOIN doctors d
ON a.doctor_id = d.doctor_id
LEFT JOIN patients p
ON t.patient_id = p.patient_id
LEFT JOIN billing b
ON t.bill_id = b.bill_id


This ensured that all treatment records were retained while linking related data.

🧹 Data Preparation

Data preprocessing included:

Handling missing values

Renaming and reordering columns

Converting date columns to datetime

Extracting patient age

Extracting appointment hour

Encoding categorical variables

These steps prepared the dataset for machine learning analysis.

📊 Exploratory Data Analysis

Key insights discovered:

👥 Patient Demographics

65% of patients were male

Median age was 36 years

👨‍⚕️ Doctors’ Workload

Dr. Sarah handled 23% of patients

Dr. Robert handled the least patients

🏥 Hospital Branch Performance

Central Hospital recorded the highest number of appointments

💰 Financial KPIs

Total revenue: $551,249.85

Central Hospital generated the highest revenue.

💳 Payment Insights

34.5% of payments were pending

Only 32% were successful

This indicates potential revenue collection inefficiencies.

📈 Operational Insights
Appointment Volume by Hour

Peak appointment time:

🕒 3 PM

Lowest appointment volume:

🕓 4 PM

🩺 Clinical Insights
Most Common Treatments
Treatment	Share
Chemotherapy	24.5%
X-Ray	20.5%
ECG	19%
Physiotherapy	18%
MRI	18%
Revenue Contribution
Treatment	Revenue Share
Chemotherapy	23.38%
MRI	21.06%
X-Ray	20.07%

Interestingly:

📊 MRI generated high revenue despite fewer appointments.

🤖 Machine Learning Models

Two predictive tasks were performed.

1️⃣ Treatment Cost Prediction (Regression)

Models used:

Multiple Linear Regression

Support Vector Regression (SVR)

2️⃣ Payment Status Prediction (Classification)

Model used:

Decision Tree Classifier

📉 Model Performance

The models performed poorly due to dataset limitations.

Model	Performance
Linear Regression	R² = -0.22
SVR	R² = -0.36
Cross-Validation Model	Mean R² ≈ -0.02
Decision Tree	Accuracy = 23%

Negative R² values indicate underfitting.

🔎 Feature Importance

Using Random Forest feature importance:

Feature	Importance
Age	0.29
Insurance Provider	Moderate
Gender	0.05

Age was the strongest predictor among selected features.

⚠️ Limitations

Several factors limited model performance:

Small dataset

Missing important clinical variables

Limited feature engineering

Lack of treatment severity data

🚀 Future Improvements

To improve the analysis:

Use larger healthcare datasets

Include medical condition severity

Add treatment duration variables

Apply advanced models like:

✔ Random Forest
✔ XGBoost
✔ Gradient Boosting
✔ Neural Networks

📚 Skills Demonstrated

This project demonstrates practical skills in:

SQL Data Integration

Data Cleaning

Feature Engineering

Exploratory Data Analysis

Machine Learning Modeling

Model Evaluation

👤 Author

Chukwudi Cajetan

Optometrist | Data Analyst | Healthcare Analytics Enthusiast

Interested in applying data analytics and machine learning to improve healthcare systems and patient outcomes.

⭐ If you found this project useful, feel free to star the repository!
