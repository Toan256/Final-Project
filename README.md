# GRADUATION PROJECT
## 1.	Research goal
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

## 8.	Key insights
**Age**: Our analysis reveals that as individuals age, their salary tends to decrease slightly after a certain point, which may reflect a market preference for younger employees in certain industries or roles.

**Gender**: The data indicates a gender wage gap, with males earning significantly more than females on average, highlighting ongoing disparities in the workplace.

**Education** Level: Higher education levels are strongly correlated with higher salaries, underscoring the importance of educational attainment in career advancement.

**Years of Experience**: Experience is a critical determinant of salary, with each additional year of experience leading to a substantial increase in earnings.

**Job Level**: Promotions and higher job levels contribute positively to salary, emphasizing the value of career progression.

**Job Field**: Certain job fields are associated with lower salaries, which may reflect differences in industry standards or demand for specific skills.

## 9.	Hypotheses based on insights
**1. Age and Salary**: There is a negative relationship between age and salary after a certain age, indicating that salaries tend to decrease as employees get older beyond a specific age threshold.

**2. Gender and Salary**: Males, on average, earn a higher salary than females, reflecting a gender wage gap in the dataset.

**3. Education Level and Salary**: Higher education levels are positively correlated with higher salaries, meaning individuals with more advanced degrees tend to earn more.

**4. Years of Experience and Salary**: There is a positive relationship between years of experience and salary, where each additional year of experience leads to an increase in earnings.

**5. Job Level and Salary**: Higher job levels are associated with higher salaries, suggesting that promotions and advancement in job hierarchy result in increased earnings.

**6. Job Field and Salary**: Certain job fields are associated with lower salaries, implying that the industry or sector in which an individual works significantly impacts their earning potential.

**7. Interaction Between Variables**: The effect of education level on salary is moderated by years of experience, meaning that the salary increase associated with higher education is more pronounced for individuals with more experience.

## 10.	Recommendations based on analysis results
**Pursue Higher Education:** Investing in further education can significantly boost earning potential, as higher education levels are strongly linked to higher salaries.

**Gain More Experience:** Accumulating years of relevant experience is crucial for increasing salary, making continuous skill development and career longevity important.

**Seek Promotions:** Actively pursuing higher job levels and responsibilities can lead to higher salaries, emphasizing the importance of career growth and advancement.

**Choose High-Demand Fields:** Selecting or transitioning to fields with higher salary potential can also be a strategic move for individuals looking to improve their earnings.

