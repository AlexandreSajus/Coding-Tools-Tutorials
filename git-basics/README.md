# Overview
Version control is a critical tool for an efficient workflow. It allows you to follow progress on your project, track changes between versions and efficiently collaborate on text files. 
The most commonly used version control tool is [**Git**](https://git-scm.com/)
Once installed, you can used git inside your terminal using commands that start with `git`
However, as there are a lot of commands to remember, it is recommended to use a graphical user interface (GUI) to interact with git to make your work easier.

A few of the most common GUI for git are :
- Visual Studio Code and Pycharm have integrated Git support
- The Git extension of JupyterLab
- [Sublime Merge](https://www.sublimemerge.com/), made by SublimeHQ, the company behind Sublime Text

However, despite these tools helping you use Git quickly, you still need to understand the main concepts of Git to use it efficiently.

# Commits
A commit is a group of modifications. This includes adding a line to a file, renaming a file, deleting a file, etc. Every version of your project is a represented by an ordered list of commits that represent the modifications needed to go from an empty folder to your full project.

## Making new commits

To create a new commit, you use the `git commit` command or you press a *Commit* button inside your GUI, after selecting the modifications you did that you want to include in your commit.

## Commit names
Every commit has a name, in the form of a hexadecimal string like "24c47f7e534fe24ec91aecb8c34674fd4e3f23a6". This string (or just the first 10 characters like "24c47f7e53" in this example) can be used to refer to the commit.

## Parent commits
Every commit (except the first one) has at least one parent commit. The set of all commits creates a tree-like structure that represents the different versions of your project. When browsing your project at a specific commit, you are seeing the modification of this commit and all it's ancestors.

## Commit messages
Every commit also *must* have a message, a piece of text (that can be as long as you want), that describes the changes made in this commit. This can be useful to remember what the changes introduced by a commit did.

# Branches
Branches are movable pointers that point to a specific commit. Because commits have hard-to-remember hexadecimal names, branches are a way to give an easy to remember name to a specific commit.

In general, your project will have a "main" or "master" branch that represents the latest stable version of your project.

When you add a commit to a project, you must always be at a specific branch. The addition of the commit will move the branch forward so that it always points to the latest commit. Branches work like branches in tree that grow, commit after commit.

## Moving between changes
You can move between branches using `git checkout <branch-name>` or the *Checkout \<branch-name\>* button in your GUI. This will change the state of your project to the branch you selected so that you can work on another version of your project. 

## Editing branches
You can create a new branch at any moment that points to any commit you want and you can also delete branches. 

# Merges
Merges are a special type of commit that have more than one parent. Usually, you have multiple branches that each contain a feature you want, so you want to merge them into a single branch.
To do this, you can use the `git merge` command or the *Merge \<source-branch\> into <\target-branch\>* button in your GUI.
This will create a new commit at the target branch that contains the modifications of the source branch.
Git will try to do this automatically, but sometimes, it does not work, for example, when source branch and target branch both modify the same line. In this case, Git will warn you that a "*Conflict*" occured and you will have to manually edit the corresponding files to chose the correct modification.
Afterwards, you can tell git that you resolved the conflict and Git will proceed by generating the Merge commit.

When you are resolving a conflict, you cannot do anything else like adding new commits, so be careful before merging that you are ready for the merge. If you were not ready, you can always cancel the merge.

# Remotes
Remotes are URLs that allow you to share your project with other people. While anybody can create and host a remote, most commonly, you will use [GitHub](https://github.com) (or [Gitlab](https://gitlab.com/explore)) to host and share your projects. 

Most projects only use one remote and every member of the project uses this remote for collaboration, but this is not required.

Remotes have names. By default, the main remote has the name "origin".

Remotes act as a copy of your project that is located on another computer. If changes are introduced in this distant project, you can use the `git pull` command (Or *Pull* button) to get the changes that occured on the branch you are currently working on. You can also use the `git push` command to send the commits you added to the branch you are to the distant computer.

For an existing project that is available in a remote, you can use the `git clone <remote-url>` command to get a copy of the project on your computer and start working on it.

Git is a decentralized version control system, which means that you can use it even when you are offline, but the `pull` and `push` commands won't work.

## Branches in remotes

To distinguish between a branch on your computer and a branch on the remote computer, you can check its name. Distant branch names start with the name of the remote. For example, you might have a "`main`" branch on your computer and a "`origin/main`" branch on the remote computer.

## Merges in remotes

If both you and the distant branch introduced commits on the same branch, git will (if possible) [merge](#Merges) the commits automatically. Because this can introduce conflicts, it is advised to that every person on a project works on a separate branch and merges only when there are done to avoid unexpected merge conflicts. 