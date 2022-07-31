---
layout: default
title: "6. MySQL"
rank: 10
---

# Database management
This and the following two modules (see [2.5](./2_5_mysql.md) and [2.6](./2_6_mysql.md)) will introduce you to the basics of creating, using, and managing databases. We will first introduce some basic elements of tabular data and database formats, using examples from a number of different applications, including spreadsheets, desktop database programmes, and larger, multi-user database servers.

## Introduction
What is a database? A database, put simply, is a structured collection of data. Yesterday (see [1.5](./1_4_data_collection.md)), we discussed the definition of and types of data available from various resources in Assyriology. When confronted with large research databases that have been compiled by a large number of people over many years, you may come to think of databases as something very complex and difficult to oversee. It is important to remember, however, that all databases have to start out somewhere, and generally tend to rely on the same, relatively limited set of foundational elements.

It is equally important to remember that databases are collections of data developed around a specific set of research questions, and in order to address these questions in specific ways. As we will see, there are a number of ways in which 

* [Data tables](#data-tables)
* [Data types](#data-types)
* [Structuring data in plain text](#structuring-data-in-plain-text)
* [Structuring data in spreadsheets](#structuring-data-in-spreadsheets)
* Sorting and filtering

#### Applications

* OpenOffice Calc (a spreadsheet computer application, part of the OpenOffice package)
* 

### Data tables
At their very base, relational databases are organised around **tables** that can be related to each other in a wide range of ways. Tables are comprised by any given number of **columns** and **rows**. As you will all probably know, since you have all tried to use a bus or train schedule or order a concert ticket with different ticket categories or prices, **columns** and **rows** serve different purposes. **Columns** contain one specific **data type** storing data referring to one specific **variable**. **Rows** are observations made and recorded in said data types and according to said variables. Thus, for example:

animal | colour | limbs | bellies
-------|--------|-------|--------
fox | red | 4 | 1
whale | blue | 2 | 1
cow | black | 4 | 4

### Data types
The data type used for each column has a significant impact on the ways in which data can be analysed (we cannot computationally calculate an average number of limbs for all animals based on text data such as 'two' and 'four'). The variable or category defined by each column essentially dictates what we can and cannot talk about when examining observations contained in individual rows. For example, we might consider a fox and a whale more closely associated than a cow based on their identical number of bellies, but the table in itself will not tell us if these animals live in water or on land.

In virtually all standard relational databases, we find data ordered and stored according to a few basic types

name | description
-----|--------------
string | also called _text_ or _character_ field, storing any number of encodable characters
integer | also called number or whole number, storing any whole numerical value
double | also called float or decimal number, storing any whole or fractional value 
date | storing any calendar date comprised by year, month, day, and time

### Structuring data in plain text
When knowing the formal conventions of these data types, you can easily write a data table in plain text, using a format such as .csv or .tsv. If taking the example above, first in .csv (Comma Separated Values):

animal,colour,limbs,bellies<br>
fox,red,4,1<br>
whale,blue,2,1<br>
cow,black,4,4<br>

\- and below in .tsv (Tab Separated Values)

animal  colour  limbs   bellies<br>
fox red 4   1<br>
whale   blue    2   1<br>
cow black   4   4<br>

When properly structured and formatted, both of these plain text formats can be readily imported into just about any database application that you will ever use. As such, their  

### Structuring data in spreadsheets
[Spreadsheets](https://en.wikipedia.org/wiki/Spreadsheet) are computer applications built for the organisation and analysis of tabular data. As they are originally designed for accounting and bookkeeping, their primary toolbox is oriented towards calculation and statistics, but they can be used in virtually any context that involves tabular data.

All spreadsheet applications are structured around **cells** arranged into a grid of **columns** and **rows**, forming a table. Cells can contain any one of a range of data types, including text, number, and date. A cell is located within a grid according to its tabular position, namely **column name** and **row number**. So, for example, cell 'A2' is the first column (A), second row (2).

An individual table within a spreadsheet application is typically referred to as a **sheet**. The entire spreadsheet file is typically referred to as a **workbook**.

Cells, sheets, and workbooks can be linked across cells, sheets, and workbooks, provided that the correct link is given. Consider for example the following address:

                    ='[Workbook1.ods]Sheet1'!C2

\- where **[Workbook1.ods]** is the workbook file name (including file format extension), **Sheet1** is the sheet, and **C2** the cell within this sheet.

## Tasks

* [Create .csv for data import](#create-a-basic-csv)
* [Import .csv to spreadsheet](#import-csv-to-spreadsheet)
* 

### Create a basic .csv
We will begin with a simple exercise in the structuring and generation of tabular data, using an administrative cuneiform text from the Old Babylonian period as an example. The text is [BM 131698](https://www.britishmuseum.org/collection/object/W_1954-0510-9) and published as no. 13 in [Talon (1997) _Old Babylonian Texts from Chagar Bazar_](https://www.zotero.org/groups/2345127/items/D44PYT23).

1. Open a new text file in VS Code
2. Locate and download the excerpt [Talon 1997 no. 13](./files/2_4_obtcb_13_talon_1997.png) from the DAA Summer School repo on GitHub
3. First read through the transliteration and translation of OBTCB 13 and identify column variables to be defined
4. Write a .csv data file including the column variables defined and record for each entity mentioned in the text
4. Save the text as a .csv named **obtcb_13.csv** and commit the file to your **daa** repository on GitHub
5. Compare and discuss different ways of structuring this text with the rest of the group

### Import .csv to spreadsheet
To demonstrate the interoperability of .csv-file formats and spreadsheets, let us now try to import this .csv to a spreadsheet application. Here, we will use OpenOffice Calc, the spreadsheet application included in a free office suite called OpenOffice.

OpenOffice Calc maintains largely the same interface and offers the same range of core functionalities as Microsoft Excel, so if you have used the latter, the OpenOffice GUI should seem familiar to you

1. Open OpenOffice Calc and select **File > Open**
2. In the **Text Import** window, you will be required to give details as to _Import_ 










