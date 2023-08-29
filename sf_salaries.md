```python
# read the data set
import pandas as pd
x=pd.read_csv("C:/Users/admin/Downloads/Sf_Salaries.csv",encoding='ISO-8859-1')
x
```

    C:\Users\admin\AppData\Local\Temp\ipykernel_14976\3522904041.py:3: DtypeWarning: Columns (3,4,5,6,12) have mixed types. Specify dtype option on import or set low_memory=False.
      x=pd.read_csv("C:/Users/admin/Downloads/Sf_Salaries.csv",encoding='ISO-8859-1')
    




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Id</th>
      <th>EmployeeName</th>
      <th>JobTitle</th>
      <th>BasePay</th>
      <th>OvertimePay</th>
      <th>OtherPay</th>
      <th>Benefits</th>
      <th>TotalPay</th>
      <th>TotalPayBenefits</th>
      <th>Year</th>
      <th>Notes</th>
      <th>Agency</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>NATHANIEL FORD</td>
      <td>GENERAL MANAGER-METROPOLITAN TRANSIT AUTHORITY</td>
      <td>167411.18</td>
      <td>0.0</td>
      <td>400184.25</td>
      <td>NaN</td>
      <td>567595.43</td>
      <td>567595.43</td>
      <td>2011</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>GARY JIMENEZ</td>
      <td>CAPTAIN III (POLICE DEPARTMENT)</td>
      <td>155966.02</td>
      <td>245131.88</td>
      <td>137811.38</td>
      <td>NaN</td>
      <td>538909.28</td>
      <td>538909.28</td>
      <td>2011</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>ALBERT PARDINI</td>
      <td>CAPTAIN III (POLICE DEPARTMENT)</td>
      <td>212739.13</td>
      <td>106088.18</td>
      <td>16452.6</td>
      <td>NaN</td>
      <td>335279.91</td>
      <td>335279.91</td>
      <td>2011</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>CHRISTOPHER CHONG</td>
      <td>WIRE ROPE CABLE MAINTENANCE MECHANIC</td>
      <td>77916.0</td>
      <td>56120.71</td>
      <td>198306.9</td>
      <td>NaN</td>
      <td>332343.61</td>
      <td>332343.61</td>
      <td>2011</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>PATRICK GARDNER</td>
      <td>DEPUTY CHIEF OF DEPARTMENT,(FIRE DEPARTMENT)</td>
      <td>134401.6</td>
      <td>9737.0</td>
      <td>182234.59</td>
      <td>NaN</td>
      <td>326373.19</td>
      <td>326373.19</td>
      <td>2011</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>148649</th>
      <td>148650</td>
      <td>Roy I Tillery</td>
      <td>Custodian</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>2014</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>PT</td>
    </tr>
    <tr>
      <th>148650</th>
      <td>148651</td>
      <td>Not provided</td>
      <td>Not provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>2014</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>148651</th>
      <td>148652</td>
      <td>Not provided</td>
      <td>Not provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>2014</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>148652</th>
      <td>148653</td>
      <td>Not provided</td>
      <td>Not provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>Not Provided</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>2014</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>148653</th>
      <td>148654</td>
      <td>Joe Lopez</td>
      <td>Counselor, Log Cabin Ranch</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>-618.13</td>
      <td>0.00</td>
      <td>-618.13</td>
      <td>-618.13</td>
      <td>2014</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>PT</td>
    </tr>
  </tbody>
</table>
<p>148654 rows × 13 columns</p>
</div>




```python
# find the information
x.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 148654 entries, 0 to 148653
    Data columns (total 13 columns):
     #   Column            Non-Null Count   Dtype  
    ---  ------            --------------   -----  
     0   Id                148654 non-null  int64  
     1   EmployeeName      148654 non-null  object 
     2   JobTitle          148654 non-null  object 
     3   BasePay           148049 non-null  object 
     4   OvertimePay       148654 non-null  object 
     5   OtherPay          148654 non-null  object 
     6   Benefits          112495 non-null  object 
     7   TotalPay          148654 non-null  float64
     8   TotalPayBenefits  148654 non-null  float64
     9   Year              148654 non-null  int64  
     10  Notes             0 non-null       float64
     11  Agency            148654 non-null  object 
     12  Status            38119 non-null   object 
    dtypes: float64(3), int64(2), object(8)
    memory usage: 14.7+ MB
    


```python
# What is the average on BasePay
x['BasePay'].mean

