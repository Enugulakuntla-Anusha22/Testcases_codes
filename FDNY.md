```python
# import the libraries 
import pandas as pd
# import the FDNY file
df=pd.read_csv("C:/Users/admin/Downloads/14.FDNY.csv",encoding='ISO-8859-1')
df
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
      <th>FacilityName</th>
      <th>FacilityAddress</th>
      <th>Borough</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>FacilityName</td>
      <td>FacilityAddress</td>
      <td>Borough</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Engine 4/Ladder 15</td>
      <td>42 South Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Engine 10/Ladder 10</td>
      <td>124 Liberty Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Engine 6</td>
      <td>49 Beekman Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Engine 7/Ladder 1/Battalion 1/Manhattan Boroug...</td>
      <td>100-104 Duane Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>214</th>
      <td>Engine 162/Ladder 82/Battalion 23</td>
      <td>256 Nelson Avenue</td>
      <td>Staten Island</td>
    </tr>
    <tr>
      <th>215</th>
      <td>Engine 167/Ladder 87</td>
      <td>345 Annadale Road</td>
      <td>Staten Island</td>
    </tr>
    <tr>
      <th>216</th>
      <td>Engine 164/Ladder 84</td>
      <td>1560 Drumgoole Road West</td>
      <td>Staten Island</td>
    </tr>
    <tr>
      <th>217</th>
      <td>Engine 168/EMS Station 23</td>
      <td>1100 Rossville Avenue</td>
      <td>Staten Island</td>
    </tr>
    <tr>
      <th>218</th>
      <td>Engine 151/Ladder 76</td>
      <td>7219 Amboy Road</td>
      <td>Staten Island</td>
    </tr>
  </tbody>
</table>
<p>219 rows × 3 columns</p>
</div>




```python
# view the content info
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 219 entries, 0 to 218
    Data columns (total 3 columns):
     #   Column           Non-Null Count  Dtype 
    ---  ------           --------------  ----- 
     0   FacilityName     219 non-null    object
     1   FacilityAddress  219 non-null    object
     2   Borough          219 non-null    object
    dtypes: object(3)
    memory usage: 5.3+ KB
    


```python
# view the first five records
df.head()
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
      <th>FacilityName</th>
      <th>FacilityAddress</th>
      <th>Borough</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>FacilityName</td>
      <td>FacilityAddress</td>
      <td>Borough</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Engine 4/Ladder 15</td>
      <td>42 South Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Engine 10/Ladder 10</td>
      <td>124 Liberty Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Engine 6</td>
      <td>49 Beekman Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Engine 7/Ladder 1/Battalion 1/Manhattan Boroug...</td>
      <td>100-104 Duane Street</td>
      <td>Manhattan</td>
    </tr>
  </tbody>
</table>
</div>




```python
# skip the duplicate header row
df=pd.read_csv("C:/Users/admin/Downloads/14.FDNY.csv",skiprows=1)
df
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
      <th>FacilityName</th>
      <th>FacilityAddress</th>
      <th>Borough</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Engine 4/Ladder 15</td>
      <td>42 South Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Engine 10/Ladder 10</td>
      <td>124 Liberty Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Engine 6</td>
      <td>49 Beekman Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Engine 7/Ladder 1/Battalion 1/Manhattan Boroug...</td>
      <td>100-104 Duane Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ladder 8</td>
      <td>14 North Moore Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>213</th>
      <td>Engine 162/Ladder 82/Battalion 23</td>
      <td>256 Nelson Avenue</td>
      <td>Staten Island</td>
    </tr>
    <tr>
      <th>214</th>
      <td>Engine 167/Ladder 87</td>
      <td>345 Annadale Road</td>
      <td>Staten Island</td>
    </tr>
    <tr>
      <th>215</th>
      <td>Engine 164/Ladder 84</td>
      <td>1560 Drumgoole Road West</td>
      <td>Staten Island</td>
    </tr>
    <tr>
      <th>216</th>
      <td>Engine 168/EMS Station 23</td>
      <td>1100 Rossville Avenue</td>
      <td>Staten Island</td>
    </tr>
    <tr>
      <th>217</th>
      <td>Engine 151/Ladder 76</td>
      <td>7219 Amboy Road</td>
      <td>Staten Island</td>
    </tr>
  </tbody>
</table>
<p>218 rows × 3 columns</p>
</div>




```python
# verify the dataset is fixed
df.isnull()
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
      <th>FacilityName</th>
      <th>FacilityAddress</th>
      <th>Borough</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>214</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>215</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>216</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>217</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>218</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>219 rows × 3 columns</p>
</div>




```python
# view the data statistics
df.describe()
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
      <th>FacilityName</th>
      <th>FacilityAddress</th>
      <th>Borough</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>219</td>
      <td>219</td>
      <td>219</td>
    </tr>
    <tr>
      <th>unique</th>
      <td>219</td>
      <td>219</td>
      <td>6</td>
    </tr>
    <tr>
      <th>top</th>
      <td>FacilityName</td>
      <td>FacilityAddress</td>
      <td>Brooklyn</td>
    </tr>
    <tr>
      <th>freq</th>
      <td>1</td>
      <td>1</td>
      <td>66</td>
    </tr>
  </tbody>
