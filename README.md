
import pandas as pd

# Responsibility 1: Read CSV files and manipulate data frames using pandas

# Read a CSV file into a DataFrame
df = pd.read_csv('your_file.csv')

# Display the first few rows of the DataFraame
print("Initial dataa:")
print(df.head())

# Responsibility 2:perform simple data cleaning tasks

# Handle missing values (filling with 0)
df.fillna(0, inplace=True)

# Remove duplicates based on a subset of columns
df.drop_duplicates(subset=['column_name'], keep='first', inplace=True)

# Responsibility 3: practice basic data manipulation operations

# Example of filtering data based on a condition
filtered_data = df[df['column_name'] > 10]

# Example of sorting data based on one or more columns
sorted_data = df.sort_values(by='column_name', ascending=False)

# Example of grouping data by a column and calculating mean of another column
grouped_data = df.groupby('grouping_column').agg({'aggregation_column': 'mean'}).reset_index()

# Display filtered, sorted, and grouped data
print("\nFiltered data:")
print(filtered_data.head())
print("\nSorted data:")
print(sorted_data.head())
print("\nGrouped data:")
print(grouped_data.head())