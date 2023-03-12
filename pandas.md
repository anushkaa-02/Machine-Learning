# Pandas
Pandas is a software library written for the Python programming language for bit manipulation and analysis. In particular it offers data
structures and operations for manipulating numerical tables and time series.

### Main data structure:
- Dataframes
- Series


### Importing pandas:
```python
import pandas as pd
```
### Importing .csv file into jupyter:
```python
pd.read_csv('file_name')
```
## Functions & attributes:
- data.head() 
  - To preview the top 5 data (You can also add value to the function to see those specific data)
- data.tail()
  - To preview the last 5 data (You can also add value to the function to see those specific data)
- data.shape
  - to see how many rows and columns
- data.describe()
  - only valid for numeric datatypes 


## Fetching rows & columns with iloc:
- data['coloumn_name']
  - to see more coloumns, add column names with separated commas.
- data.iloc[any row no]
  - fetch either 1 row or multiple rows.
  - can apply fancy indexing also.
