# Workforce-Efficiency-Analysis

Project Summary
Business Case & Goal:
The goal of this project is to predict the performance rating of employees based on various features in the dataset. This analysis will help in identifying key factors affecting performance, department-wise performance, and building a model for hiring decisions. Additionally, recommendations for improving employee performance will be provided based on insights from the analysis.

Dataset Overview:
Size: 1200 rows, 28 columns
Features:
Quantitative: 19 (11 numeric, 8 ordinal)
Qualitative: 8
Irrelevant Feature: EmpNumber (alphanumeric)
Project Goals:
Department-wise performance analysis
Identifying the top 3 important factors affecting employee performance
Building a model to predict employee performance
Providing recommendations to improve employee performance
Data Analysis
Feature Description:
The dataset includes categorical, numerical, and ordinal features.

Categorical Features:
EmpNumber
Gender
EducationBackground
MaritalStatus
EmpDepartment
EmpJobRole
BusinessTravelFrequency
OverTime
Attrition
Numerical Features:
Age
DistanceFromHome
EmpHourlyRate
NumCompaniesWorked
EmpLastSalaryHikePercent
TotalWorkExperienceInYears
TrainingTimesLastYear
ExperienceYearsAtThisCompany
ExperienceYearsInCurrentRole
YearsSinceLastPromotion
YearsWithCurrManager
Ordinal Features:
EmpEducationLevel
EmpEnvironmentSatisfaction
EmpJobInvolvement
EmpJobLevel
EmpJobSatisfaction
EmpRelationshipSatisfaction
EmpWorkLifeBalance
PerformanceRating
Analysis Types:
Univariate, Bivariate & Multivariate Analysis:
Univariate Analysis: Examines the distribution of individual features.
Bivariate Analysis: Studies the relationship between features and the target variable.
Multivariate Analysis: Analyzes the relationship between multiple features concerning the target variable.
Key Insights:
Positive correlation with performance rating: EmpEnvironmentSatisfaction, EmpLastSalaryHikePercent, EmpWorkLifeBalance.
Exploratory Data Analysis
Distribution and Statistical Measures:
Analyzed distributions for features like age, number of companies worked, hourly rate, and work experience.
Checked skewness and kurtosis of features.
Found skewness in features like YearsSinceLastPromotion.
Data Pre-Processing:
Missing Values: None
Categorical Data Conversion:
Manual Encoding: Mapping labels based on frequency.
Frequency Encoding: Transforming categorical data into numerical values based on frequency distribution.
Outlier Handling: Using IQR for non-normally distributed features.
Feature Transformation: Applied square root transformation to handle skewness.
Scaling Data: Standard scaling (mean = 0, standard deviation = 1).
Feature Selection:
Dropped unique and constant features.
Checked correlations using a heatmap.
Found no highly correlated features.
Applied PCA, reducing dimensions to 25 features.
Machine Learning Model Creation & Evaluation
Defining Features: Identified dependent and independent features.
Balancing Data: Used SMOTE to address class imbalance.
Splitting Data: 80% for training, 20% for testing.
Algorithms Used:
Support Vector Machine
Random Forest
Artificial Neural Network (MLP Classifier)
Model Performance:
Support Vector Classifier: Training accuracy: 96.61%, Test accuracy: 94.66% (overfit after hyperparameter tuning)
Random Forest: Training accuracy: 100%, Test accuracy: 95.61% (decreased after hyperparameter tuning)
Artificial Neural Network (MLP): Training accuracy: 98.95%, Test accuracy: 95.80%
Final Model:
Selected the Artificial Neural Network (MLP Classifier) for its balanced performance.

Saving Model:
Model saved using pickle.

Tools and Libraries:
Tools:
Jupyter
Libraries:
Pandas
Numpy
Matplotlib
Seaborn
pylab
Scipy
Sklearn
Pickle
Goal 1: Department-Wise Performance Analysis
Insights:
Sales: Level 3 performers dominate; males slightly outperform females.
Human Resources: Level 3 is the majority; older employees perform lower, females perform well.
Development: Predominantly level 3 performers; gender performance is similar.
Data Science: Highest level 3 performance; fewer level 2 performers, males do better.
Research & Development: Age doesn’t affect performance levels; females perform well.
Finance: Performance decreases with age; males perform better; experience inversely related to performance.
Goal 2: Top 3 Important Factors Affecting Employee Performance
Employment Environment Satisfaction: Most employees at levels 3 and 4.
Employee Salary Hike Percentage: High performance linked to salary hikes between 11-19% and 20-22%.
Employee Work Life Balance: Level 3 shows the highest performance rating.
Goal 3: A Trained Model to Predict Employee Performance
Model Accuracy:
Support Vector Classifier: 98.28%
Random Forest Classifier: 95.61%
Artificial Neural Network (MLP): 95.80%
Goal 4: Recommendations to Improve Employee Performance
Focus on improving employee environment satisfaction.
Implement regular salary hikes to boost performance.
Promote employees every 6 months.
Enhance work-life balance.
Prefer female candidates for HR roles.
Leverage the higher performance in development and sales departments.
Pay attention to employees with low/medium job satisfaction and relationship satisfaction as they often show excellent performance.
