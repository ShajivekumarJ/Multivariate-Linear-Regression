# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import Pandas and Scikit-learn and load the carsemission.csv dataset.
### Step2
Select Weight and Volume as independent variables and CO2 as the dependent variable.
### Step3
Create and train the Multivariate Linear Regression model.
### Step4
Display the regression coefficients and intercept.
### Step5
Predict and display CO₂ emission for Weight = 3300 and Volume = 1300.
## Program:
```py

# NAME : SHAJIVE KUMAR J
# REG NO : 212225230258

# Dataset Setup - Run this cell before starting the experiment

import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")

import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:

### Insert your output

<img width="1082" height="508" alt="Screenshot 2026-09-06 223808" src="https://github.com/user-attachments/assets/5a93140a-8642-4a10-9850-6853e0f6210a" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
