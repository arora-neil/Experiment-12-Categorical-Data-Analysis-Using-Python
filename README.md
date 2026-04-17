# Aim: Categorical Data Analysis Using Python

# Theory: 
Categorical Data Analysis involves analyzing data that can be divided into distinct groups or categories. These categories may or may not have an inherent order.

Types of Categorical Data:
1. Nominal Data

    Categories without any order

    Examples: Gender, Department, Blood Group

2. Ordinal Data

    Categories with a meaningful order or ranking

    Examples: Grades (A, B, C), Ratings (Good, Better, Best), Education Level
   
   

## Dataset 1: Student Data Analysis

  The dataset is loaded using:
  
  import pandas as pd
  
  df = pd.read_csv()
  
  This dataset contains categorical variables such as: Gender, Department, Grade

  1. df['Grade'].value_counts() - Counts the number of occurrences of each category
  2. df['Department'].value_counts() - Provides number of students in each department
  3. df['Grade'].value_counts(normalize=True) * 100 - Converts frequency into percentage
  4. df['Gender'].value_counts() - Counts number of males and females
  5. pd.crosstab(df['Gender'], df['Grade']) - Shows relationship between two categorical variables
  6. pd.crosstab(df['Department'], df['Gender']) - Shows grade distribution across departments
  7. pd.crosstab(df['Department'], df['Grade'], normalize='index') * 100 - Converts counts into percentages row-wise
  8. df.groupby('Department')['Grade'].value_counts() - Groups data by department then counts grades within each group

## Dataset 2: E-Commerce Data Analysis
  1. df['Category'].value_counts() - Counts number of orders per category
  2. df['Payment_Method'].value_counts() - Shows most commonly used payment methods
  3. df['Payment_Method'].value_counts(normalize=True) * 100 - Shows percentage usage of each payment method
  4. df[df['Category'] == 'Electronics'] - Filters dataset based on condition
  5. df.sort_values(by='Category') - Sorts dataset based on column values
  6. df['Category'].unique() - Returns all unique categories
  7. df['Category'].nunique() - Returns count of distinct categories
  8. pd.crosstab(df['Category'], df['Payment_Method']) - Shows relationship between category and payment method
  9. df.groupby(['Category','Payment_Method']).value_counts() - Groups data based on multiple columns
