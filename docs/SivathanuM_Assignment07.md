#### Muthulekshmi Sivathanu
#### 02-03-2021
#### Foundations of Databases and SQL programming
#### Assignment-07
## Functions
### Introduction

The module describes about built in functions and user defined functions which are used in SQL to retrieve data from database.

### SQL User Defined function Usage

Like functions in programming languages, User Defined Functions accept parameters, do some calculation on the parameters, and return the result. The result can be a single value ( Figure 1 )  or a table, as in below.

![](https://github.com/muthulekshmis/DBFoundations-Module07/blob/main/docs/Picture%201.png)

Figure 1 Function returning single value

A function allows us to dynamically pass a scalar value. Based on the scalar value, the function can return a table. For the same function definition, we can pass different values. For each value, a table can be returned. Without functions, we would end up creating multiple views with select statement for each scalar value. In Figure 2 we use the same function to fetch table rows for different values 0, 1 and -1 .

![](https://github.com/muthulekshmis/DBFoundations-Module07/blob/main/docs/Picture%202.png)

Figure 2 Function returning table based on different parameter

Join can be performed using a column extracted through UDF and a column from a table. This will increase the solution possibilities .

### Inline Table Valued Function	vs Multi Statement Table Valued Function

![](https://github.com/muthulekshmis/DBFoundations-Module07/blob/main/docs/ITVF%20vs%20MSTVF.png)

Scalar function: Scalar function can accept any number of parameters, but it returns a single data value of the type defined in returns class.   Since the function defined in Figure 1 returns a single data value, it is a scalar function. The term scalar means, a single simple flat value, compared to complex structured values such as array or result set. 
Table Valued Function: This returns a table which is a result of single select statement. If the same function in Figure 2 returns a table (RETURNS TABLE) it becomes a table valued function. There are two types in it which are Inline Table Valued Function and Multi Statement Table Valued Function
System Function: These functions are pre-built and provide many system functions which is used to perform a variety of operations.  CAST, CONVERT, ISNULL are some of the system functions. 	

### Summary
In this module, I learnt about many built in functions. Queries were tried using these functions and executed successfully. The module also briefed about user defined functions. In question 7 of the assignment, “YEAR(CAST InventoryDate) AS Date” did not bring any change in the result as there was only one year 2017 . When tried with “MONTH(CAST InventoryDate) AS Date” , it still did not show any change , as inventory date which was already grouped and ordered using “partition-by” and “ordered by” in Question 6 was used in Question 7.


------------------------------------------------------------------------------------------
Referred from Module 7 Notes
https://database.guide/difference-between-multi-statement-table-valued-functions-inline-table-valued-functions-in-sql-server/ Referred on 03-01-2021 
https://database.guide/difference-between-multi-statement-table-valued-functions-inline-table-valued-functions-in-sql-server/ Referred on 03-01-2021