</table>
</div>




```python
# view the attributes of dataset
x=df.columns
x

```




    Index(['FacilityName', 'FacilityAddress', 'Borough'], dtype='object')




```python
# view the index of dataset
df.iloc()
print(df.index)

```

    RangeIndex(start=0, stop=219, step=1)
    


```python
# count the number of records for each attribute
df.count()
```




    FacilityName       218
    FacilityAddress    218
    Borough            218
    dtype: int64




```python
# view the datatypes of all three attributes
df.dtypes()

```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[13], line 2
          1 # view the datatypes of all three attributes
    ----> 2 df.dtypes()
    

    TypeError: 'Series' object is not callable



```python
# select FDNY information for boroughwise
df.loc[:,"Borough"]
```




    0          Manhattan
    1          Manhattan
    2          Manhattan
    3          Manhattan
    4          Manhattan
               ...      
    213    Staten Island
    214    Staten Island
    215    Staten Island
    216    Staten Island
    217    Staten Island
    Name: Borough, Length: 218, dtype: object




```python
#view FDNY information for each borough
df.groupby("Borough").count()

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
      <th>FacilityName</th>
      <th>FacilityAddress</th>
    </tr>
    <tr>
      <th>Borough</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Bronx</th>
      <td>34</td>
      <td>34</td>
    </tr>
    <tr>
      <th>Brooklyn</th>
      <td>66</td>
      <td>66</td>
    </tr>
    <tr>
      <th>Manhattan</th>
      <td>48</td>
      <td>48</td>
    </tr>
    <tr>
      <th>Queens</th>
      <td>50</td>
      <td>50</td>
    </tr>
    <tr>
      <th>Staten Island</th>
      <td>20</td>
      <td>20</td>
    </tr>
  </tbody>
</table>
</div>




```python
# select FDNY information for manhattan
x=df[df["Borough"]=="Manhattan"]
x
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
      <th>FacilityName</th>
      <th>FacilityAddress</th>
      <th>Borough</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Engine 4/Ladder 15</td>
      <td>42 South Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Engine 10/Ladder 10</td>
      <td>124 Liberty Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Engine 6</td>
      <td>49 Beekman Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Engine 7/Ladder 1/Battalion 1/Manhattan Boroug...</td>
      <td>100-104 Duane Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Ladder 8</td>
      <td>14 North Moore Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Engine 9/Ladder 6</td>
      <td>75 Canal Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Engine 15/Ladder 18/Battalion 4</td>
      <td>25 Pitt Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Engine 28/Ladder 11</td>
      <td>222 East 2nd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Engine 5</td>
      <td>340 East 14th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Engine 55</td>
      <td>363 Broome Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Ladder 20/Division 1</td>
      <td>253 Lafayette Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Engine 24/Ladder 5/Battalion 2</td>
      <td>227-29 6th Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Engine 33/Ladder 9</td>
      <td>42 Great Jones Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Ladder 3/Battalion 6</td>
      <td>108 East 13th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Squad 18</td>
      <td>132 West 10th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Engine 34/Ladder 21</td>
      <td>440 West 38th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Engine 26</td>
      <td>220 West 37th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Engine 3/Ladder 12/Battalion 7</td>
      <td>150 West 19th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Engine 1/Ladder 24</td>
      <td>142-46 West 31st Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Engine 14</td>
      <td>14 East 18th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Engine 16 / Ladder 7</td>
      <td>234 East 29th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Engine 21</td>
      <td>238 East 40th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Engine 54/Ladder 4/Battalion 9</td>
      <td>782 8th Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Engine 23</td>
      <td>215 West 58th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Rescue 1</td>
      <td>530 West 43rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Engine 40/Ladder 35</td>
      <td>131 Amsterdam Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Ladder 25/District Office 4/Division 3</td>
      <td>205-207 West 77th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Engine 74</td>
      <td>120 West 83rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Engine 65</td>
      <td>33 West 43rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Engine 8 / Ladder 2 / Battalion 8</td>
      <td>167 East 51st Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Engine 39/Ladder 16</td>
      <td>157-59 East 67th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Engine 44</td>
      <td>221 East 75th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Engine 22/Ladder 13/Battalion 10</td>
      <td>159 East 85th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Engine 58/Ladder 26</td>
      <td>1367 5th Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Engine 53/Ladder 43</td>
      <td>1836-46 3rd  Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Engine 91</td>
      <td>242 East 111th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Engine 35/Ladder 14</td>
      <td>2282 3rd Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Engine 76/Ladder 22/Battalion 11</td>
      <td>145-51 West 100th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Engine 47</td>
      <td>502 West 113th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Engine 59/Ladder 30</td>
      <td>111 West 133rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>40</th>
      <td>Engine 37/Ladder 40</td>
      <td>415 West 125th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>41</th>
      <td>Engine 69/Ladder 28/Battalion 16</td>
      <td>248 West 143rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>42</th>
      <td>Engine 80/Ladder 23</td>
      <td>503 West 139th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Engine 84/Ladder 34</td>
      <td>513 West 161st Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>44</th>
      <td>Engine 67</td>
      <td>518 West 170th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Engine 93/Ladder 45/Battalion 13</td>
      <td>515 West 181st Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Engine 95/Ladder 36</td>
      <td>29 Vermilyea Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>47</th>
      <td>Marine 1</td>
      <td>Little West 12th Street/Hudson River</td>
      <td>Manhattan</td>
    </tr>
  </tbody>
