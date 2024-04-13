# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE
```
 import pandas as pd
 df=pd.read_csv("/content/Data_set .csv")
 df
 df.head(10)
 df.info()
 df.isnull()
 df.isnull().sum()
 df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
 df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
 df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
 df.head()
 df['rating']=df['rating'].fillna(df['rating'].mean())
 df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean
 df.head()
 df['watchers']=df['watchers'].fillna(df['watchers'].median())
 df.head()
 df.info()
 df.isnull().sum()
```
#  OUTPUT

![310740569-e4dd3206-39fc-43b4-83aa-5cc7e7f3fdee](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/f8176ad3-162f-4e07-a39b-5fd381525d1e)

![310740614-e3bfb971-4f37-4232-9354-ddbb82eda8c9](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/cfd2d8e6-eada-4901-b634-d5d387bba60c)

![310740686-2b5c794a-0f11-43a4-9529-1f8ce5cf3f2e](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/ba4bff05-5bdc-4dc8-bec8-674003c2a5aa)

![310740887-b6cb3f0b-4e13-4dcc-9ae8-38d746f39cb8](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/d911f2bc-39d2-467e-bd31-82e83c099591)

![310740951-5584adf2-5eeb-406f-8ee8-191f2736e22a](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/9a05ba09-c6ce-4dfe-83f4-1a17442387d0)

![310741004-36a39d7d-fb1b-4697-9e9f-ec96dc3f2007](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/52e73565-f456-4241-a6c3-d94bd22e6384)

![310741025-a7b68596-c6b3-456d-ab77-61fea5fafb50](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/eb071262-eb59-42e5-9ef8-a402c764c756)

![310741087-8a976467-021b-4ffb-a79e-42cda7cee00d](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/a0a32ca4-b7ab-4611-9a7d-16be03ed27f0)

![310741158-0473d45f-e910-4!324-aad6-7b878907df60](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/ff85512f-4eab-400d-936d-4e8e7a205f01)

![310741278-fc100e71-c851-4738-a6db-20b99952bdbb](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/7ec27e08-0268-45b5-8b2c-68ef1aa73368)

![310741328-f68b6d74-5344-4ca8-be2f-3b17bce90121](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/2ddb61a6-0880-48f1-8d4e-9dce2a161090)

![310741362-12d4bad2-ffd2-431d-9499-bbc458278d36](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/a6f9b7a1-84f7-413b-ad5b-fdae5e0c8ace)

![310741402-dfa6dfda-beaf-4526-ad2f-3e3ce8366478](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/13307b4d-a42d-4b3f-99aa-adbe7f16ba48)

![310741435-500bcfc5-be2d-4172-94a7-f04422a092fe](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/d3241d23-e846-492a-af49-89ce412a3559)

![310741402-dfa6dfda-beaf-4526-ad2f-3e3ce8366478](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/471f9a4a-a9df-43af-a441-1b06c79038b9)

![310741924-95ecfb40-c36b-4d77-a62d-46235ebf9a94](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/a9dabcc5-9386-4976-acaf-f6519c6de436)

![310742019-3ad59f36-b6d9-4a6f-9200-8f7220ba5183](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/266254be-39a2-447a-a350-3cfbbb1f0745)
## 2)Outlier Detection and Removal:
To read a given dataset and remove outliers and save a new dataframe.
## ALGORITHM:
1) Remove outliers using IQR

(2) After removing outliers in step 1, you get a new dataframe.

(3) use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result

(4) for the data set height_weight.csv find the following

(i) Using IQR detect weight outliers and print them

(ii) Using IQR, detect height outliers and print them

## PROGRAM :
```
  import pandas as pd
  import numpy as np
  import seaborn as sns
  import pandas as pd
  from scipy import stats
  df = pd.read_csv("/content/heights.csv")
  sns.boxplot(data=df)
  sns.scatterplot(data=df)
  max =df['height'].quantile(0.90)
  min =df['height'].quantile(0.15)
  max
  min
  dq = df[((df['height']>=min)&(df['height']<=max))]
  dq
  low = min-1.5*iqr
  high = max+1.5*iqr
  dq = df[((df['height']>=min)&(df['height']<=max))]
  dq
```
## ZSCORE:
```
  import pandas as pd
  import numpy as np
  import seaborn as sns
  import pandas as pd
  from scipy import stats
  data = {'weight':[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}
  df = pd.DataFrame(data)
  df
  sns.boxplot(data=df)
  z = np.abs(stats.zscore(df))
  print(df[z['weight']>3])
  val =[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]
  out=[]
  def d_o(val):
  ts=3
  m=np.mean(val)
  sd=np.std(val)    
  for i in val:
  z=(i-m)/sd
  if np.abs(z)>ts:
  out.append(i)
  return out
  op = d_o(val)
  op
```
## OUTPUT :

![310743822-d3414cc1-7d2e-4261-886a-f8e23854e7bf](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/ebba643e-6e79-4309-895a-3a99050e6e4a)

![310744349-c1d105e1-5e56-433d-b0aa-9c0a78dcea7f](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/e25964de-f3bb-4081-a1a4-ef6b8671dd7d)

![310744374-b4b7dada-45c3-463a-8380-44df29c1a6fc](https://github.com/AdhithiyanK/ODD2023-Datascience-Ex01/assets/121029258/bba3e660-ca18-434e-abc7-52b75ba21d99)

## RESULT :
Thus, the given data is read, cleansed and the cleaned data is saved into the file and the given data is read,remove outliers and save a new dataframe was created and executed successfully.
