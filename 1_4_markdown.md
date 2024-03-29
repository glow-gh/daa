---
layout: default
title: "4. Markdown"
rank: 4
---
# Markdown
This module builds on the previous module (see [1.3 Markdown](./1_3_markdown.md)), and demonstrates how to commit files to GitHub using VS Code, and how to publish Markdown documents to the web using [GitHub Pages](https://pages.github.com).

## Introduction
[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language for creating formatted text for online use. A [Markdown]([Markdown](https://daringfireball.net/projects/markdown/)) file can also be used as a very powerful notepad to keep track of workflows, files and links. Markdown files can also be made to build individual pages to a public webpage, for example by using [GitHub Pages](https://pages.github.com) to publish Markdown files from a [GitHub](github.com) repository.

## Aims
Knowing how to create and set up Markdown files will provide you with a versatile plain text format able to include text, links, and basic visualisations that can be deployed in your personal workflow and online. Markdown files are widely used in blogging and for online documentation, especially on [GitHub](github.com). As such, they can combine note-taking and assignment writing with a light-weight format for publishing content to the web.

#### Applications
* [Visual Studio Code](https://code.visualstudio.com) - a versatile source code editor with built-in Git

#### Resources
* [The Markdown Guide](https://www.markdownguide.org)
* [Getting Started with Markdwon](https://programminghistorian.org/en/lessons/getting-started-with-markdown)

## Tasks
* [Commit a Markdown document to GitHub](#commit-a-markdown-document-to-github)
* [Publish a Markdown document with GitHub Pages](#publish-a-markdown-document-with-github-pages)
* [Adding an index page](#adding-an-index-page)

### Commit a Markdown document to GitHub
As you have been adding content to your Markdown document, you may have noticed that a counter has switched on on the **Source Control** menu icon in the left-hand **Activity Bar**. This indicates that pending changes to a given number of documents have been made.

In order to stage and commit these changes to GitHub from VS Code, we follow the same essential steps as demonstrated for GitHub Desktop in the previous module (see [1.2 GitHub](./1_2_github.md)).

1. Select the **Source Control** pane in the left-hand **Activity Bar**.

2. First locate the appropriate repository. This will be easy enough as you should only have one repository open (namely the **daa** repository).

3. From the **Changes** expandable list, select **first_markdown.md**, right-click and select **Stage Changes** (or simply press the '+'-symbol on the right)

4. You should now see a second expandable list appear, named **Staged Changes**. As with GitHub Desktop, this means that the changes has been staged, but not commited. If you select the file in the **Staged Changes** list, the editor viewer will open an index pane showing changes to the file.

5. To commit staged changes, click the check mark next to the name of the repository and enter a commit message.

6. To push the committed changes to GitHub, click the **More Actions...** button and select **Push**. 

7. Go to your GitHub account and check that the file has been added with the approproate commit message.

### Publish a Markdown document with GitHub Pages
Our last task will be to learn the basics of publishing Markdown documents to the World Wide Web using [GitHub Pages](https://pages.github.com). To do this, we will first need to confirm the necessary settings on the GitHub repository and select a theme: 

1. Check that the GitHub repository that we wish to publish from is set to **Public**
2. Check that **GitHub Pages** has been enabled for the repository in question
3. Select a theme. For the present exercise, we will use the **Minimal** theme.

To publish Markdown files on [GitHub Pages](https://pages.github.com), we need to introduce a couple of files to control the appearance. A common file format used to control appearance for text content written in Markdown is **YAML**, with the file extension **.yml**.

4. Create a new file named **_config.yml** and make sure that it is stored in the same directory as **first_markdown.md**.

5. Save the below code to this file:

```
theme: jekyll-theme-minimal
title:  [Your name] - DAA 2022
description: My GitHub Page
show_downloads: false
```

6. Create a folder named **_data** in the same directory

7. Create a file named **toc.yml** in this directory (**daa/_data**), and save the below code to this file:

```
toc:
- title: First Markdown
  url: first_markdown.html
```

If you want to add further items to this list, simply repeat the latter two lines below. Note that YAML syntax is notoriously sensible to typing errors, so one open space too many or too few will break the script.

8. Create a folder named **_layouts** in the **daa** directory

9. Add the file named [default.html](./_files/default.html) (available at [glow-gh/daa/_files](https://github.com/glow-gh/daa/tree/main/_files/default.html) to your (**daa/_layouts**) folder. This file involves a more complex .html-script. You are welcome to contact module teachers for input on how to change it if desired.

10. Add the file named [post.html](./_files/default.html) (available at [glow-gh/daa/_files](https://github.com/glow-gh/daa/tree/main/_files/post.html) to your (**daa/_layouts**) folder. This file involves a more complex .html-script. You are welcome to contact module teachers for input on how to change it if desired.

11. Lastly, we will need to add a header to **first-markdown.md**, so that the YAML files know what and where to place the various elements in the file on GitHub Pages. A YAML header is inserted at the very top of a Markdown document (l. 1). Here, insert the following:

```
---
layout: default
title: "First Markdown""
rank: 1
---
```

12. Finally, all of the revised and newly created files need to be committed and pushed to your GitHub repository.
13. Go to the corresponding GitHub Pages address of the repository. The URL can be found under **Settings** tab of the GitHub repository.

### Adding an index page
The home- or landing page of your GitHub Pages webpage will show the contents of the repository README.md by default. You would prefer to have another Markdown file here, as a README.md is not intended as a webpage introduction text. What you should do is create and add to the same directory as your **first_markdown.md** another Markdown file named **index.md**. This will then be automatically inserted as the landing page text of the webpage.

## Summary
This module has taught you how to commit Markdown documents to GitHub and how to build a small webpage from these files, using YAML and HTML-files to structure webpage content. A GitHub Pages webpage can be used to publish assignments or small projects and to share information or ideas with others. This module has not offered a more in-depth introduction to .yml or .html that is needed to structure a GitHub webpage, but you are welcome to contact Rune Rattenborg ([rune.rattenborg@lingfil.uu.se](mailto:rune.rattenborg@lingfil.uu.se)) if you want input on how to alter the structure or add further elements.


## Further reading
* [The Markdown Guide](https://www.markdownguide.org) for copious documentation on Markdown formatting and use with GitHub Pages.
* [On Jekyll navigation](https://jekyllrb.com/tutorials/navigation/) for additional information on setting up YAML files and associated .html-code, please see the below webpage.





