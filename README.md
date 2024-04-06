# SBA-Loan-Approval-Analysis-Prediction
## Introduction
1.	Background
Since its establishment in 1953, the U.S. Small Business Administration (SBA) has been dedicated to promoting and aiding the development of small enterprises within the U.S. credit market. Small businesses are a crucial source of job innovation in the United States, and the growth and development of these entities have significant social value by generating employment opportunities and reducing unemployment. The SBA mitigates bank risk and stimulates loan issuance to small businesses through its loan guarantee program. Nevertheless, the proportion of default on these guaranteed loans has been a contentious issue, sparking a broad discussion on the role of government in the credit market.

2.	Motivation
Historically, the small business loan guarantee program has propelled many startups to success, such as FedEx and Apple Computer. However, there have been numerous instances of small businesses and startups defaulting on their SBA-guaranteed loans, which has been a focal point of controversy. This has led to two perspectives: one believes that credit markets can operate efficiently without government intervention, while the other argues that the social benefits of job creation by businesses receiving government-guaranteed loans far exceed the costs associated with defaulted loans. Therefore, it is imperative to explore the effectiveness of the SBA loan guarantee program and its impact on banking decisions.

3.	Goal
The objective of this study is to thoroughly examine the role of the SBA loan guarantee program in facilitating access to credit for small businesses, analyze the main factors influencing the default rate of guaranteed loans, and assess the effectiveness of the program in creating jobs and promoting social benefits. Additionally, the study aims to provide banks with a more precise framework for risk assessment to optimize the loan approval process and enhance the overall efficiency of the small business credit market.



## Methodology
1.	Data Cleaning
Identify and correct errors and inconsistencies in the data to improve its quality. This includes: 
•	Handling Missing Values: Identify columns with missing values and decide on a strategy for handling them (e.g., imputation, deletion).
•	Removing Duplicates: Check for and eliminate any duplicate records that may skew the model training. 
•	Converting Data Types: Ensure that each column is of the correct data type (e.g., numeric, categorical). Implement data type conversion when necessary.
•	Addressing Outliers: Looking for any anomalies in the data that might need to be addressed.

2.	Exploratory Data Analysis (EDA)
Begin EDA by examining the distribution and relationships between factors such as loan sizes and industry types through visualizations and statistical summaries. This helps identify key factors influencing loan risk, spot anomalies, and challenge assumptions, guiding hypothesis and model development.

3.	Feature Engineering
Convert categorical to numeric data, create new features, normalize numerical values, and explore feature interactions to improve predictive performance. Use dimensionality reduction, like PCA, to streamline the model and minimize overfitting, preparing the data for machine learning and enhancing prediction accuracy for loan approvals.

4.	Model Selection and Training
For such a classification problem that aims to predict a binary outcome (loan approved or denied), several machine learning models could be suitable. Here are some models that we intend to employ for this project:
•	Naïve Bayes Classification: Logistic regression estimates the probability that a given input point belongs to a certain class. it could effectively handle binary classification of loan approval or denial.
•	Decision Tree: Decision tree offers an intuitive, graphical approach to decision-making, modeling complex, non-linear relationships through a series of binary questions, making them ideal for our complex loan approval problem, which could be influenced by several factors.
•	Random Forest: Based on Decision Trees, Random Forest creates a robust ensemble that averages multiple trees to reduce overfitting and enhances predictive accuracy for complex datasets in our loan approval project. 
•	Support Vector Machines (SVM): SVM excels in high-dimensional spaces by finding the optimal boundary between classes, using the kernel trick for non-linear separation, making them highly effective for distinguishing between approved and denied loans with complex feature relationships.
5.	Model Evaluation and Tuning
Evaluate model performance using appropriate metrics (e.g., accuracy, precision, recall, F1 score) and use techniques like cross-validation for more robust evaluation. Perform hyperparameter tuning to optimize the model's performance.

## Description of the Dataset
This dataset from the U.S. Small Business Administration (SBA) comprises 899,164 records and 27 columns, totaling 179.43MB, detailing various aspects of SBA loans. 

It includes key identifiers and information about borrowers, such as names and locations (city, state, zip code), as well as detailed loan specifics like the North American Industry Classification System (NAICS) code, loan approval date and fiscal year, loan terms, employment impact, and financial details (amount disbursed, loan status, and SBA's guaranteed portion). 

For the purpose of predicting loan approval outcomes or assessing loan risk, the most critical features would likely include NAICS (to gauge industry risk), Term and NoEmp (assessing loan term viability and business stability), NewExist (differentiating between new and existing businesses), CreateJob and RetainedJob (employment impact), UrbanRural (geographical market), RevLineCr and LowDoc (loan types), DisbursementGross, GrAppv, and SBA_Appv (financial exposure), and finally, MIS_Status as an indicator of loan performance. These features encapsulate the borrower's profile, loan characteristics, and the potential risk and impact associated with the loan.

Source of dataset: https://www.kaggle.com/datasets/mirbektoktogaraev/should-this-loan-be-approved-or-denied
