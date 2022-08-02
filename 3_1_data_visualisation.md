---
layout: default
title: "1. Data Visualisation"
rank: 15
---

# Visualising Data

This session will give an overview of data visualisation techniques and introduce some tools that can be used to visualise data.

### Visualising data with Tableau
Tableau is a data visualisation software. There are numerous tutorials available, including Tableau's own e-learning platform that you have access to as part of your license. The following is therefore only a very brief introduction to the most important features:

- **Data Source / Connections**: Tableau can import .xls files (Excel files, NOTE: not .csv files!), .txt files, .json files and others, as well as connect to servers. At the bottom, you can also see some workbooks that come with the software and you can also use to practice. After connecting to your chosen data source, you can run Data Interpreter to clean your data if necessary. Tableau outputs the results of the data cleaning operation as an .xls file.
- **Worksheet (Sheet1)**: On the left hand side, you can see your tables and the respective data type (text, number, boolean, date, geographical data). The most important data types for our purposes are text (represented by the symbol Abc) and number (represented by #). Tableau automatically detects which data type your data is, but you can also manually adjust that.
- Tableau uses the terms **Dimensions** and **Measures**. Generally, Dimensions are text values (and represented in blue in Tableau) and Measures are number values (represented in green). Dimensions as independent variables and Measures are dependent variables (and a function of one or more Dimensions). 
- **Marks Toolbar**: Here you can adjust how you want to represent your data. You can label it and adjust colour, size and detail.
- **Column and Row Shelves**: your can drag and drop your tables in there and then your visualisation will appear in the Canvas-section below.
- The **Show Me** pane: This shows you the types of graphs and charts you can create and how many Dimensions and Measures you need for them.
- **Creating Graphs**: Drag and drop table values into the Column and Row Shelves. You always need at least one Measurement value (Count is usually a good option). Then select the type of graph you would like to create. You can edit your labels in the Marks Toolbar. 
- **Exporting Graphs**: Go to Worksheet > Export > Image. Select the information you would like to include, click on Save... and select the file format (.png, .bmp or .jpg).

### Assignments
#### Task 1
Load the file Collections.xls into Tableau (this dataset contains data about museum collections holding cuneiform documents). This dataset contains geographical information. Drag and drop Country (ISO) and Count into the Column and Row Shelves to display the number of collections with cuneiform objects per country on a map.

### Task 2
Load the File Nationalmuseum.xls into Tableau (this dataset contains the texts from the Danish National Museum that are in CDLI). Analyse the collection of this museum by visualising different aspects of the collection. Which types of graph are particularly useful for which analyses?

### Task 3 (Advanced)
Go to the new CDLI (https://cdli.mpiwg-berlin.mpg.de). Find a small (ideally <1000 results) subset of texts via the search function and download the catalogue data for your search results as a .csv file. Convert the .csv file to .xls and import it into Tableau. Analyse your dataset in Tableau and create some different graphs.

## Resources

Tableau (free student license can be requested here: https://www.tableau.com/academic/students)

## Literature
Hudson, Pat, and Mina Ishizu. History by Numbers: An Introduction to Quantitative Approaches. London: Bloomsbury Academic, 2016. https://www.bloomsbury.com/uk/history-by-numbers-9781474294157/.

Yau, Nathan. Visualize This: The FlowingData Guide to Design, Visualization, and Statistics. Wiley. 2011.

