# Suspicious-Activity-Detection-
[ ***READ ME*** *Below are several projects related to using Excel, Python, and SQL to detect unusual transactions within a dataset.* ]

## 1. Excel Dataset 

| Transaction Date | Amount | Sender      | Receiver     | Location         |
|------------------|--------|-------------|--------------|------------------|
| 2024-10-01       | 15000  | John Doe    | ABC Corp     | United States    |
| 2024-10-03       | 2000   | Jane Smith  | XYZ Ltd      | United Kingdom   |
| 2024-10-04       | 25000  | Alice Chen  | DEF Corp     | Singapore        |
| 2024-10-05       | 800    | Mark Brown  | HIJ Ltd      | United States    |
| 2024-10-06       | 6000   | Emma Wilson | KLM Corp     | Germany          |
| 2024-10-07       | 35000  | John Doe    | OPQ Ltd      | Cayman Islands   |
| 2024-10-08       | 12000  | Jane Smith  | RST Corp     | United States    |
| 2024-10-09       | 500    | Mark Brown  | XYZ Ltd      | Canada           |
| 2024-10-10       | 1500   | Alice Chen  | DEF Corp     | Singapore        |
| 2024-10-11       | 18000  | Emma Wilson | UVW Ltd      | Cayman Islands   |
| 2024-10-12       | 7500   | John Doe    | ABC Corp     | United Kingdom   |
| 2024-10-13       | 40000  | Jane Smith  | XYZ Ltd      | Russia           |
| 2024-10-14       | 9000   | Alice Chen  | KLM Corp     | United States    |
| 2024-10-15       | 17000  | Mark Brown  | OPQ Ltd      | Germany          |
| 2024-10-16       | 2000   | Emma Wilson | RST Corp     | Singapore        |
| 2024-10-17       | 30000  | John Doe    | ABC Corp     | Russia           |
| 2024-10-18       | 9500   | Jane Smith  | UVW Ltd      | Canada           |
| 2024-10-19       | 4000   | Alice Chen  | HIJ Ltd      | United States    |
| 2024-10-20       | 25000  | Mark Brown  | XYZ Ltd      | Russia           |
| 2024-10-21       | 7000   | Emma Wilson | DEF Corp     | Cayman Islands   |

Above is the data set showing what was used to detect unusual transactions. With a step-by-step process, 1. Highlighted and identified the high-value transactions greater than or equal to $10,000. Instructions: **Home > Conditional Formatting > Highlight Cell Rules > Greater than > Choosing a desired amount **. 2. Highlighted Duplicate transactions that could indicate suspicious activity. Instructions: **Home > Conditional Formatting > Highlight Cell Rules > Duplicate values **. 3. Sheet #2 I've created a Pivot Table to summarize the data of the total transactions by the amount/location. **Download File Here: **


2. Python Analysis
   I have used Python with the provided tools for efficiently filtering and manipulating large datasets. I was able to quickly apply various conditions to filter data based on specific criteria, which is essential for identifying suspicious transactions. **Download File Here or View Code Below: **
   
   # READ ME: I will be using Python for deeper data analysis and automation 

# Import pandas libary as an alias pd

import pandas as pd 

#setting a variable for excel dataset
# Loading the Excel file dataset into Python. "File name: Suspicious Activity Detection Excel Data.xlsx"
# File path: "C:\Users\bradl\OneDrive\Desktop\Suspicious Transaction Detection Tool Project\Suspicious Activity Detection Excel Data.xlsx"

df = pd.read_excel("C:/Users/bradl/OneDrive/Desktop/Suspicious Transaction Detection Tool Project/Suspicious Activity Detection Excel Data.xlsx")

# Printing all rows and columns of the dataframe 
df.columns = df.columns.str.strip()
print(df)

# Filtering by amount greater than $10,000, sender, and location
high_value_transaction = df[df['Amount'] > 10000]
Jane_Smith = df[df['Sender'] == 'Jane Smith ']
US_Transactions = df[df['Location'] == 'United Kingdom']


print(high_value_transaction)
print(Jane_Smith)
print(US_Transactions)

# Analyzing the Data 

# 1. Analyzing the total amount of High-Value Transactions
total_amount_transaction = high_value_transaction['Amount'].sum()
print(f"The total amount of high value transactions: ${total_amount_transaction:.2f}")

# 2. Counting the amount of transactions each sender made
sender_transaction_count = df['Sender'].value_counts()
print(sender_transaction_count)

#3. Average transaction amount by the location 
average_transaction_location = df.groupby('Location')['Amount'].mean()
print(average_transaction_location)


# Visualizing the data importing library matplotlib
import matplotlib.pyplot as plt

# plotting the transactions by the sender 
sender_transaction_count.plot(kind='bar', color='skyblue')
plt.title('Sender Transaction Count')
plt.xlabel('Sender')
plt.ylabel('Number of Transactions')
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()


4. SQL Querying
   
