# DAX-Power-BI

DAX (Data Analysis Expressions) is a formula language used in Power BI, Excel Power Pivot, and other Microsoft products for data modeling and analysis. It provides a variety of functions for working with data and creating calculated columns, measures, and tables. Here are some key DAX functions with examples and explanations:

# SUMX:

Description: Calculates the sum of an expression evaluated for each row in a table.
#Example:
Total Sales = SUMX(Sales, Sales[Quantity] * Sales[Price])
This calculates the total sales by multiplying the quantity and price for each row in the "Sales" table and then summing the results.

# AVERAGE:

Description: Calculates the average of a column of numeric values.
# Example:

Average Sales Price = AVERAGE(Sales[Price])
This calculates the average price of products in the "Sales" table.

COUNTROWS:

Description: Counts the number of rows in a table or table expression.
Example:
DAX
Copy code
Number of Customers = COUNTROWS(Customers)
This counts the number of rows in the "Customers" table.

FILTER:

Description: Returns a table that includes only the rows that meet the specified conditions.
Example:
DAX
Copy code
High-Value Customers = FILTER(Customers, Customers[Total Sales] > 1000)
This filters the "Customers" table to include only those customers with total sales greater than $1000.

IF:

Description: Returns one value if a condition is true and another if it's false.
Example:
DAX
Copy code
Sales Category = IF(Sales[Quantity] > 10, "High", "Low")
This categorizes sales as "High" if the quantity is greater than 10, otherwise "Low".

RELATED:

Description: Follows a relationship and retrieves the related value from another table.
Example:
DAX
Copy code
Employee's Department = RELATED(Departments[DepartmentName])
This retrieves the department name associated with an employee from the "Departments" table based on the established relationship.

MAX:

Description: Returns the maximum value from a column of numeric values.
Example:
DAX
Copy code
Highest Sales Value = MAX(Sales[SalesAmount])
This returns the highest sales amount from the "Sales" table.

RANKX:

Description: Assigns a rank to each row in a table based on the values in a specific column.
Example:
DAX
Copy code
Sales Rank = RANKX(Sales, Sales[SalesAmount])
This assigns a rank to each sale based on the sales amount in the "Sales" table.

EARLIER:

Description: Returns a value from a previous row context in a calculated column or measure.
Example:
DAX
Copy code
Sales Growth = Sales[SalesAmount] - EARLIER(Sales[SalesAmount])
This calculates the sales growth by subtracting the previous row's sales amount.

COUNTAX:

Description: Counts the number of rows in a table that meet a specified condition.
Example:
DAX
Copy code
Number of High Sales = COUNTAX(Sales, IF(Sales[SalesAmount] > 1000, 1, 0))
This counts the number of rows in the "Sales" table where the sales amount is greater than $1000.
