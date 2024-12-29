# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: s.rohith kumar
RegisterNumber:24004371  
*/
```
import chardet

file="spam.csv"

with open(file,'rb') as rawdata:

result = chardet.detect(rawdata.read(100000))

result

import pandas as pd

data = pd.read_csv("spam.csv",encoding='windows-1252')

data.head()

data.isnull().sum()

x=data['v1'].values

y=data['v2'].values

from sklearn.model_selection import train_test_split

x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_st

from sklearn.feature_extraction.text import CountVectorizer

cv=CountVectorizer()

x_train=cv.fit_transform(x_train)

x_test=cv.transform(x_test)

from sklearn.svm import SVC

svc = SVC(kernel='linear')

svc.fit(x_train,y_train)

y_pred=svc.predict(x_test)

y_pred

from sklearn import metrics

accuracy=metrics.accuracy_score(y_pred,y_test)

accuracy

## Output:
![SVM For Spam Mail Detection](sam.png)
![Screenshot (78)](https://github.com/user-attachments/assets/1ca0628d-34a9-4370-a902-1bc4b5a4c9d3)
![Screenshot (79)](https://github.com/user-attachments/assets/82aef8ad-42bc-4927-be65-0a10a78e9827)
![Screenshot (80)](https://github.com/user-attachments/assets/220db180-b207-4200-80da-fb02d5242124)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
