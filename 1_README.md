# **Overview**

- In this project, we solve a commonly faced problem by **HR professionals** which is **employees insufficient capacity due to excessive absenteeism**.

- So, we built a **logistic regression ML model** to predict the **probability of excessive absenteeism**.

- Having predicted the **probability of excessive absenteeism**, **HR professionals** will be enabled to **manage the employees capacity more effictively**.



# **Environment** & **Packages**

| Package Name | Functionality                 |
|--------------|-------------------------------|
| Pandas       | Data Manipulation             |
| numpy        | Numerical Calculations & Array Manipulations   |
| matplotlib         | Data visualization           |
| sklearn | ML requirements                 |
| pickle     | Saving models and scalers                 |




# **Data Sources**

- [Emplyee Absenteeism Raw Data](https://github.com/Ayman947/HR-LogisticRegression-PredictingAbsenteeism/blob/main/Data-Files/1_absenteeism_data.csv)
| Field    |     Description                                                               | Sample Values |
|----------------|---------------------------------------------------------------------------------------|---------------|
| ID    | Employee ID number|  123             |
| Reason for absence      | Abstract Numbers for absence reasons | 2, 4 or 26              |
| Date          | The date of absence | 07/07/2015	              |
| Transportation Expense | The commuting expenses from home to work in a specific currency                                          | 60               |
| Distance to Work       | The distance from home to work in kilometers                |  22              |
| Age            | The employee age                                                                       |    32           |
| Daily Work Load Average      | The average time of daily work measured in minutes                                                                |        226       |
| Body Mass Index         | A metric the indicate the overall employee's health                                                               |     24 |
Education |Encoded Numbers for educational levels: High School, BSc, MSc and PhD. | 1|
| Children | No. of employee's children | 2 |
| Pets | No. of pets an employee has | 3 |
| Absenteeism Time in Hours | The amount of absenteeism in hours | 1 |



# **Data Cleansning & Preprocessing**

- Dropping the unneeded columns.
- Getting dummies of all categorical columns.
- Concatenating dummies and dropping the baselines.
- Renaming and reordering the columns.
- Converting the date column into a datetime object.
- Extracting month and day of week from the date column.
- Scaling inputs.
- Split the data into train and test datasets.
- Backeliminate columns after training the model.


# **Modeling**

- We've built a **logistic ML model** to predict **excessive absenteeism probability**.

- Our model's accuracy is **73.57 %** (i.e For every 100 predictions, there are 74 predictions are true.)

- ![Confusion Matrix](https://github.com/Ayman947/HR-LogisticRegression-PredictingAbsenteeism/blob/main/Data-Files/Confusion-matrix.PNG)
- ![Inputs Odds Ratio](https://github.com/Ayman947/HR-LogisticRegression-PredictingAbsenteeism/blob/main/Data-Files/Input-odds.PNG)



# **Final Results**

- [Predicts Of New Data](https://github.com/Ayman947/HR-LogisticRegression-PredictingAbsenteeism/blob/main/Data-Files/Predictions.csv)
- [Excessive Absenteeism Predictors Dashboard](https://public.tableau.com/app/profile/ayman.el.taweel/viz/AbsenteeismDashboard_16279048897150/ExcessiveAbsenteeismDashboard)

