# DAX-Power-BI

**DAX (Data Analysis Expressions)** is a formula language used in Power BI, Excel Power Pivot, and other Microsoft products for data modeling and analysis. It provides a variety of functions for working with data and creating calculated columns, measures, and tables. Here are some key DAX functions with examples and explanations:



# COUNT: Counts cells containing numbers.
=COUNT(Sales[Amount])
This counts the number of non-blank values in the 'Amount' column of the 'Sales' table.

# COUNTA: Counts non-empty cells.
= COUNTA(Reseller[Phone])
The COUNTA function counts any type of information, and this includes error values and empty text. For example, if the range returns an empty string, the COUNTA function counts that value. What it does not count are empty cells.

# COUNTAX: Counts non-blank cells that meet a condition.
=COUNTAX(FILTER(Sales, Sales[Amount] > 100), Sales[Product])
This counts the number of rows in the 'Sales' table where the 'Amount' column is greater than 100, based on the 'Product' column.

# COUNTX: Counts items that meet a condition in a table.
=COUNTX(Sales, Sales[Quantity] * Sales[Unit Price])
This counts the number of rows in the 'Sales' table where the product of 'Quantity' and 'Unit Price' is not blank.

# COUNTROWS: Counts the number of rows in a table.
=COUNTROWS(Customer)
This counts the number of rows in the 'Customer' table.

# COUNTBLANK: Counts blank cells.
=COUNTBLANK(Sales[Discount])
This counts the number of blank or null values in the 'Discount' column of the 'Sales' table.
