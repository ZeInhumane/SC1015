# HR Employment Attrition and Monthly Income Analysis

## As part of SC1015 Mini-Project
Lab Group FR1 Group 1

Chan Jin How Matthew U2323106J

Darren Tan Kai Jen U2323995J

## Background
In this competitive job market, there are many factors which can impact people's outcomes of finding a job, whether they can survive in that job, whether they are able to cope with the income, etc. These days, we keep seeing new articles of not just any random company, but big name comapines like Google and SEA Group retrenching employees suddenly. 

According to the Straits Times, retrenchment rate has been on the rise in recent years.
(https://www.straitstimes.com/singapore/singapore-resident-employment-rebounded-in-2024-with-fewer-retrenchments-mom)

Graduates are not having a good time either. Many of them are unable to find a job.
(https://www.straitstimes.com/singapore/fewer-uni-graduates-in-2024-found-full-time-work-though-more-had-higher-pay-survey)
(https://www.straitstimes.com/singapore/fewer-fresh-poly-grads-secure-full-time-jobs-in-2024-after-graduation-but-take-home-higher-pay)
On a good note, incomes have been increasing, which we also see during our Exploratory Data Analysis later.

Employment is still a big headache to many. This is despite advances in education quality in today's modern, digital age. Everybody wants a higher salary. Everybody also wants to be in a job that not only pays well, but also perform job roles which they enjoy.

## Problem Statement
What factors significantly influence employment outcomes amid a more competitive job market?

## Objective
This project investigates the factors that affects job attrition and income. We use the **Employee Attrition Dataset** by IBM.

The dataset contains data of individuals, including a myraid of factors, not limited to education level, education field, job satisfaction and even performance ratings. It also comes with their Monthly Income, and their attrition status, which will be our target variables for our model.

Our objective is to find out which of such factors are influential in affecting attrition and income, and hence make recommendations to job seekers on what to focus on.

## Dataset
The dataset can be accessed here:  
[Credits to @nelson-wu for the dataset, our DSAI project is not based on his ml project on his repository.](https://github.com/nelson-wu/employee-attrition-ml/blob/master/WA_Fn-UseC_-HR-Employee-Attrition.csv)

Key features in the dataset:
| **Variable**                | **Description**                                                                 |
|----------------------------|---------------------------------------------------------------------------------|
| Age                        | Age of the employee                                                            |
| Attrition                  | Whether the employee has left the company (Yes/No)                             |
| BusinessTravel             | Frequency of business travel                                                   |
| DailyRate                  | Daily rate of the employee                                                     |
| Department                 | Department in which the employee works                                         |
| DistanceFromHome          | Distance between employee's home and workplace                                 |
| Education                  | Education level (1 = Below College, 5 = Doctor)                                |
| EducationField             | Field of study                                                                 |
| EmployeeCount              | Headcount value (constant, typically 1 per row)                                |
| EmployeeNumber             | Unique ID assigned to each employee                                            |
| EnvironmentSatisfaction    | Satisfaction with the work environment (1–4 scale)                             |
| Gender                     | Gender of the employee                                                         |
| HourlyRate                 | Hourly wage                                                                    |
| JobInvolvement             | Level of job involvement (1–4 scale)                                           |
| JobLevel                   | Job level (seniority or pay grade)                                             |
| JobRole                    | Role or job title                                                              |
| JobSatisfaction            | Job satisfaction level (1–4 scale)                                             |
| MaritalStatus              | Marital status of the employee                                                 |
| MonthlyIncome              | Monthly income                                                                 |
| MonthlyRate                | Monthly rate                                                                   |
| NumCompaniesWorked         | Number of companies the employee has worked at                                 |
| Over18                     | Whether the employee is over 18 (typically constant = 'Y')                     |
| OverTime                   | Whether the employee works overtime (Yes/No)                                   |
| PercentSalaryHike          | Percentage increase in salary                                                  |
| PerformanceRating          | Performance rating (1–4 scale)                                                 |
| RelationshipSatisfaction   | Satisfaction with relationships at work (1–4 scale)                            |
| StandardHours              | Standard work hours (usually constant, e.g., 40)                               |
| StockOptionLevel           | Stock option level (0–3)                                                       |
| TotalWorkingYears          | Total years of professional experience                                         |
| TrainingTimesLastYear      | Number of training sessions attended last year                                 |
| WorkLifeBalance            | Work-life balance rating (1–4 scale)                                           |
| YearsAtCompany             | Total number of years at the company                                           |
| YearsInCurrentRole         | Years in current role                                                          |
| YearsSinceLastPromotion    | Years since last promotion                                                     |
| YearsWithCurrManager       | Years with current manager                                                     |
| TenureBucket               | Categorical tenure grouping (bucketed years at company)                        |


## Team Roles
The project is divided into two main roles:

### Person A: Data Preprocessing and Exploratory Data Analysis (EDA)
- Clean and preprocess the dataset.
- Perform exploratory data analysis to uncover trends and relationships.
- Visualize key insights (e.g., heatmap to see which factors have high correlations with our response variable).

### Person B: Machine Learning Modeling & Evaluation
- Build predictive models for:
  - **Attrition**: Binary classification.
  - **MonthlyIncome**: Regression 
- Evaluate model performance using appropriate metrics (R²,Mean Absolute Error, Mean Squared Error).
- Interpret results and draw conclusions.

## Key Tasks
1. **Data Preprocessing**:
   - Handle missing values. (Which we found to have none.)
   - Encode categorical variables (We did it through a one hot encoder, which occured during the model training actually).
   - Normalize/standardize numerical features. (For non tree based models, which actually happened during model traning again.)

2. **Exploratory Data Analysis**:
   - Analyze distributions with use of heatmaps, boxplots, histograms etc.
   - Compare outcomes.
   - Identify correlations between features.

3. **Machine Learning Modeling**:
   - Split data into training and testing sets.
   - Train models for:
     - Predicting attrition (binary classification).
     - Predicting monthly income (regression).
   - Evaluate models.

4. **Results and Insights**:
   - Summarize findings.
   - Provide actionable insights for stakeholders (e.g., students, retrenched job seekers).

## Requirements
To run the code, ensure you have the following Python libraries installed:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Install dependencies using:
```bash
pip install -r requirements.txt