```




    <bound method NDFrame._add_numeric_operations.<locals>.mean of 0            167411.18
    1            155966.02
    2            212739.13
    3              77916.0
    4             134401.6
                  ...     
    148649            0.00
    148650    Not Provided
    148651    Not Provided
    148652    Not Provided
    148653            0.00
    Name: BasePay, Length: 148654, dtype: object>




```python
# What is the highest amount of OvertimePay in dataset
x['OvertimePay'].max
```




    <bound method NDFrame._add_numeric_operations.<locals>.max of 0                  0.0
    1            245131.88
    2            106088.18
    3             56120.71
    4               9737.0
                  ...     
    148649            0.00
    148650    Not Provided
    148651    Not Provided
    148652    Not Provided
    148653            0.00
    Name: OvertimePay, Length: 148654, dtype: object>




```python
# What is the Job Tile of JOSEPH DRISCOLL
x[x['EmployeeName']=='JOSEPH DRISCOLL']['JobTitle']
```




    24    CAPTAIN, FIRE SUPPRESSION
    Name: JobTitle, dtype: object




```python
# How much does JOSEPH DRISCOLL make(Including Benefits)
x[x['EmployeeName']=='JOSEPH DRISCOLL']['TotalPayBenefits']

```




    24    270324.91
    Name: TotalPayBenefits, dtype: float64




```python
# What is the name of highest paid person(Including benefits)
x[x['TotalPayBenefits']==x['TotalPayBenefits'].max()]

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Id</th>
      <th>EmployeeName</th>
      <th>JobTitle</th>
      <th>BasePay</th>
      <th>OvertimePay</th>
      <th>OtherPay</th>
      <th>Benefits</th>
      <th>TotalPay</th>
      <th>TotalPayBenefits</th>
      <th>Year</th>
      <th>Notes</th>
      <th>Agency</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>NATHANIEL FORD</td>
      <td>GENERAL MANAGER-METROPOLITAN TRANSIT AUTHORITY</td>
      <td>167411.18</td>
      <td>0.0</td>
      <td>400184.25</td>
      <td>NaN</td>
      <td>567595.43</td>
      <td>567595.43</td>
      <td>2011</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
# What is the name of lowest paid person(Including benefits)
x[x['TotalPayBenefits']==x['TotalPayBenefits'].min()]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Id</th>
      <th>EmployeeName</th>
      <th>JobTitle</th>
      <th>BasePay</th>
      <th>OvertimePay</th>
      <th>OtherPay</th>
      <th>Benefits</th>
      <th>TotalPay</th>
      <th>TotalPayBenefits</th>
      <th>Year</th>
      <th>Notes</th>
      <th>Agency</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>148653</th>
      <td>148654</td>
      <td>Joe Lopez</td>
      <td>Counselor, Log Cabin Ranch</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>-618.13</td>
      <td>0.00</td>
      <td>-618.13</td>
      <td>-618.13</td>
      <td>2014</td>
      <td>NaN</td>
      <td>San Francisco</td>
      <td>PT</td>
    </tr>
  </tbody>
</table>
</div>




```python
# What was the average(mean) BasePay of all employess per year ? (2011 - 2014) 
y=x.groupby('BasePay')['Year'].mean()
y
```




    BasePay
    -166.01         2012.0
    -121.63         2012.0
    -109.22         2012.0
    -106.6          2012.0
    -101.88         2012.0
                     ...  
    9991.53         2014.0
    9997.15         2014.0
    9998.60         2014.0
    9999.59         2014.0
    Not Provided    2014.0
    Name: Year, Length: 109900, dtype: float64




```python
# How many Unique Job Tiles are there
x['JobTitle'].nunique()
```




    2159




```python
# What are the top 5 most common jobs
x["JobTitle"].value_counts().head(5)
```




    Transit Operator                7036
    Special Nurse                   4389
    Registered Nurse                3736
    Public Svc Aide-Public Works    2518
    Police Officer 3                2421
    Name: JobTitle, dtype: int64




