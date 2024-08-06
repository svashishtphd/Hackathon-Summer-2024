# BASE Team - Biomedical Data Science Hackathon 2024

## General Information
* Predictions must be written to the `prediction/prediction.csv` file to be scored.

* The scoreboard will be located [here](https://github.com/Rochester-Biomedical-DS/Hackathon-Summer-2024/Leaderboard.Hackathon.2024.md) once the competition begins.

* The competition runs through 2:59 PM EDT 17-August-2023. The predictions each team has committed to their repository at that time will be used to determine their final score.

# Working with Git and GitHub
Git is a method for **version control**, which allows you to record and see all changes that you and your team make over time to your code. All changes over the lifetime of the project are recorded every time you save your code, allowing anybody to go back to previous versions. GitHub is a hosting website that allows users to store their Git repositories remotely and work with other people on projects. 

There are two main locations for projects to be stored: **remotely** or **locally**. The version of the project available on GitHub is the **remotely** stored version of the project, while the copies on people's computers are the **locally** stored version of the projects. 

GitHub users can **clone** the **remote** version from GitHub to their own computer to create a **local** copy on their computer. Then, they can change and alter the files however they want. When multiple people work on the same file and try to update the **remote** copy on GitHub but have different changes, the files need to be **merged** to select which changes should be kept from both versions. This can get tricky, so its best if people work on files separately.

To work on files separately and only merge all of the changes at the end, Git uses **branches** branches allow for users to work on individual copies of the code where they can make as many changes as they want, then **merge** the changes to the **main** code at the end. This lets you make lots of changes freely and save your progress as you go without worrying about affecting other peoples work. 
> Note: Before you merge into the main repository, try to clean up your work as much as possible to reduce the work needed to merge the files (remove files that you aren't using anymore, remove output files that can be generated from the code, etc.)

## Getting Started:

### Cloning repositories

To download a repository to your own local computer, first you need to decide where you want to store your projects. I recommend making a folder called `github` where you can keep the local versions of your projects.

Open a terminal and navigate into your `github` folder. 

Use the command `git clone https://github.com/Luminarada80/Hackathon-Summer-2024.git` to create a **local** clone of the GitHub repository. This lets you work on everything locally, and is the main way that people share and distribute code on GitHub.

If you are working with other people and/or are going to be altering the files on GitHub, I recommend making a **branch** once you clone the repository. This will create a copy of the entire repository that you can alter without changing the **main** branch, keeping everything clean for other users. The **main** branch is the one that you see first when you go to someones github repository.

### Saving your progress

> **Important!** Save your progress often, when you are starting out it is easy to lose your progress by accidentally reverting your changes or overwriting your files from the remote repository. Dont include large files, as GitHub repositories have a 50 MB size limit. You can alter your `.gitignore` file to ignore files with certain filename extensions, such as `.csv`. This can help with keeping the size of the repository small. In general, try to just save code and small files to the remote repository, and use other storage methods such as Box or OneDrive to store large data files remotely.

**Staging changes**

Once you have made changes, you need to tell Git that you want to save the changes that you have made. You can see any changes by typing the command `git status` into your command line while in your project directory. **Unstaged changes** are changes that you made, but have not yet specified that you want to save. **Staged changes** are changes that you have made, and will be saved. To stage changes, you use the command `git add <file name>`. This will tell Git that you want to save this file. To stage all changes, use the command `git add .`. 

**Committing changes**

Once you have specified which changes you want to keep, you need to tell Git that you are done and want to save your progress. Use the `git commit -m "<commit message>"` command to commit your changes. 
> The **commit message** is a message describing which changes you made, so *be as detailed as possible* so that other people can keep track of what each person is working on and what has changed. 

**Pushing changes**

When you are ready to save your **local** changes to the **remote** repository on GitHub, you will `push` your commits.

In general, to save your work, you will use the following commands:
- `git add .` stage all of your changes
- `git commit -m "<commit message>"` to commit your staged changes with a message about what you did
- `git push` to push your saved changes to the remote repository.

**Pulling changes**

If your version of the code is behind, use the `git pull` command to update your **local** code with the **remote** version. This is useful if you are working on the same code across multiple computers or with other poeple to keep your code up to date. 

**Reverting unwanted changes**

If you accidentally make a commit that you dont want, you can use the following commands to go back to an older commit:

* `git log` will show you a list of your commits along with each commit's unique ID. Copy the commit ID of the commit you want to revert back to.
* `git revert <ID>` will revert everything back to the way the directory was at that commit.


### Branches
Each person should have their own branch for each feature they are working on. When you are done, you will **merge** your branch with **main** to combine your features with everyone elses.

**Working with branches in the command line**
* `git branch` will show you a list of the available branches (* denotes the current branch)
* `git checkout -b <branch name>` allows you to create a new branch
* `git branch switch <branch name>` allows you to switch to a new branch
* `git push --set-upstream origin <name>` specifies the upstream (remote) repository for the branch you're working on. This only needs to be done when first creating a new branch, in this case just use **main** as the origin name

