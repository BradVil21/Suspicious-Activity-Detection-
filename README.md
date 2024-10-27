# Suspicious-Activity-Detection-
[ ***READ ME: *** *Below are several projects related to using Excel, Python, and SQL to detect unusual transactions within a dataset.* ]

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


## 2. Python Analysis
   I have used Python with the provided tools for efficiently filtering and manipulating large datasets. I quickly applied various conditions to filter data based on specific criteria, which is essential for identifying suspicious transactions. **Download File Here: **


## 3. SQL Querying
   
