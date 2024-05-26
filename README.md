# Git and GitHub

Git is a version control software. In one way or the other you may need to use a git and a GitHub together.

You need to use git and GitHub either to store your projects on the cloud or to collaborate with your team. This means it allows developers or writers to work on the same project even if they are located in different locations.

Version control is a means of recording changes to a file or set of files over time so that you can recall specific versions later.

If you prefer watching the tutorial click this [link](https://www.youtube.com/watch?v=9cCApTLb_Io&list=PLbvhRHYrmshSCAHZbibqh_px_LxnU54dk)

### 1. Install Git

First, you need to install the version control software, Git.

- Git:
  Install [git](https://git-scm.com/downloads)

### 2. Checking status of the repository

The _git status_ command allows you to know the status of the project:
If it is

- initiated
- modified
- staged

We can write the command _git status_ at any time. It is a means to to check what is happening on your project.

### 3. Configure your name and your email

Open the Git bash if your device is Windows, or open the Mac terminal if your device is MacOS and then write the following commands

```shell
git config --global user.name 'yourname'
git config --global user.email 'youremail'
```

### 4. Create a local git repository

In this step, you will create a folder (directory) for your project. A project is just a simple folder that stores all the files related to a certain project. A local repository is a project or a folder that is on your computer.

If your Git bash is not opened, go to start and type git bash. Git terminal will popup on Windows devices. If it is MasOS just open the Mac terminal. On the terminal write:

```shell
mkdir project_name
cd project_name
```

By the way, you can also create the folders the usual way using on the GUI(Graphical User Interface) of Windows or Mac.

### 5. Initialize Git

After creating a new local repository or in an existing local repository, initialize the repository by the following command:

```shell
   git init
```

Once, the repository is initialized git tracks the changes in the files and folders of the project.

### 6. Add file to the staging area

The file can be added to the staging area in multiple ways.
To add a single file, we use the _git add_ command followed by a file name

```shell
   git add filename
```

To add multiple files using their file names using the command _git add_ followed by file names

```shell
   git add filename1 filename2
```

Sometimes, we may make a lot of changes, and adding files one by one is tiring and not product. Therefore, we can use a short and product way. The _git add_ command followed by a dot allows adding files and folders at once to the stage area. Remember, there is a space between the add and the dot.

To add all files and folders at once

```shell
   git add .
```

To add and commit at the same time

```sh
  git commit -am 'commit message'
```

### 7. Unstage a file

```shell
    git reset HEAD filename
```

### 8. Commit the changes

Commit means taking a snapshot or a copy of your file at that point in time. You may associate it with saving a file with a new name (save as).

```shell
   git commit -m 'your message'
```

Your commit message has to be associated with the changes or modifications you make.

### 9. Git log

The _git log_ command allows knowing the commit history of the project. It list down all the commit history

### 10. Git log --oneline

The **git log --oneline** command allows to list minified log history

### 11. Git log -<limit>

For instance, this **git log --5** command list 5 commit history.

### 12. Git check out

We can identify the commit id of each commit using the _git log_ command. Then we can make use of this id to retire any previous commit.

```sh
git checkout commit-id
```

### 13. Creating a branch

We can create a copy of the master(main) using a branch. You built an awesome application. You like to keep this awesome application as it is but you like to add some features.
This is the time, you need branching the master. The branch is the copy of the master at branching instant. After branching, the branch and the master don't see each other. You can create as many branches as you want.

To create a branch:

- Only to create branch

```shell
    git branch  branch-name
```

- To create and checkout to the branch at the same time:

```shell
    git checkout -b branch-name
```

To switch between branches:

```shell
    git checkout main
    git checkout branch-name
```

To list down all the branches:

```shell
    git branch
```

### 14. Create account on GitHub

Now, create an account on GitHub and sign in using your emails and password

- GitHub
  Sign up on [GitHub](https://github.com/)

### 15. Create Repository on GitHub

Go to [GitHub](https://github.com/) and create a repository by click the plus icon on the top right corner.

### 16. Connecting git with remote repository

In this step, you will connect your local git repository with your remote GitHub repository

```shell
    git remote add origin remote_repository_ul
```

The word origin could be any word. It is a means to assign the repository URL.
If this is step is passed without error, you are ready to push it to your remote GitHub repository. Push means actually uploading what you have on your local to remote repository.

### 17. Push

Before you push(upload), please commits any changes and if it is ready push your files to your remote GitHub repository using the following command.

```shell
    git push -u origin master
```

### 18. Merge

When you work on an individual project or a team project you may have different branches. Mostly you will have a master(main), develop and other branches. Then you will merge other branches to your develop and your develop to master. It is possible to merge any branches. For instance, lets merge feature branch to develop

```shell
    git checkout develop
    git merge feature
```

Using the above code, now the develop and feature branches do have the same content

### 19. Pull

If your team merges new features to the develop, then you will be behind, now you need to make your project to the current stage by pulling from develop

```shell
    git checkout yourbranch
    git pull origin develop
```

```sh
    git checkout develop
    git merge yourbranch
    git push -u origin develop
```

If you are a sole developer that works by yourself then you can test the _git pull_ command by modifying some of the files from your remote repository and pull it using the _git pull_ command.
