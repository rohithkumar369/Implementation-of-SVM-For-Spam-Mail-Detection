# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
 1.Import pandas and matplotlib.pyplot
 
 2.Read the dataset and transform it
 
 3.Import KMeans and fit the data in the model
 
 4.Plot the Cluster graph 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..

Developed by: s.rohith kumar

RegisterNumber:  24004371
*/
import chardet

file="spam.csv"

with open(file,'rb')	as	rawdata:

 result = chardet.detect(rawdata.read(100000))

 result

 import pandas as pd

 data = pd.read_csv("spam.csv",encoding='windows-1252')

 data.head()

data.info()

data.isnull().sum()

 x	=	data['v1'].values

 y	=	data['v2'].values

 from	sklearn.model_selection	import	train_test_split

 x_train,x_test,y_train,y_test	=	train_test_split(x,y,test_size=0.2,random_state=0)

 from	sklearn.feature_extraction.text	import	CountVectorizer

 cv	=	CountVectorizer()
 
 x_train	=	cv.fit_transform(x_train)

 x_test	=	cv.transform(x_test)

 from	sklearn.svm	import	SVC

 svc	=	SVC(kernel	=	'linear')

 svc.fit(x_train,y_train)

 y_pred	=	svc.predict(x_test)

 y_pred

## Output:
![SVM For Spam Mail Detection](sam.png)
![Screenshot (62)](https://github.com/user-attachments/assets/6e0e521d-41a5-480c-b8ad-5ff3ecc90ba6)
5d96c2ecb701)
![Screenshot (63)](https://github.com/user-attachments/assets/f59a8317-0c2a-489a-97a6-09e29deb8961)
![Screenshot (64)](https://github.com/user-attachments/assets/3057d386-9724-4ca2-9c76-87383fc31619)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
