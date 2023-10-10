# DS_exp3
# Ex03-Univariate-Analysis
# AIM:
To read the given data and perform the univariate analysis with different types of plots.

# EXPLAINATION:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

# ALGORITHM:
Step1:Read the given data set using standard libraries.

Step2:Get the information about the data.

Step3:Remove the null values from the data.

Step4:Mention the datatypes from the data.

Step5:Count the values from the data.

Step6:Do plots like sepallength,species,sepalwidth.

# PROGRAM
```
import pandas as pd import numpy as np import matplotlib.pyplot as plt import seaborn as sns

df=pd.read_csv("/content/iris.csv")

df.head()

df.tail()

df.nunique()

df.iloc[:,4].value_counts()

for i in range(0,df.shape[1]): print("-----------",df.columns[i],"------------") print(df.iloc[:,i].value_counts()) print("---------------------------------------")

sns.countplot(x='species',data=df)

dfv=df.loc[df['species']=='virginica']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*') plt.xlabel('sepal length') plt.show() ##plt.plot(df_setosa['sepal_length'],np.zeros_like(df_setosa['sepal_length']),'o')

dfs=df.loc[df['species']=='setosa'] dfc=df.loc[df['species']=='versicolor']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o') plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+') plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-') plt.xlabel('SEPALLENGTH') plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_width","sepal_width").add_legend(); plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_length","sepal_length").add_legend(); plt.show()

sns.pairplot(df,hue="species",size=3)
```

# OUPTUT:
![image](https://github.com/Leela1822/DS_exp3/assets/106167639/2cb45994-a388-4d45-865d-7f991c653e4e)


![image](https://github.com/Leela1822/DS_exp3/assets/106167639/f0cf4cf5-4517-44e9-904c-5a2a97a71256)



![image](https://github.com/Leela1822/DS_exp3/assets/106167639/a07f3944-b640-4106-90d7-21bcde9d653a)




![image](https://github.com/Leela1822/DS_exp3/assets/106167639/c45e9e5d-b598-4735-a8c8-8611587ec53c)



![image](https://github.com/Leela1822/DS_exp3/assets/106167639/7996a8de-8eb4-479c-bd22-ee4146192c92)


![image](https://github.com/Leela1822/DS_exp3/assets/106167639/ed372e89-9e87-42a6-aa23-a2cb824b45fa)



![image](https://github.com/Leela1822/DS_exp3/assets/106167639/401492f4-698c-47f0-940d-56e486c014d3)



![image](https://github.com/Leela1822/DS_exp3/assets/106167639/f9e9e489-f70e-41c2-86b0-156daebc576b)




![image](https://github.com/Leela1822/DS_exp3/assets/106167639/de04bff1-ce51-40b4-87e3-acd11f8857e3)


![image](https://github.com/Leela1822/DS_exp3/assets/106167639/c61ab9ce-5657-498b-a64a-cbdc05dc4bd5)



![image](https://github.com/Leela1822/DS_exp3/assets/106167639/ba079e74-3a8c-4dd8-b66a-a654561eb452)


# RESULT:
Thus we have read the given data and performed the univariate analysis with different types of plots are created and verified succesfully.
