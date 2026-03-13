# Numpy
**importing numpy:**
```
import numpy as np
```
**Array Creation**
```
np.array([1, 2, 3])              # 1D array
np.array([[1, 2], [3, 4]])       # 2D array (Matrix)
np.zeros((2, 3))                 # 2x3 matrix filled with 0s
np.ones((3, 3))                  # 3x3 matrix filled with 1s
np.arange(0, 10, 2)              # [0, 2, 4, 6, 8] (start, stop, step)
np.linspace(0, 1, 5)             # [0., 0.25, 0.5, 0.75, 1.] (5 evenly spaced values)
np.eye(3)                        # 3x3 identity matrix
np.random.rand(2, 2)             # 2x2 matrix of random values [0, 1)
np.random.randint(1, 10, size=5) # Array of 5 random integers between 1 and 9
```
**Array Attributes**
```
arr = np.array([[1, 2, 3], [4, 5, 6]])

arr.shape      # (2, 3)          gives dimensions (rows, cols)
arr.ndim       # 2               gives number of dimensions
arr.size       # 6               gives total number of elements
arr.dtype      # dtype('int64')  gives data type of elements
```
**Indexing & Slicing**
```
arr = np.array([10, 20, 30, 40, 50])
arr[1]         # 20              access specific index
arr[1:4]       # [20, 30, 40]    slicing [start:end]

arr2d = np.array([[1, 2, 3], [4, 5, 6]])
arr2d[0, 1]    # 2               access row 0, col 1
arr2d[:, 1]    # [2, 5]          get all rows, 1st column
arr2d[0, :]    # [1, 2, 3]       get 0th row, all columns

# Boolean Indexing
arr[arr > 25]  # [30, 40, 50]    filters elements based on condition
```
**Math Operations**
```
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

a + b          # [5, 7, 9]       element-wise addition
a - b          # [-3, -3, -3]    element-wise subtraction
a * b          # [4, 10, 18]     element-wise multiplication
a / b          # [0.25, 0.4, 0.5]element-wise division
a ** 2         # [1, 4, 9]       element-wise exponentiation

# Matrix Operations
np.dot(a, b)   # 32              Dot product (1*4 + 2*5 + 3*6)
a @ b          # 32              Shorthand for dot/matrix multiplication
```
**Aggregation Functions**
```arr = np.array([[1, 2], [3, 4]])

np.sum(arr)          # 10        sum of all elements
np.sum(arr, axis=0)  # [4, 6]    sum across columns (vertically)
np.sum(arr, axis=1)  # [3, 7]    sum across rows (horizontally)
np.min(arr)          # 1         minimum value
np.max(arr)          # 4         maximum value
np.mean(arr)         # 2.5       average of all elements
np.std(arr)          # 1.118     standard deviation
np.argmin(arr)       # 0         index of minimum value
np.argmax(arr)       # 3         index of maximum value (in flattened array)
```
**Reshaping & Manipulating**
```
arr = np.arange(1, 7)            # [1, 2, 3, 4, 5, 6]

arr.reshape(2, 3)                # [[1, 2, 3], [4, 5, 6]] (changes shape)
arr.ravel()                      # flattens multi-dim array to 1D
arr.T                            # transposes the array (rows become cols)

a = np.array([1, 2])
b = np.array([3, 4])
np.concatenate((a, b))           # [1, 2, 3, 4]
np.vstack((a, b))                # [[1, 2], [3, 4]] (vertical stack)
np.hstack((a, b))                # [1, 2, 3, 4] (horizontal stack)
```
---
# Pandas
**importing pandas**
```
import pandas as pd
```
**Series**
It is 1D array which can hold the data of ay datatype
```
s = pd.Series([10, 20, 30], index=['a', 'b', 'c'])  #we can also provide array and index files as list
```
**Dataframes**
It is 2D array which is in tabular format
```
data = {"Name": ["Alice", "Bob"], "Age": [25, 30]}
df = pd.DataFrame(data)

# Reading & Writing Data
df = pd.read_csv("data.csv")     # read from CSV file
df = pd.read_excel("data.xlsx")  # read from Excel file
df.to_csv("output.csv", index=False) # write DataFrame to CSV
```
**Viewing & Inspecting Data**
```
df.head(5)          # view first 5 rows
df.tail(3)          # view last 3 rows
df.info()           # prints index, columns, non-null counts, memory usage
df.describe()       # basic statistical details (mean, std, min, max) of numeric cols
df.shape            # (rows, cols)
df.columns          # list of column names
df.dtypes           # data types of each column
df.index            # row indices
```
**Selection & Indexing**
```
# Selecting Columns
df["Age"]                # returns 'Age' column as a Series
df[["Name", "Age"]]      # returns multiple columns as a DataFrame

# Selecting Rows (.loc for labels, .iloc for integer positions)
df.loc[0]                # row with index label 0
df.iloc[0]               # 0th row (integer based)
df.loc[:, "Age"]         # all rows, 'Age' column
df.iloc[0:2, 0:2]        # first 2 rows, first 2 columns
```
**Filtering**
```
df[df["Age"] > 25]                   # rows where Age > 25
df[(df["Age"] > 25) & (df["Name"] == "Bob")] # multiple conditions (AND)
df[(df["Age"] < 20) | (df["Age"] > 60)]      # multiple conditions (OR)
df[df["Name"].isin(["Alice", "Eve"])]        # filter by list of values
```
**Handling Missing Data**
```
df.isna()                   # boolean df showing True for missing (NaN) values
df.isna().sum()             # count of missing values per column
df.dropna()                 # drop all rows containing any missing value
df.dropna(axis=1)           # drop all columns containing any missing value
df.fillna(0)                # replace missing values with 0
df["Age"].fillna(df["Age"].mean(), inplace=True) # fill NaN with column mean
```
**Modifying Dataframe**
```
df["Salary"] = [50000, 60000]        # add new column
df.rename(columns={"Name": "Emp_Name"}, inplace=True) # rename column
df.drop("Salary", axis=1)            # drops a column (axis=1)
df.drop(0, axis=0)                   # drops a row (axis=0)
df.replace(25, 26)                   # replace specific values in DF
df.sort_values(by="Age", ascending=False) # sort by specific column
```
**Grouping and Aggregation**
```
df["Age"].value_counts()             # counts unique values in a column
df["Age"].unique()                   # returns array of unique values
df["Age"].nunique()                  # number of unique values

# Groupby
df.groupby("Department")["Salary"].mean() # average salary per department
df.groupby("Department").agg({"Salary": "mean", "Age": "max"}) # multiple aggregations
```
**Merging and Concatenation**
```
df1 = pd.DataFrame({"ID": [1, 2], "Name": ["Alice", "Bob"]})
df2 = pd.DataFrame({"ID": [1, 2], "Score": [90, 85]})

# Merge (SQL-like Joins)
pd.merge(df1, df2, on="ID", how="inner")  # merges on common column 'ID'

# Concatenate (Stacking DataFrames)
pd.concat([df1, df2], axis=0)        # stacks vertically (rows on top of rows)
pd.concat([df1, df2], axis=1)        # stacks horizontally (side-by-side)
```
