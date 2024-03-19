---
Type: Learning
Course: "[[ZTM Machine Learning Course]]"
---
## Introduction 
- Pandas is a [[Python]] based data manipulation tool 
## Importing and getting started 
- `import pandas as pd`
## Datatypes 
- Two main data types:
	- `pd.Series`: one dimensional array 
	- `pd.DataFrame`: two dimensional array
## Importing & exporting data 
- `pd.read_csv("path/filename.csv")`: imports your CSV file as a DataFrame 
- `pd.to_csv("filename.csv")`: exports your DataFrame as CSV
## Anatomy of DataFrames 
![[pandas-anatomy-of-a-dataframe.png]]
## Describing data 
- `.dtypes`: shows what datatype each column contains 
- `.describe()`: returns a quick statistical overview of the numerical columns 
- `.info()`: shows some useful information about a DataFrame like how many rows there are, whether there are missing values, the datatype of each column 
- Statistical methods 
	- `.mean()`, `.sum()`
- `.columns`: shows all the columns of the DataFrame 
- `.index`: shows the values in a DataFrame's index 
- `len(DataFrame)`: shows the length (number of rows) of a DataFrame
## Viewing & selecting data 
- `DataFrame.head()`
- `DataFrame.tail()`
- `DataFrame.loc[]`: accesses a group of rows and columns by labels or a boolean array 
- `DataFrame.iloc[]`: accesses a group of rows and columns by integer indices 
- `DataFrame['column name']`
- `DataFrame['column name'] > 5`: filters and shows only the rows that meet the condition 
- `DataFrame.plot()`
- `DataFrame.hist()`
- `pd.crosstab`: computes a cross-tabulation of two or more factors 
## Manipulating data 
- `.fillna()`: fills in missing data 
- `.dropna()`: removes all data that has missing values 
- `.drop('column name', axis=1)`: removes the specified column 
- `.sample(frac=1)`: randomly samples different rows from a DataFrame and the `frac` parameter indicates the fraction of rows (1=100%, 0.5=50%, and so on)
- `sample(n=1)`: same as above, but you can specify the number of rows to sample instead of the percentage by using the `n` parameter 
- `reset_index()`: adds a new column of indices 
- `.apply(lambda x: x / 1.6)` converts the values from km to mi 
## Other functions & methods 
- `DataFrame[column].cumsum()`: cumulative sum of specified column
- `pd.date_range("1/1/2020", periods)`: periods is how many entries 