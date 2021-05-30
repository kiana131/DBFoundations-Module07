Kiana Sua 
<br>
5/29/21
<br>
IT FDN 130 A
<br>
Assignment 07

## SQL Functions

### Introduction

In this document I will define what is a SQL function and discuss why you might want to use a UDF (User-Defined Function). In addition, I will further explain the different types of UDF’s: scalar, inline and multi-statement. 

### SQL Function

A function is a database object that is composed of one or SQL more statements. SQL has built-in functions such ROUND and POWER, but you can also create custom function (UDL – User- Defined Function).  Functions can be separated in two different types, functions that return multiple rows (table) or functions that return a single row. Functions are like views but allow for multiple statements while a view is a single statement. Furthermore, they allow the input of parameters to change the results of the query while views do not. However, a huge drawback of using functions is that you cannot manipulate the state of the database such as performing operations such as insert, update and delete. (Figure1)  

![image](https://user-images.githubusercontent.com/84612735/120095708-36d1f680-c0dc-11eb-9a38-c685704beec8.png)

**Figure 1: Example of process of a function.**

Why would you use a function? A function can serve a few purposes, but the main usefulness of a function is that they allow for faster execution.  This is because you can write the function once and then recall it however many times that you need in the program.  When the program recalls the code and reuse it for repeated execution, this decreases the compilation time of the query. Furthermore, since it allows for modular programming, you can modify it independently from the source code. This is good for being able to separate more complex code from basic queries. Lastly, a function can help decrease network traffic because of its ability to reduce calculation and bundling commands. When used in conjunction with the WHERE clause a function can also help to further filter the records returned which in turn helps optimization. 

### Different Types of Functions
There are three main types of functions scalar, inline table-valued and multi-statement. Below they are defined:

**Scalar** – The best way to think of scalar functions is to think of what the definition of the word scalar is in math. In mathematics something that is scalar is something that has only magnitude and no direction. You can think of it as something that is representable by a position on a scale or a line.  It can be one of more variables, but the range is one-dimensional or in other words “flat”. This is in direct comparison to a vector function which is multi-dimensional and more complex. Therefore, a scalar function is something that returns only scalar values. 

**Inline Table-Valued** – This is a function that instead of returning a single scalar value like the one described prior, it returns a set of values. This can be compared to a view in SQL; however, the biggest difference is that this accepts parameters.  

**Multi-Statement Table-Valued Functions** - This returns a data set like inline table-valued functions, but it is different in that it can contain more than one statement. Furthermore, the structure of the table returned can be defined. Therefore, another way to think of it is that Inline Table-Valued Functions are like views while multi-statement is like stored procedures. Like views, ITV allow for better performance, but you cannot impact the underlying code and tables. Like stored procedures, MSTVF are slower or more “expensive” processes but can impact the underlying database tables.

### Conclusion
In summary, functions can be used to optimize performance by allowing a system to recall code and re-use it which decreases the compilation time. It is always good when writing a code to do as much as you can to not rewrite the same code again and reduce code repetition. Scalar, Inline and Multi-statement are all different types of functions. Scalar returns a single one-dimensional value while inline returns a dataset. Multi-statement also returns a dataset but has the further advantage of allowing for the table values to be defined and the ability to impact he is underlying database tables. 

