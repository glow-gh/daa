---
layout: default
title: "2.2 R and RStudio"
rank: 8
---

# R and RStudio

## Introduction
This module will introduce you to the coding language R and the integrated developer environment software package RStudio. R is a widely used coding language with particularly strong abilities in handling, manipulating, and visualising large amounts of tabular data. 

RStudio is an IDE (integrated developer environment) designed specifically for use with R, which adds a number of features to the base R Console, including overviews

##### Applications
* [R](https://www.r-project.org) - a coding language (can be downloaded at [https://www.r-project.org](https://www.r-project.org)) 
* [RStudio](https://www.rstudio.com/products/rstudio/download/) - an integrated developer environment (IDE) for R (can be downloaded at [https://www.rstudio.com/products/rstudio/download/](https://www.rstudio.com/products/rstudio/download/))
* [R Markdown](https://rmarkdown.rstudio.com) - a Markdown syntax for producing notebooks including R code 

### Tasks

* [The R Console](#the-r-console)
* [The R Editor](#the-r-editor)
* [Creating an R Notebook document](#creating-an-r-notebook-document)
* [Setting up an R Studio project](#setting-up-an-rstudio-project)
* [RStudio and GitHub](#rstudio-and-github)
* [Libraries and packages](#libraries-and-packages)
* [Importing sample data](#importing-sample-data)
* [Evaluating sample data](#evaluating-sample-data)

## R
While we will primarily be working with RStudio in this and the next module, let us just briefly introduce coding in R itself. 

### The R Console
Coding in R can be undertaken with the use of the R Console, which is an integral part of a standard R installation. Note that R can also be written directly in the Windows Command Prompt or the MacOS Terminal.

1. Open the R editor on your laptop
2. Take a moment to familiarise yourself with the interface. The default interface when opened will give you a short version description of the R version you are currently using, information on how to access citation information and demos
3. Below this initial text is a line starting with a >, which is a coding line where new commands can be entered. Note that the R Console will execute the command given in this line when pressing **Enter**
4. Type in '**getwd()**', a command that will return the path of the current working directory, and press **Enter**.

### The R Editor
To write scripts in R, standard practice is to use an R Editor document, which allows you to save the script as a self-contained file. While you can use the R Console to try out commands, you cannot save scripts from this location.

1. To write a script in R, start by opening a new document using **File > New Document**. This document is called an R Editor
2. In the first line of this document, type in '**getwd()**' again and press **Enter**. Note how the command in a line is not executed. Instead, the cursor moves to the line below. To execute a command in a line in the R Editor window, you need to instead press **Command + Enter** for execute the line where the cursor is placed, or highlight the lines that you want to execute and then press **Command + Enter**. You should then see the command executed appear in the R Console, followed by a results line preceded by '[1]'
3. Let us try this out while performing a standard exercise in R, namely identifying and setting the working directory of a script.
4. Write in the following set of commands:
    > getwd()<br>
    > setwd("[path of your Documents folder")<br>
    > dir.create("R")<br>
    > setwd("[path of your Documents folder/R")<br>
    > getwd()
5. Now highlight all five lines of code and press **Command + Enter**.
6. Note the listing of commands executed and the result returned at the end. The working directory should now be set to a folder named **R**, contained in your **Documents** folder

When working with R and RStudio, it is standard practice always to start out by checking the current working directory using **getwd()**, and to set the desired working directory if necessary using **setwd()**

7. To save the script in the R Editor, go to **File > Save** and save the script to the R folder. Note the file extension of an R script file, namely **.R**
8. Close the script and R Console. Note that when closing the R Console, R will ask if you want to save the current workspace image, so that the commands and results currently in the Console will be stored until R Console is opened again.

## RStudio
It is perfectly possible to write extensive and complex scripts in R Console and R Editor, but unless you are a trained coder, it will quickly become difficult to manage the various outputs and files involved. To this end, RStudio provides you with a working environment for writing R scripts _and_ keep track of files, functions, and libraries.

1. Open RStudio
2. Initially, let us familiarise ourselves with the various elements that make up the RStudio user interface
3. The default user interface will contain three primary windows with a number of different internal panes. 
    * The principal one is the **Console** on the left hand side, which you are already familiar with.
    * On the top right, we have the **Environment** window, which will show you all **objects** currently found within the coding environment
    * On the bottom right, finally, is the **Viewer**, which also includes panes for **Files**, **Plots**, **Packages**, and **Help**
4. In the current setup, the **Console** works in the same way, namely in that you can write and execute commands in R. You will rarely use it for these purposes in RStudio, however, but it is important to note that the **Console** will still show all commands executed and results returned, just as with the R Editor in the base R Console

### Creating an R Notebook document
A central feature in RStudio is the ability to create more elaborate file formats than base R. A much used format is [R Markdown](https://rmarkdown.rstudio.com), a variety of basic Markdown syntax that we saw yesterday (see [1.3 Markdown](./1_3_markdown.md)), which can also include and run R code.

R Markdown files come in two different varieties in RStudio, namely R Markdown and R Notebook. The former is a file format, the latter is a way of viewing and generating .html-formatted output from R Markdown. Both formats are stored in R Markdown, using the file extension **.Rmd**. For reasons that will become clearer in a moment, we will start by creating an R Notebook.

1. Open the dropdown menu from the **New File** icon in the far left of the top toolbar and select **R Notebook**
2. A new window will open above the **Console** window, with some guiding text on the format and use of an R Markdown document
3. Start by saving this file to your R folder, with the file name **first_r_markdown**

A couple of remarks about the structure of an R Markdown or Notebook file. The top four lines contains a YAML header, which you encountered during the [Markdown](./1_3_markdown.md) module yesterday. This includes the title of the document when converted, and the conversion output, which is set to .html as default for R Notebooks.

Below comes the standard Markdown syntax that you should already be familiar with. R Markdown formats will accept the same Markdown syntax as you were introduced to yesterday.

The highlighted area below is a **chunk** of R code. R code is included in R Markdown using **\```{r}** when starting the chunk and **```** when closing the chunk. You can also press the button **Insert a new code chunk** on the top R Notebook window toolbar. Within this space, R code can be entered and executed.

1. As stated in the guiding text, try executing the command given in the chunk by pressing the **Run Current Chunk** arrow on the right or pressing **Command + Shift + Enter** when the cursor is inside the chunk.
2. The resulting graph is generated by executing the base R function **plot()** on a dataframe named **cars**
3. As mentioned in the guiding text below the graph, an R Notebook will save an .html-file containing code and output from Markdown. This can be visualised if pressing the **Preview** button on the top R Notebook window toolbar.
4. You should now see an .html-version of the R Notebook in the **Viewer** window on the bottom right.

### Setting up an RStudio project
Just like VS Studio has workspaces to manage various file collections, RStudio has **projects**. Projects are useful because they will help you keep track of files, and also because they can be synced with a **GitHub** repository to allow for **Git** version control of R projects and files.

1. To set up a project, go to the top right corner of the RStudio interface and open the drop-down menu from the **Project (None)** button.
2. Select **New Project**
3. In the **New Project Wizard**, you can choose from three options:
    * **New Directory**, which creates a new folder and associates this with an RStudio project
    * **Existing Directory**, which makes an existing folder an RStudio project directory
    * or **Version Control**, which allows you to clone a remote Git repository, for example from GitHub, to a local directory and use this as an RStudio project directory
4. Choose **Existing Directory**
5. As project working directory, give the **R** folder that you set up previously
6. Press **Create Directory**

You should know see a number of things happening with RStudio. First, the project button text in the top right corner will have changed from **Project (None)** to **R**, indicating which project RStudio is currently working in. Second, the **Viewer** windown in the bottom right will have changed to the **Files** pane, giving you an overview of all the files contained in the project directory, namely the **R** folder.

### RStudio and GitHub
Integrating RStudio with GitHub is easy provided that you already have **Git** installed on your system, have set up a GitHub user profile, and have a repository that can be cloned.

1. Create a private repository on your GitHub user account named **daa_rstudio**, and remember to include a README file
2. Copy the URL of the new repository
3. In RStudio, go to the **Project** button in the top right corner and select **Version Control > Git**
4. In the **Clone Git Repository** window, paste in the repository URL, give the project directory a name (**daa_rstudio**) and check the location
5. Press **Create Project**

### Libraries and packages
We have now been through setting up RStudio for working with R code and Markdown. Now, let us look at how R and RStudio handles data. To do this, we should first introduce the concepts of **libraries** or **packages** in R. **Libraries** are collections of functions or commands, that can be downloaded to R and RStudio and launched when required. One of the things that make R such a versatile programming language is the very wide range of **libraries** available. In the **Packages** pane of the **Viewer** window, you can see a list of libraries available on your system, and those that are currently loaded.

Curated libraries can be downloaded in RStudio by selecting **Tools > Install Packages...** from the top menu. We will try downloading a single library in a little while, to illustrate how that works. 

### Importing sample data
R comes with a set of native libraries typically referred to as **base R**, which include the most basic functions for working with a variety of data. Now, we will import some sample data and see how some of these functions work. We will use a basic .csv prepared by the GLoW project, which contains an index of the c. 550 archaeological locations where cuneiform inscriptions have been found. You can read more about this resource in [Rattenborg et al. 2021](https://cdli.ucla.edu/pubs/cdlj/2021/cdlj2021_001.html) and see the online location of the resource on [Zenodo](https://doi.org/10.5281/zenodo.4960710).

To import a .csv from an online location to R, we can use the command **read.csv()** with the download URL of the .csv-version of CIGS. Note that filepaths in R should always be enclosed in "" or ''.

1. Paste the code given below into a chunk in the R Notebook and then run the chunk
> read.csv("https://zenodo.org/record/5642899/files/CIGS_v1_4_20211101.csv?download=1")
2. The result returned should be a table with 25 columns and 564 rows

The .csv-version of the CIGS index is a very small file in the context of what R can handle. When importing very large data files, from a local disk or a remote location, it is often preferable to check the format and structure of the file before importing the entire dataset. For this we can use the **head()** function, which returns a set number of rows from the beginning of the file.

3. Paste the code given below into a chunk in the R Notebook and then run the chunk
> head(read.csv("https://zenodo.org/record/5642899/files/CIGS_v1_4_20211101.csv?download=1"))
4. The result returned should be a table with 25 columns and only six rows

So far, we have performed operations that have not actually imported the data contained in CIGS into RStudio, but rather served to view and inspect the data file. If we want to work further with this data, we would need to turn it into an object that can be subjected to data manipulation. In R, tabular data such as CIGS is called **dataframes**. These can be created by using an arrow operator **->** or **<-**, which will forward the result of a given command to a variable, or object.

5. Paste the code given below into a chunk in the R Notebook and then run the chunk
> cigs <- read.csv("https://zenodo.org/record/5642899/files/CIGS_v1_4_20211101.csv?download=1")
6. The result should be the appearance of a data object in the **Environment** window on the top right.
7. Write a new chunk with the command **head(cigs)** and inspect the result.

### Evaluating sample data
We now have an object that can be subjected to further analysis and manipulation. First, let us look at some basic tools for examining data. 

The **cigs** dataframe contains 25 columns. You can of course print the entire dataframe, or open it from the **Environment** window by clicking the object, but printing a list of column names may often be just as useful. We can do so using the **names()** function

1. Enter the command **names(cigs)** into a chunk in the R Notebook and then run the chunk
2. The result is a list of the CIGS column names, ordered from left to right and top to bottom

Results can be turned into objects as well. For example, we can create a vector from the column names returned.

3. Enter the command **names(cigs) -> cigs_col_names** into a chunk in the R Notebook and then run the chunk
4. The result is a list of values appearing in the **Environment** window

As with OpenRefine presented yesterday (see [1.6 Data Cleaning](./1_5_data_cleaning.md)), we can also print unique values from a column to see what values are included. This can be done using the **unique()** function.

5. Enter the command **unique(cigs$transc_name)** into a chunk in the R Notebook and then run the chunk
6. This is a poor example, as most columns in CIGS actually will contain only unique values, but it is a very useful function in many other cases
7. Note here the introduction of the **$** to specify columns within a dataframe

### Loading a library

Introducing a filter to sort or subset records according to specific criteria is also possible, but somewhat cumbersome in base R. Here, we can load a library package called **dplyr**, which includes a good filter function

8. You can install a library package using **Tools > Install Packages...**  from the top menu bar, or by using the base function **install.packages()** in R
9. When **dplyr** is installed, enter the command **filter(cigs, accuracy == 3)**
10. This returns all records with an accuracy value of 3. Note that numbers are not in "" in R - unless they are characters
11. The results of a filter function can also be stored to a separate object, using the -> operator, for example **filter(cigs, accuracy == 3) -> cigs_acc_3**

## Manipulating data
Finally a few examples on how data can be manipulated. There are a number of ways to extract parts of a dataframe to a new dataframe using very simple syntax. 

With the **dplyr** library loaded, grouped summaries of a dataframe can be obtained using the **count()** function.

1. Enter the command **cigs %>% count(accuracy)** into a chunk in the R Notebook and then run the chunk
2. The result can be stored as a new dataframe

3. Selecting a specific number of rows in a dataframe, for example using [ ] to specify the range of rows and the range of columns (in that order). Compare the results of the two following examples
> **cigs[1:2, ]**<br>
> **cigs[1:2, 1:2]**


### A GLoW R Notebook for importing data dumps
In conclusion, let us demonstrate the application of R Notebooks in building large, annotated scripts for performing various tasks.