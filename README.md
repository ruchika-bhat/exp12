# AIM: CATEGORICAL DATA ANALYSIS USING PYHTON


# THEORY:
Categorical Data Analysis is a statistical method used to analyze data that can be classified into distinct categories or groups. 
Unlike numerical data, categorical data represents qualitative attributes such as gender, department, grades, or types of transactions. 
The primary objective of this analysis is to summarize, interpret, and find relationships between such categorical variables.
In this experiment, Python is utilized as a computational tool to perform categorical analysis efficiently. 
The pandas library plays a crucial role by providing DataFrame structures that allow easy manipulation, organization, and analysis of categorical datasets.

# Data Representation Using DataFrames:
A dataset is first loaded into a pandas DataFrame, which is a two-dimensional labeled data structure. 
It enables efficient handling of rows and columns, similar to tables in databases.
import pandas as pd
df = pd.read_csv('data.csv')
The DataFrame structure allows categorical variables to be stored as columns and facilitates various operations such as filtering, counting, and grouping.

# Identification of Categorical Variables:
Categorical variables are identified based on their data type and unique values. These variables typically contain a limited number of distinct categories.
df.info()
df['Column_Name'].unique()
info() provides details about data types and non-null counts
unique() lists all distinct categories present in a column
This step is important for understanding the structure and diversity of the dataset.

# Frequency Distribution:
Frequency distribution is a fundamental concept in categorical data analysis. It represents the number of occurrences of each category.
df['Column_Name'].value_counts()
This method helps in:
Identifying dominant and rare categories
Understanding how data is distributed across groups

# Relative Frequency and Percentage Distribution:
To better interpret categorical data, frequencies are often converted into proportions or percentages. This provides a normalized view of the data.
df['Column_Name'].value_counts(normalize=True) * 100
Percentage distribution is especially useful when comparing datasets of different sizes or analyzing proportional representation.

# Cross Tabulation:
Cross tabulation is used to examine the relationship between two categorical variables. It displays the joint frequency distribution in a tabular form.
pd.crosstab(df['Column1'], df['Column2'])

This technique helps in:
Identifying patterns between variables
Studying dependencies or associations
Performing comparative analysis across categories

# Normalized Cross Tabulation:
To enhance interpretability, cross-tabulated data can be normalized to show percentages instead of raw counts.
pd.crosstab(df['Column1'], df['Column2'], normalize='index') * 100

This provides:
Row-wise proportional distribution
Better comparison within each category group

# Grouping:
Grouping is an advanced technique used to organize data into subsets based on one or more categorical variables. 
It allows detailed analysis within each group.
df.groupby('Column1')['Column2'].value_counts()

Grouping helps in:
Performing hierarchical analysis
Observing trends across multiple categories
Extracting deeper insights from structured data

# Data Inspection and Validation:
Before performing analysis, it is essential to inspect the dataset to ensure accuracy and consistency.
df.head()
df.shape
head() displays the initial rows of the dataset
shape provides the number of rows and columns

This step ensures that the dataset is correctly loaded and ready for analysis.


# CONCLUSION:
Categorical Data Analysis using Python provides a systematic approach to handling qualitative data. By applying techniques such as frequency distribution,
percentage analysis, cross tabulation, and grouping, meaningful patterns and relationships can be identified. 
The use of pandas simplifies these operations and enhances efficiency, making Python a powerful tool for statistical data analysis.






