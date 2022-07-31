---
layout: default
title: "2. GitHub"
rank: 2
---

# GitHub
This module will introduce you to [GitHub](github.com) and the use of the distributed version control coding language Git. The aim is to provide you with the skills to manage and monitor data and text files for research in an online multi-user environment, and to give you some experience in the basics of version control for keeping track of files.

## Introduction
[GitHub](github.com) is an online hosting service for software development and version control, built around [Git](https://git-scm.com), a free and open-source distributed version control system.

The good thing about [GitHub](github.com) is that it provides you with an online and highly versatile platform for creating, storing, sharing, and publishing text and data. So, to keep all of the files and scripts that you will be producing during the [Digital Applications in Assyriology Nordic Summer School](./index.md) in one easily accessible place, we thought it best to start out by introducing you to [GitHub](github.com).

## Aims
With a [GitHub](github.com) user account, you will be able to store and publish virtually any type of file from a remote location, while being able at the same time to create, edit, and upload files from a local work station with detailed version control. This means that you will also be able to restore previous versions of data files if anything goes wrong, and that you will be able to share data with other users on [GitHub](github.com) - and make use of theirs too!

This class will take you through the following processes:

* [Create a personal GitHub account](#create-a-personal-github-account)
* [Set up a GitHub repository](#set-up-a-github-repository)
* [Clone a repository](#clone-a-github-repository)
* [Create and push a file to GitHub](#create-a-commit-to-github)

#### Applications
* [GitHub Desktop](https://desktop.github.com) - a desktop client application maintained by GitHub

#### Resources
* [GitHub Docs](https://docs.github.com/en) - documentation and tutorials for everything GitHub
* [GitHub Desktop](https://docs.github.com/en/desktop) - GitHub Docs subsection on GitHUb Desktop

## Tasks
### Create a personal GitHub account
1. To create a GitHub personal user account, first go to [www.github.com](www.github.com) and choose **Sign up**.
2. Enter an e-mail and a password
3. Enter a user name
4. Access your user profile

Take a moment to familiarise yourself with the user interface. Note that your user profile has a URL, with the format **https://github.com/** followed by your user name. This user profile is publicly accessible by default.

Through **Edit profile** on the left, you can add links to your personal website, Twitter handle, and include a short bio. In the **Search** field in the top left corner, you can search for users, repositories, projects, and organisations.

In the **Search** field, try searching for **cdli_gh**. The results will be sorted according to type, with **Repositories** at the top. Scroll down to **Users**, and select **CDLI cdli-gh** from the results list.

You have now reached the GitHub organisation page of the [Cuneiform Digital Library Initiative](http://cdli.mpiwg-berlin.mpg.de). If you choose **Follow** on the right, you can follow this organisation, which means that you will receive notifications to your own user profile about activities by the users and organisations that you are following.

With a GitHub account, you can then follow, inspect, and reuse data and code published by other GitHub users and organisations.

### Set up a GitHub repository
Now, let us proceed to create a file directory, or a **repository**, as it is called on GitHub. When you have created a GitHub user profile, you also need a repository in order to work with and store files and data associated with that user profile. Essentially, a repository is a file directory, just like a folder on a computer.

1. From your user profile, choose the **Repositories** tab. This will give you an overview of the repositories belonging to your user profile.
2. Now, choose **New** to create a new repository
3. You will be required to name your repository. Give your repository the name **daa**
4. Set the repository to **Private**
5. Be sure to check **Add a README file**
5. Choose **Create repository**

You should now have a repository named **daa** associated with your GitHub account. Note that this also will have received a dedicated URL, namely **https://github.com/yourusername/daa/**. 

### Clone a GitHub repository
The point about a distributed version control system such as GitHub is that you can store files with an online hosting service _and_ work on those locally, either individually or as a group.

This is done by **cloning** a repository on your online GitHub user profile to your local drive. To work with cloned GitHub repositories on your local drive, you will usually need a GitHub desktop client. For this task, we will use [GitHub Desktop](https://desktop.github.com), but later today, you will also be introduced to code editors with built-in Git capability (see [1.3 Markdown](./1_3_markdown.md)). A good source code editor can essentially speaking perform most of the tasks that you will need a desktop client such as [GitHub Desktop](https://desktop.github.com) for, _and_ allow you to add, delete, and edit files in your cloned repositories at the same time.

For now, let's go with [GitHub Desktop](https://desktop.github.com). Through this link [(https://desktop.github.com)](https://desktop.github.com), you can download and install the [GitHub Desktop](https://desktop.github.com) client on your laptop. Please do so before continuing.

To clone a GitHub repository to your local drive, you should first decide on where on your local drive this repository should be located. It's a good thing to think a couple of steps ahead, and if you want to work more with GitHub files, you will most likely be needing more repositories in the future for your projects. The easiest thing is to keep all of your cloned repositories in a similar location on your local drive.

1. On your local drive, navigate to your **User/Documents** directory
2. Create a new folder in this location named **github** (do not use capital letters)
3. Now, go back to your GitHub user profile online and navigate to your **daa** repository.
4. Choose **Code** and select **Open with GitHub Desktop**
5. From the pop-up window, check that the URL of the repository is correct. The repository path should be **https://github.com/yourusernamer/daa**. Below, check that the path on your local drive is correct. It should be **yourusername/Documents/github/daa**.
6. Press **Clone**.
7. You should automatically be returned to **GitHub Desktop**.
8. Check that the repositories pane on the left now has **daa** as the current repository.

Because [GitHub Desktop](https://desktop.github.com) is not a text or code editor, but a file management application, you cannot see the files included in the **daa** repository before changes have been made in these files.

9. From the three options in the center pane, choose **Show in Finder**
10. You should now see the contents of the **daa** folder in your **Finder** (for MacOS) or **File Explorer** (for Windows).
11. Open the file **README.md** in your default text editor, either **TextEdit** (MacOS) or **Notepad** (Windows).
12. Add your name and email in the second line, below **# daa**.
13. Save and close the text editor.

### Create a commit to GitHub
What you have done now is to add changes to a file which is part of a cloned GitHub repository. This means that you now have two different versions of the **README.md**; one in your online GitHub repository, another on your local drive. To update the the version online with the changes on your local drive, you will now need to make a **commit**. A **commit** pushes the file version stored on your local drive to the online repository, thus updating the online **master** version to correspond to your local version.

If you return to the [GitHub Desktop](https://desktop.github.com) interface, you will see that the **README.md** has appeared in the left-hand **Changes** pane and is marked with a yellow square tag. The yellow square tag indicates that the file has been **modified**, and in the main pane you can see a summary of the changes constituting these modifications. Most file managers and IDEs with embedded Git employs a simple colour coding for file changes:

colour | meaning
-------|----------
 <span style="color:green">green</span> | New or untracked file
<span style="color:yellow">yellow</span> | Modified file
<span style="color:red">red</span> | Deleted or removed file

To update the online version of the file with these modifications, let us go through the various steps of making a **commit** and **pushing** a file to GitHub. This may sound overly complicated to start with, but as we will see, there are good reasons for every step of this process.

Whenever you have completed and saved edits to a file, the file will be listed as **modified** in the **Changes** pane of GitHub Desktop. This merely means that GitHub Desktop has registered a change in the file relative to the last version of the file logged by the embedded Git, but this change has not been stored or distributed anywhere else.

1. To commit these changes to the online version, you will first need to **stage** the changes to the file. In **GitHub Desktop**, this is done by checking the box next to the file name in the **Changes** pane.
2. Then, you will need to write a summary of the commit and - when necessary - a more detailed description of the cnahges included in this commit in the box in the bottom left corner.
3. A **commit message** is the best and easiest way of keeping track of what changes you made to a file in a specific version, and so it is worth your while to provide a clear and concise **commit message** at all times.
4. When you have typed in a **commit message**, click **Commit to main** below.

To **commit** changes to a file means that the changes to the currently saved local version will be committed to the version control system Git. This stores a snapshot of the current version and changes relative to previous versions on your local harddrive. The various Git versions of a file can be inspected in **GitHub Desktop** by clicking the **History** tab next to the **Changes** tab in the lefthand window

In order to forward these changes to the version of the file stored online on your GitHub account, an additional step is needed. This is called a **push**, in that it pushes the commit to the relevant GitHub repository. If multiple people are working on files from the same GitHub repository, you would also occasionally want to update your local files from the versions stored in the GitHub repository. This is called a **pull**. Performing a **push** and a **pull** at the same time is called a **sync** (as we will see in the next module, cf. [1.3](./1_3_markdown.md))

5. To **push** the commit to your GitHub repository, please locate the button in the top bar marked with an ↑ and the label **Push origin**. When no commits have been made that require pushing to GitHub online, the label will say **Fetch origin** (should you want to make a **pull** from the repository version online).
6. To push your **commit**, simply press the button saying **Push origin**. Upon a succesful commit, the button should revert to saying **Fetch origin**, indicating that no **commits** remain on your local drive that have not been pushed to GitHub online
7. To verify that the changes have been successfully pushed to the repository, go to the online GitHub repository and confirm the updated commit message for the **README.md**.

### Branches in GitHub repositories

As a final note, we have not dealt with **branches** of a GitHub repository in the present module. The core version of a repository on GitHub is called **main**, and what we have done so far has been to pull and push commits directly to and from the **main** branch. When becoming more accostumed to the GitHub workflow, and especially when multiple users are working on the same repository, it is not advisable to constantly make changes directly to the **main** branch of a repository, as this is liable to cause inconsistencies between the changes that you and others make. 

#### Creating branches and forks

Instead, when you want to work on developing a feature or document without having to include changes that other users are making on the main version of the repository, it is advisable to create a new **branch** from the main **branch** and work on this branch instead.

Note that you can only create a **branch** from a repository if you have **write access** to this repository. 

You can read a lot more about this under the GitHub Docs [Working with branches](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches) entry.

If you do not have **write access**, the corresponding action is called a **fork**. A fork can be performed on any public GitHub repository by any GitHub user, and is designed to allow users to further develop and augment code and documentation prepared by other users or projects. A **fork** is then essentially a **clone** of a GitHub repository to which you yourself do not have access rights.

You can read more about forks under the GitHub Docs [About forks](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks) entry.

#### Merging
In order to integrate your work on a separate branch with the main branch of the repository, you will subsequently need to create a **pull request** (typically referred to as a **PR** in GitHub jargon). Once accepted by the repository manager (yourself or someone else with editorial access), changes in the _head_ branch (the one you have been working on) are included in the _base_ or _main_ branch (the primary repository branch), and the _head_ branch can be deleted.

More information about pull requests and merging are available from the GitHub Doc [Collaborating with pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests) entry.

## Summary
To conclude, this module has taught you to set up and use a GitHub account and repository for local editing and online storing of files, and how to maintain version control using Git to oversee changes in this files. When thinking about it, this setup can be used to work with a wide range of materials in a flexible way while maintaing the ability to backtrack and correct errors in previous edits. A GitHub account and repository will also enable you to prepare and publish projects online using **Markdown** and **GitHub Pages**, something that we will cover in the next module.
