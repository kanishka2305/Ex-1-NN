<H3>ENTER YOUR NAME</H3>Kanishka V S
<H3>ENTER YOUR REGISTER NO.</H3> 212222230061
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
### importing libraries:
```py
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
```
### Reading the dataset:
```py
df=pd.read_csv("/content/Churn_Modelling.csv", index_col="RowNumber")
df
```
### Dropping the unwanted Columns:
```py
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df
```
### Checking for null values:
```py
df.isnull().sum()
```
### Checking for duplicate values:
```py
df.duplicated()
```
### Describing the dataset:
```py
df.describe()
```
### Scaling the dataset:
```py
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1
```
### Allocating X and Y attributes:
```py
x=df1.iloc[:,:-1].values
x
y=df1.iloc[:,-1].values
y
```
### Splitting the data into training and testing dataset:
```py
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
```


## OUTPUT:
### DATASET:
![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/d0ce7824-e82c-4024-80f9-6df1ef4daf6e)

### DROPPING THE UNWANTED DATASET:
![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/03a6cbbe-d10c-4ceb-a97a-cfe752017b29)

### CHECKING NULL VALUES:
![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/767bd5f5-a4dd-44b3-99ce-f4b8316d5da1)

### CHECKING FOR DUPLICATION:
![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/865077ff-ee7b-46b0-8200-9378ea4b3048)

### DESCRIBING THE DATASET:

![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/e36f5fa2-e7bd-4eb1-9d66-62ee4ba9b9d1)


### SCALING THE DATASET:
![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/9cc2aaaf-4dc2-43a4-adfc-50699860c8ca)

### X FEATURES:
![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/b0bd9e2e-c6f9-4acc-b0c1-46c6abe4dca1)

### Y FEATURES:
![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/017463b7-4f39-4ddc-8363-f5e4985c9d35)


### SPLITTING THE TRAINING AND TESTING DATASET:
![image](https://github.com/kanishka2305/Ex-1-NN/assets/113497357/7cea33d1-fcae-4610-bdb7-d206d0217a45)


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


