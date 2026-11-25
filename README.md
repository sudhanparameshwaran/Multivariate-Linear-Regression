# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>Start the program and import the required libraries, Pandas and Scikit-learn

### Step2
<br>Load the car emission dataset from the GitHub URL and save it as a CSV file.

### Step3
<br>Read the dataset and separate the input features (Weight, Volume) and output variable (CO2).

### Step4
<br>Create and train a Linear Regression model using the dataset, then calculate the coefficients and intercept.

### Step5
<br>Give the input values (Weight = 3300, Volume = 1300) and predict the CO2 emission using the trained model.

## Program:
```
developed by: Sudhan P
register number: 26019297
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
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/735282a7-3f55-43ed-8266-d761a612ed04" />


<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
