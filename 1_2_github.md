# GitHub
## Introduction
[GitHub](github.com) is an online hosting service for software development and version control, built around [Git](https://git-scm.com), a free and open-source distributed version control system.

The good thing about GitHub is that provides you with an online and highly versatile platform for creating, storing, sharing, and publishing text and data. So, to keep all of the files and scripts that you will be producing during the **Digital Applications in Assyriology Nordic Summer School** in one easily accessible place, we thought it best to start out by introducing you to GitHub.

This class will take you through the following processes:

* [Create a personal GitHub account](#task1)
* [Set up a GitHub repository](#task2)
* [Clone a repository](#task3)
* [Create and push a file to GitHub](#task4)

###### Applications
* [GitHub Desktop](https://desktop.github.com) - a desktop client application maintained by GitHub

## Tasks
### <a id="task1">Create a personal GitHub account</a>
1. To create a GitHub personal user account, first go to [www.github.com](www.github.com) and choose **Sign up**.
2. Enter an e-mail and a password
3. Enter a user name
4. Access your user profile

Take a moment to familiarise yourself with the user interface. Note that your user profile has a URL, with the format **https://github.com/** followed by your user name. This user profile is publicly accessible by default.

Through **Edit profile** on the left, you can add links to your personal website, Twitter handle, and include a short bio. In the **Search** field in the top left corner, you can search for users, repositories, projects, and organisations.

In the **Search** field, try searching for **cdli_gh**. The results will be sorted according to type, with **Repositories** at the top. Scroll down to **Users**, and select **CDLI cdli-gh** from the results list.

You have now reached the GitHub organisation page of the [Cuneiform Digital Library Initiative](http://cdli.mpiwg-berlin.mpg.de). If you choose **Follow** on the right, you can follow this organisation, which means that you will receive notifications to your own user profile about activities by the users and organisations that you are following.

### <a id="task2">Set up a GitHub repository</a>
Now, let us proceed to create a file directory. When you have created a GitHub user profile, you also need a repository in order to work with and store files and data associated with that user profile. Essentially, a repository is a file directory, just like a folder on a computer.

1. From your user profile, choose the **Repositories** tab. This will give you an overview of the repositories belonging to your user profile.
2. Now, choose **New** to create a new repository
3. You will be required to name your repository. Give your repository the name 'daa'
4. Set the repository to **Private**
5. Be sure to check **Add a README file**
5. Choose **Create repository**

### <a id="task3">Clone a GitHub repository to your local drive</a>
The point about a distributed version control system such as GitHub is that you can store files with an online hosting service _and_ work on those locally, either individually or as a group.

This is done by **cloning** a repository on your online GitHub user profile to your local drive. To work with cloned GitHub repositories on your local drive, you will usually need a GitHub desktop client. For this task, we will use **GitHub Desktop**, but later in the summer school programme you will also be introduced to code editors with built-in Git capability. A good source code editor can essentially speaking perform most of the tasks that you will need a desktop client such as **GitHub Desktop** for, _and_ allow you to add, delete, and edit files in your cloned repositories at the same time.

For now, let's go with **GitHub Desktop**. Through this link [(https://desktop.github.com)](https://desktop.github.com), you can download and install the **GitHub Desktop** client on your laptop. Please do so before continuing.

To clone a GitHub repository to your local drive, you should first decide on where on your local drive this repository should be located. It's a good thing to think a couple of steps ahead, and if you want to work more with GitHub files, you will most likely be needing more repositories in the future for your projects. The easiest thing is to keep all of your cloned repositories in a similar location on your local drive.

1. On your local drive, navigate to your **User/Documents** directory
2. Create a new folder in this location named **github** (do not use capital letters)
3. Now, go back to your GitHub user profile and navigate to your **daa** repository.
4. Choose **Code** and select **Open with GitHub Desktop**
5. From the pop-up window, check that the URL of the repository is correct. The repository path should be **https://github.com/yourusernamer/daa**. Below, check that the path on your local drive is correct. It should be **yourusername/Documents/github/daa**.
6. Press **Clone**.
7. You should automatically be returned to **GitHub Desktop**.
8. Check that the repositories pane on the left now has **daa** as the current repository.

Because **GitHub Desktop** is not a text or code editor, but a file management application, you cannot see the files included in the **daa** repository before changes have been made in these files.

9. From the three options in the center pane, choose **Show in Finder**
10. You should now see the contents of the **daa** folder in your **Finder** (for MacOS) or **File Explorer** (for Windows).
11. Open the file **README.md** in your default text editor, either **TextEdit** (MacOS) or **Notepad** (Windows).
12. Add your name and email in the second line, below **# daa**.
13. Save and close the text editor.

### Create a commit to GitHub

What you have done now is to add changes to a file which is part of a cloned GitHub repository. This means that Git has logged these changes on your local drive. It also means that you now have two different versions of the **README.md**; one in your online GitHub repository, another on your local drive. To merge the changes on your local drive with the version online, you will now need to make a **commit**. A **commit** pushes the file version stored on your local drive to the online repository, thus updating the online **master** version to correspond to your local version.

If you return to the **GitHub Desktop** interface, you will see that the **README.md** has appeared in the left-hand pane and is marked with a yellow square tag. The yellow square tag indicates that the file has been modified, and in the main pane you can see a summary of the changes constituting these modifications.

To update the online version of the file with these modifications, let us go through the various steps of making a **commit**.

1. There

```
This is a piece of code
```
