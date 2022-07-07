---
layout: default
title: "3. Markdown"
rank: 3
---

**NOTE: WILL BE EXPANDED TO TWO HOURS BEFORE AND AFTER LUNCH, REMOVE REGEX TO TUESDAY**

# Markdown
This module will introduce you to Markdown, a markup language that will allow you to create simple, yet powerful notepads, documents, and webpages. In addition, you will learn how to create, commit and publish Markdown documents to the web using GitHub Pages.

## Introduction
[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language for creating formatted text for online use. A Markdown file can also be used as a very powerful notepad to keep track of workflows, files and links. Markdown files can also be made to build individual pages to a public webpage, for example by using GitHub Pages to publish Markdown files from a [GitHub](github.com) repository.

## Aims
Knowing how to create and set up Markdown files will provide you with a versatile plain text format able to include text, links, and basic visualisations that can be deployed in your personal workflow and online. Markdown files are widely used in blogging and for online documentation, especially on [GitHub](github.com).

#### Applications
* [MacDown](https://macdown.uranusjr.com) (editor for MacOS)
* [ghostwriter](https://wereturtle.github.io/ghostwriter/) (editor for Windows)
* [Visual Studio Code](https://code.visualstudio.com) - a versatile source code editor with built-in Git

#### Resources

* [The Markdown Guide](https://www.markdownguide.org)
* [Getting Started with Markdwon](https://programminghistorian.org/en/lessons/getting-started-with-markdown)

## Tasks
* [Set up Virtual Studio Code](#vscode)
* [Create a Markdown file](#task1)
* [Understand Markdown text formatting](#task2)
* [Create anchors and hyperlinks](#task3)
* [Commit a Markdown document to GitHub](#task4)
* [Publish a Markdown document with GitHub Pages](#task5)

### <a id="vscode">Set up and prepare Virtual Studio Code IDE</a>

Before starting on the tasks just listed, we will need to equip you with a text and source code editor capable of pulling, managing and pushing files to your GitHub repository _and_ editing a wide variety of file formats. As noted in the previous section [(1.2 GitHub)](./1_2_github.md), [GitHub Desktop](https://desktop.github.com) is excellent for managing files with Git version control in cloned repositories locally, but it cannot provide you with an environment for creating and editing files. There are plenty of editors specifically for Markdwon available for free online, including e.g. applications such as [MacDown](https://macdown.uranusjr.com) (for MacOS) and * [ghostwriter](https://wereturtle.github.io/ghostwriter/) (for Windows).

To give you a feel for editors able to handle a wider range of file formats, we will use [Visual Studio Code](https://code.visualstudio.com), also commonly referred to as VS Code. VS Code is a type of [integrated developer environment (IDE)](https://en.wikipedia.org/wiki/Integrated_development_environment) software that combines a [source-code editor](https://en.wikipedia.org/wiki/Source-code_editor) with directory management and embedded Git. Though produced by Microsoft, VS Code is free and open-source, and available for Windows, MacOS, and Linux.

1. First, you will need to download and install [Visual Studio Code](https://code.visualstudio.com). Note that the application is free, but will require you to set up a Microsoft account (if you do not already have one). Otherwise, please follow the download instructions. Once you have downloaded and installed the software, please open VS Code.

2. In order to connect VS Code with your GitHub user profile, you will now need to download the [GitHub Pull Requests and Issues](https://code.visualstudio.com/docs/editor/github) extension. Once you have downloaded and installed this extension, return to VS Code.

3. When opening VS Code for the first time, you should see the applications starting page, which gives you a list of basic actions to perform. 

![Get Started pane in Virtual Studio Code](./images/image_1_3_vs_code_start.png "Get Started pane in Virtual Studio Code")

4. In order to make use of the GitHub repository that you set up in the last course module (see 1.2 GitHub), we should start by cloning your working repository to VS Code, so that you can pull and push files while editing.

To do so, please click **‘Clone Git Repository’**. Before you can clone a GitHub repository to VS Code, you will be required to login to GitHub via VS Code. Follow the instructions.

5. Now, once you are signed in via VS Code, you will be asked to choose which of the repositories associated with your account that you would like to clone. Choose the repository created in the last session (see **[1.2 GitHub](./1_2_github.md)**) that was named **daa**. 

Once this repository has been added to the Explorer window on the left, the repository will be tracked by the embedded Git of VS Code. Meaning that you can now pull and push edits to any file in this repository directly from VS Code. 

Let us just briefly go over the user interface of VS Code. From the menu buttons in the left-hand Activity Bar, you should have the following options:

* Explorer
* Search
* Source Control
* Run and Debug
* Extensions
* GitHub

\- and in the bottom left of the same ribbon:

* Accounts
* Manage

6. Before we start working with Markdown, it will also be good to save your repository as a dedicated workspace. A workspace or project makes the management and backup of multiple files considerably easier. You can save the current Explorer directory as a working space by choosing **File > Save Workspace As….**. Please name the workspace **daa**

### <a id="task1">Create a Markdown file</a>
You can now start working with the editing of files. A Markdown file uses the file extension **.md**. You can create a wide range of files in VS Code by applying the appropriate file extension upon first save. 

1. To create a Markdown file, simply choose **File > New Text File...**
2. This will open a new and empty editor window. To save the untitled text file as Markdown, choose **File > Save** and name file **first_markdown.md**
3. The bottom status bar in VS Code should now reflect that the document being edited is a Markdown file

### <a id="task2">Understanding Markdown text formatting</a>
Markdown is a lightweight markup language, which is easy and intuitive to work with. You can find several guides to Markdown online, but generally they will all cover about the same range of formatting elements as those included on this cheat sheet - [https://www.markdownguide.org/cheat-sheet/](https://www.markdownguide.org/cheat-sheet/).

1. <p>Because Markdown is a basic markup language for plain text, you would probably wnat to know what the output looks like while you are editing it. To turn on a preview pane for your **first_markdown.md** in VS Code, click the **Open Preview to the Side** icon in the top right corner.<br><br>You should now be able to see the Markdown code and the actual output side-by-side.</p>

2. The primary structuring element in a **.md**-file are the headers. These are preceded by **#**, **##**, **###** and so on in descending order over six levels. Below is the format first as entered, then as output:

```
# Header
## Header
### Header
#### Header
##### Header
##### Header
```

\```
# Header
## Header
### Header
#### Header
##### Header
##### Header
\```

3. No specific fond types are possible with Markdown, but they can be implemented with HTML. Standard formatting elements, such as **bold** and _italics_ are, however, included.

```
**bold**
_italics_
~~strikethrough~~
~superscript~
```

\```
<br>**bold**<br>
_italics_<br>
~~strikethrough~~<br>
\```

4. It is possible to create a number of different lists, numbered, bullet points, and checkboxes.

```
1. first
2. second
3. third

* first point
* second point
* third point

- [ ] first box
- [ ] second box
- [ ] third box
```

\```
1. first
2. second
3. third

* first point
* second point
* third point

- [ ] first box<br>
- [ ] second box<br>
- [ ] third box<br>
\```

5. It is also possible to make simple tables, using the syntax given below:

```
column1 | column2 | column3
--------|---------|-----------
cell1 | cell4 | cell7
cell2 | cell5 | cell8
cell3 | cell6 | cell9
```

\```
column1 | column2 | column3
--------|---------|-----------
cell1 | cell4 | cell7
cell2 | cell5 | cell8
cell3 | cell6 | cell9
\```

### <a id="task3">Create anchors and hyperlinks</a>
Another very useful feature in Markdown documents is the ability to create links internally in the text (also called 'anchors' or 'flags') and hyperlinks to external resources, including files and websites.

1. A basic hyperlink in Markdown format is generated by placing square brackets **[]** around the linked text, and the link itself in parenthesis **()** immediately after the text to be linked. Thus, a link to your own GitHub user profile could look like this:

```
[My GitHub user profile](https://github.com/yourusername)
```
\```
<br>[My GitHub user profile](https://github.com/yourusername)<br>
\```

2. The same syntax is employed if you want to create a link to another file located in the same directory as the file you are editing. Here, you can use '**./**' before the file name, which will then refer the link to the same directory location. Thus, a link to the README.md file already in your **daa** repository could look like this:

```
[README.md](./README.md)
```

\```<br>
[README.md](./README.md)<br>
\```

### <a id="task4">Commit a Markdown document to GitHub</a>
As you have been adding content to your Markdown document, you may have noticed that a counter has switched on on the Source Control menu icon in the left-hand Activity Bar. This indicates that pending changes to a given number of documents have been made.

In order to stage and commit these changes to GitHub from VS Code, we follow the same essential steps as demonstrated for GitHub Desktop in the previous module (see [1.2 GitHub](./1_2_github.md)).

1. Select the **Source Control** pane in the left-hand Activity Bar.

2. First locate the appropriate repository. This will be easy enough as you should only have one repository open (namely the **daa** repository).

3. From the **Changes** expandable list, select **first_markdown.md**, right-click and select **Stage Changes** (or simply press the '+'-symbol on the right)

4. You should now see a second expandable list appear, named **Staged Changes**. As with GitHub Desktop, this means that the changes has been staged, but not commited. If you select the file in the **Staged Changes** list, the editor viewer will open an index pane showing changes to the file.

5. To commit staged changes, click the check mark next to the name of the repository and enter a commit message.

6. To push the committed changes to GitHub, click the **More Actions...** button and select **Push**. 

7. Go to your GitHub account and check that the file has been added with the approproate commit message.

### <a id="task5">Publish a Markdown document with GitHub Pages</a>
Our last task will be to learn the basics of publishing Markdown documents to the World Wide Web using GitHub Pages. To do this, we will first need to confirm the necessary settings and select a theme: 

1. Check that the GitHub repository that we wish to publish from is set to **Public**
2. Check that **GitHub Pages** has been enabled for the repository in question
3. Select a theme. For the present exercise, we will use the **Minimal** theme.

To publish Markdown files on GitHub Pages, we need to introduce a couple of files to control the appearance. A common file format used to control appearance for text content written in Markdown is **YAML**, with the file extension **.yml**.

4. Create a new file named **_config.yml** and make sure that it is stored in the same directory as **first_markdown.md**.

5. Create a folder named **_data** in the same directory

6. Create a file named **_toc.yml** in this directory (daa/_data), and save the below code to this file:

```
docs_list_title: My DAA page
docs:

- title: First Markdown
  url: first_markdown.html
```

7. 

**TO BE COMPLETED**





