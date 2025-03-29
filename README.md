# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns 
df=pd.read_csv("/content/titanic_dataset.csv")
df
```

![364725871-988efb87-c540-48fd-a6d0-fe33f5e57b75](https://github.com/user-attachments/assets/21339e06-5e8b-491f-a1b4-d110d07a5402)

## df.info()
![364726097-e1f49bca-e714-417b-ae4a-7b2ce3709324](https://github.com/user-attachments/assets/121202e2-3d76-437d-b822-40fce964836a)

## df.shape
![364726261-97d9098e-8c3c-4f7b-b8ef-fe4400699aaa](https://github.com/user-attachments/assets/226e59af-8278-4c9f-ae6d-15ee74634e59)

## df.describe()
![364726336-1307157c-e110-4aea-a95a-fa4ca9f148f7](https://github.com/user-attachments/assets/0cb82c3a-74d6-4495-a7e4-cb2243020dda)

## df.set_index("PassengerId",inplace=True)
## df.describe()
![364726470-07936145-b19b-4821-ad42-5606a461f776](https://github.com/user-attachments/assets/c4488e10-026c-42ad-a59a-47c3cc864bf3)

## df.nunique()
![364726552-9e50613d-0c97-4831-aa9d-21cad20d5176](https://github.com/user-attachments/assets/ca6f5e74-c356-43ba-9ded-8feed5ea9b92)

## df["Survived"].value_counts()
![364726691-710015ce-7fb3-444c-8559-fdd48203ee3e](https://github.com/user-attachments/assets/da28bfae-0428-4077-9c8f-41c1d3034579)

## per=(df["Survived"].value_counts(normalize=true)

![364728450-002bd98c-11d4-40cb-b4c6-395467601517](https://github.com/user-attachments/assets/19e2ac92-6e4a-47c6-9d16-871b2f2dc1f1)

## sns.countplot(data=df,x="Survived")
![364728631-af255087-2259-43c4-9b33-9dfb90dcaf38](https://github.com/user-attachments/assets/c75b02be-43d4-4d69-be2b-55d73a18fbd9)

## df.Pclass.unique()
![364728714-f173fde1-71ae-4faa-8cb5-d66e505df39b](https://github.com/user-attachments/assets/220db27e-4c2f-4ced-a64f-2b11fb2a573c)

## df.rename(columns= {'Sex':'Gender'}, inplace=True)
![364728819-66fa890b-add4-4f7e-80fb-ca9525800c52](https://github.com/user-attachments/assets/77a74eb4-916d-4985-83bc-fde4b1e5d89f)

## sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)
![364728953-3c673d38-27cc-4c1e-aeaa-990edfc54335](https://github.com/user-attachments/assets/61beef2a-1199-4bab-8df0-577e15f12cb7)

## sns.catplot(x='Survived',hue="Gender",data=df,kind="count")
![364729211-7fd601b0-5dc5-43af-9c8e-bd901a15bbc8](https://github.com/user-attachments/assets/2869afc2-a903-4391-ae0e-eeb8c36bbf31)

 ## df.boxplot(column="Age",by="Survived")
 ![364729329-c0da1927-6181-4b81-9a33-32ddb3ad4ffa](https://github.com/user-attachments/assets/35570470-188d-4ed9-94fa-02a11293e27a)

## sns.scatterplot(x=df["Age"],y=df["Fare"])
![364729454-d66d2beb-f9a5-4bf0-80b0-90c5c56c3bb7](https://github.com/user-attachments/assets/19515897-7616-489e-90eb-e82c06ce16cb)

## sns.jointplot(x="Age",y="Fare",data=df)
![364729581-7ad0241e-12ef-4306-baae-e0e582cdff2b](https://github.com/user-attachments/assets/f3eae183-fd09-4b12-95b2-19f8a4f5799e)

## fig,ax1 = plt.subplots(figsize=(8,5))
 pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Gender',data=df)
 ![364729765-b45ce949-6ad2-4458-8967-83b6a2877359](https://github.com/user-attachments/assets/e8d28f62-a928-4b12-8a35-2150f8258389)


## sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="Count")
![364729887-ac1b5d57-2d66-451a-8134-9d041d46a26b](https://github.com/user-attachments/assets/232cab63-6166-44b4-a554-6facccde03a6)

## corr = df.corr()
sns.heatmap(corr,annot=True)
![364730247-fab28ab5-3ed8-4359-8bf6-6e382a183caf](https://github.com/user-attachments/assets/f600cb76-85ec-48d4-98aa-3630bd41d100)


## sns.pairplot(df)
![364730503-e94d0676-7750-4796-940d-84bd9cba670d](https://github.com/user-attachments/assets/bfa3e06d-0f7d-4bb6-a3fa-c964edfcd539)

# RESULT
Hence performing Exploratory Data Analysis on the given data set is successfully.
