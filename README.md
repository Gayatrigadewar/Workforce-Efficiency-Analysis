# Workforce-Efficiency-Analysis

## Project Summary

### Business Case & Goal:
Based on the given features of the dataset, we need to predict the performance rating of employees. The data science project involves an analysis of employee performance to achieve the following goals:

1. Department-wise performances
2. Identify top 3 important factors affecting employee performance
3. Develop a trained model to predict employee performance based on input factors for hiring decisions
4. Provide recommendations to improve employee performance based on insights from the analysis

### Dataset Overview:
- **Rows:** 1200
- **Columns:** 28
- **Quantitative Features:** 19 (11 numeric, 8 ordinal)
- **Qualitative Features:** 8
- **Irrelevant Feature:** EmpNumber (alphanumeric)

## Analysis

### Feature Description:
The dataset includes categorical, numerical, and ordinal features.

#### Categorical Features:
- EmpNumber
- Gender
- EducationBackground
- MaritalStatus
- EmpDepartment
- EmpJobRole
- BusinessTravelFrequency
- OverTime
- Attrition

#### Numerical Features:
- Age
- DistanceFromHome
- EmpHourlyRate
- NumCompaniesWorked
- EmpLastSalaryHikePercent
- TotalWorkExperienceInYears
- TrainingTimesLastYear
- ExperienceYearsAtThisCompany
- ExperienceYearsInCurrentRole
- YearsSinceLastPromotion
- YearsWithCurrManager

#### Ordinal Features:
- EmpEducationLevel
- EmpEnvironmentSatisfaction
- EmpJobInvolvement
- EmpJobLevel
- EmpJobSatisfaction
- EmpRelationshipSatisfaction
- EmpWorkLifeBalance
- PerformanceRating

### Univariate, Bivariate & Multivariate Analysis:
- **Univariate Analysis:** Examines the unique labels of categorical features and the range & density of numeric features.
- **Bivariate Analysis:** Examines the relationship between each feature and the target variable.
- **Multivariate Analysis:** Examines the relationship between two or more features with respect to the target variable.

**Conclusion:** Features like EmpEnvironmentSatisfaction, EmpLastSalaryHikePercent, and EmpWorkLifeBalance show a positive correlation with performance rating.

## Exploratory Data Analysis

### Basic Checks & Statistical Measures:
- No constant columns in numerical or categorical data.
- **Distribution Analysis:**
  - Age distribution is primarily between 30-40 years.
  - Most employees worked up to 2 companies before the current one.
  - Hourly rate range is 65-95 for most employees.
  - Employees generally have up to 5 years of experience in the company.

### Skewness and Kurtosis of Numerical Features:
- **YearsSinceLastPromotion** is skewed:
  - Skewness: 1.972
  - Kurtosis: 3.519

## Data Pre-Processing

1. **Check Missing Values:** No missing values found.
2. **Categorical Data Conversion:** 
   - Manual Encoding
   - Frequency Encoding
3. **Outlier Handling:** Used IQR for features with outliers.
4. **Feature Transformation:** Applied Square Root Transformation for skewed data.
5. **Scaling:** Standard scaling to normalize the data.

## Feature Selection

1. Dropped unique and constant features.
2. Checked correlation with a heatmap.
3. Checked for duplicates (none found).
4. Applied PCA to reduce dimensionality (selected 25 features).
5. Saved pre-processed data with the target feature.

## Machine Learning Model Creation & Evaluation

1. Defined dependent and independent features.
2. Balanced the data using SMOTE.
3. Split data into training (80%) and testing (20%) sets.

### Algorithms Used:
1. Support Vector Machine (SVM)
2. Random Forest
3. Artificial Neural Network (MLP Classifier)

**Performance:**
- **SVM:** 98.28% accuracy (overfitting observed)
- **Random Forest:** 95.61% accuracy
- **ANN (MLP Classifier):** 95.80% accuracy (selected model)

## Saving Model
Saved the trained model using pickle.

## Tools and Libraries Used:
### Tools:
- Jupyter Notebook

### Libraries:
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scipy
- Sklearn
- Pickle

# Goal 1: Department-Wise Performances

### Plots Used:
1. **Violinplot:** Shows the distribution of data across different departments.
2. **CountPlot:** Shows the count of observations in each categorical bin using bars.

### Insights:
- **Sales:** Higher performance rating for males compared to females.
- **HR:** Females perform better; older employees perform lower.
- **Development:** Consistent level 3 performance across ages and genders.
- **Data Science:** Highest average performance; males perform slightly better.
- **R&D:** Good performance among females.
- **Finance:** Performance decreases with age; males perform better.

# Goal 2: Top 3 Important Factors Affecting Employee Performance

### Important Factors:
1. Employment Environment Satisfaction
2. Employee Salary Hike Percentage
3. Experience Years In Current Role

### Insights:
- **EmpEnvironmentSatisfaction:** Higher levels correlate with better performance.
- **EmpLastSalaryHikePercent:** 11-19% hike correlates with better performance.
- **EmpWorkLifeBalance:** Level 3 shows high performance.

# Goal 3: A Trained Model to Predict Employee Performance

### Selected Model:
- **Artificial Neural Network (MLP Classifier)** with 95.80% accuracy.

# Goal 4: Recommendations to Improve Employee Performance

1. Focus on improving employee environment satisfaction.
2. Provide regular salary hikes.
3. Promote employees every 6 months.
4. Improve work-life balance.
5. Consider hiring more females for HR roles.
6. Pay attention to employees with lower job and relationship satisfaction but high performance.

## Conclusion:
The project successfully identifies key factors affecting employee performance, provides a reliable predictive model, and offers actionable recommendations to improve performance across departments.

