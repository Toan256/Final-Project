# GRADUATION PROJECT
## 1.	Research Overview
The salary of an individual is influenced by various factors. This study aims to explore and analyze the determinants of Vietnamese salary and develop a predictive model based on relevant variables. The independent variables considered in the research include age, gender, education level, years of experience, job level, and job field. The dependent variable is salary. By applying statistical methods and data modeling techniques, the study will assess the impact of each factor on salary and propose an effective salary prediction model. The findings of this research can provide valuable insights for individuals, employers, and policymakers in making informed decisions regarding compensation.

## 2.	Research objective
This study specifies three main objectives, including:
(1) Examining the factors that influence salary levels.
(2) Proposing a model for predicting salary.
(3) Suggesting methods for individuals to improve their salary.

## 3.	Research question
What factors influence salary, and how do they impact it?

## 4.	Research scope
Data of Vietnamese workforce in 2023 from multiple sources, including surveys, job posting sites, and other publicly available sources. A total of 6698 data points were collected.The dataset included fivevariables: age, experience, job role, and education level and salary.
Original data source: https://docs.google.com/spreadsheets/d/1O45dk0h5SaVkq5VVn4_dVp11rkNXVY6ziwdbkOxX9h8/edit?usp=sharing
| Age | Gender | Education Level   | Job Title                             | Years of Experience | Salary  |
|-----|--------|-------------------|---------------------------------------|---------------------|---------|
| 32  | Male   | Bachelor's        | Software Engineer                     | 5                   | 9000    |
| 28  | Female | Master's          | Data Analyst                          | 3                   | 6500    |
| 45  | Male   | PhD               | Senior Manager                        | 15                  | 15000   |
| 36  | Female | Bachelor's        | Sales Associate                       | 7                   | 6000    |
| 52  | Male   | Master's          | Director                              | 20                  | 20000   |
| 29  | Male   | Bachelor's        | Marketing Analyst                     | 2                   | 5500    |

Cleaned data source: https://docs.google.com/spreadsheets/d/1v_P_q5EWeNMHFTpal7MgBTVpdouhhXRARNxMOcmCiWU/edit?usp=sharing
| Age | Gender | Education Level | Years of Experience | level | field | Salary  |
|-----|--------|-----------------|---------------------|-------|-------|---------|
| 32  | 1      | 2               | 5                   | 2     | 1     | 9000    |
| 28  | 0      | 3               | 3                   | 2     | 2     | 6500    |
| 45  | 1      | 4               | 15                  | 9     | 3     | 15000   |
| 36  | 0      | 2               | 7                   | 2     | 4     | 6000    |
| 52  | 1      | 3               | 20                  | 10    | 3     | 20000   |
| 29  | 1      | 2               | 2                   | 2     | 5     | 5500    |
| 42  | 0      | 3               | 12                  | 8     | 6     | 12000   |

## 5.	Research object
This research examines the factors affecting Vietnamese labor’s salary

## 6.	Scientific contribution
Scientifically, research has contributed three fundamental meanings.
(1) This study confirmed the elements that have effects on Vietnamese income
(2) This was one of the most recent studies on Vietnamese Salary.
(3) This study can be used as a starting point for further research.

## 7.	Technologies
The research begins with data cleaning, which is performed using Google Sheets to ensure accuracy and consistency in the dataset. After cleaning, the data is analyzed using correlation analysis and linear regression. The correlation analysis helps identify relationships between the independent variables (such as age, gender, education level, years of experience, job level, and job field) and the dependent variable (salary). Linear regression is then conducted using Python's Pandas library to quantify these relationships and develop a predictive model for salary.
