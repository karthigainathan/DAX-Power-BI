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




# CALCULATE:Modifies the filter context for scalar calculations (e.g., aggregations).
CALCULATE(SUM(Sales[Amount]), Sales[Region] = "North")

The CALCULATE function is one of the most important functions in DAX. It allows you to change the filter context for a calculation and evaluate an expression in a different context.
It can be used to modify row context (when used in calculated columns) or filter context (when used in measures).
You can add, modify, or remove filters, and then calculate an expression based on the modified context.
CALCULATE is commonly used to apply filters, perform calculations with different contexts, and control how calculations are aggregated.

# Modifies the filter context for table calculations (e.g., filtering tables).
CALCULATETABLE(Sales, Sales[Region] = "North")

The CALCULATETABLE function is similar to CALCULATE, but it is specifically designed to change the filter context for tables rather than for scalar values.
It evaluates an expression within a modified filter context and returns a table of results.
CALCULATETABLE is useful when you want to apply filters to tables and perform calculations with the filtered tables.