</table>
</div>




```python
# view the FDNY information for each manhattan
x=df[df["Borough"]=="Manhattan"]
x
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
      <th>FacilityName</th>
      <th>FacilityAddress</th>
      <th>Borough</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Engine 4/Ladder 15</td>
      <td>42 South Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Engine 10/Ladder 10</td>
      <td>124 Liberty Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Engine 6</td>
      <td>49 Beekman Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Engine 7/Ladder 1/Battalion 1/Manhattan Boroug...</td>
      <td>100-104 Duane Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Ladder 8</td>
      <td>14 North Moore Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Engine 9/Ladder 6</td>
      <td>75 Canal Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Engine 15/Ladder 18/Battalion 4</td>
      <td>25 Pitt Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Engine 28/Ladder 11</td>
      <td>222 East 2nd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Engine 5</td>
      <td>340 East 14th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Engine 55</td>
      <td>363 Broome Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Ladder 20/Division 1</td>
      <td>253 Lafayette Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Engine 24/Ladder 5/Battalion 2</td>
      <td>227-29 6th Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Engine 33/Ladder 9</td>
      <td>42 Great Jones Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Ladder 3/Battalion 6</td>
      <td>108 East 13th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Squad 18</td>
      <td>132 West 10th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Engine 34/Ladder 21</td>
      <td>440 West 38th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Engine 26</td>
      <td>220 West 37th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Engine 3/Ladder 12/Battalion 7</td>
      <td>150 West 19th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Engine 1/Ladder 24</td>
      <td>142-46 West 31st Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Engine 14</td>
      <td>14 East 18th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Engine 16 / Ladder 7</td>
      <td>234 East 29th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Engine 21</td>
      <td>238 East 40th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Engine 54/Ladder 4/Battalion 9</td>
      <td>782 8th Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Engine 23</td>
      <td>215 West 58th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Rescue 1</td>
      <td>530 West 43rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Engine 40/Ladder 35</td>
      <td>131 Amsterdam Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Ladder 25/District Office 4/Division 3</td>
      <td>205-207 West 77th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Engine 74</td>
      <td>120 West 83rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Engine 65</td>
      <td>33 West 43rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Engine 8 / Ladder 2 / Battalion 8</td>
      <td>167 East 51st Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Engine 39/Ladder 16</td>
      <td>157-59 East 67th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Engine 44</td>
      <td>221 East 75th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Engine 22/Ladder 13/Battalion 10</td>
      <td>159 East 85th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Engine 58/Ladder 26</td>
      <td>1367 5th Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Engine 53/Ladder 43</td>
      <td>1836-46 3rd  Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Engine 91</td>
      <td>242 East 111th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Engine 35/Ladder 14</td>
      <td>2282 3rd Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Engine 76/Ladder 22/Battalion 11</td>
      <td>145-51 West 100th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Engine 47</td>
      <td>502 West 113th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>40</th>
      <td>Engine 59/Ladder 30</td>
      <td>111 West 133rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>41</th>
      <td>Engine 37/Ladder 40</td>
      <td>415 West 125th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>42</th>
      <td>Engine 69/Ladder 28/Battalion 16</td>
      <td>248 West 143rd Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Engine 80/Ladder 23</td>
      <td>503 West 139th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>44</th>
      <td>Engine 84/Ladder 34</td>
      <td>513 West 161st Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Engine 67</td>
      <td>518 West 170th Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Engine 93/Ladder 45/Battalion 13</td>
      <td>515 West 181st Street</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>47</th>
      <td>Engine 95/Ladder 36</td>
      <td>29 Vermilyea Avenue</td>
      <td>Manhattan</td>
    </tr>
    <tr>
      <th>48</th>
      <td>Marine 1</td>
      <td>Little West 12th Street/Hudson River</td>
      <td>Manhattan</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
