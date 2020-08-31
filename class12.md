# Pandas in 10
We can import it:
`import pandas as pd`

## Object creation
* Creating a Series by passing a list of values, letting pandas create a default integer index:

    ` s = pd.Series([1, 3, 5, np.nan, 6, 8])`

* Viewing data

    1. To view the top and bottom rows of the frame:

     `df.head()` and `df.tail(3)`

    2. Display the index, columns:

      `df.tail(3)` and `df.columns`


* DataFrame.to_numpy() gives a NumPy representation of the underlying data.

* Selection : 

1. Getting
Selecting a single column, which yields a Series, equivalent to df.A:

2. Selection by label:

`df.loc[dates[0]]`

3. Selection by position:

`df.iloc[3]`

## String Methods

1. Merge:

pandas provides various facilities for easily combining together Series and DataFrame objects with various kinds of set logic for the indexes and relational algebra functionality in the case of join / merge-type operations.

2. Join

SQL style merges.

3. Grouping

By “group by” we are referring to a process involving one or more of the following steps:

* Splitting the data into groups based on some criteria

* Applying a function to each group independently

* Combining the results into a data structure
