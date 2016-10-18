# learn-git
An introduction to collaboration using Git and Github.

## Introduction
This learning journey will help you acquire the skills to collaborate using Git and Github. Anyone is welcome to fork it and learn!

## Requirements
To start off, we first need two things: *Git* and *Github* account.

- [Git](https://git-scm.com/) is a version control system that is used for development of codes/software and other version control tasks. It allows multiple parties to collaborate on a single project/document (in this case the tex file) without ruining each other's version. To start collaborating the Git way, you will need a distribution of Git on your machine.
  - for Windows users I suggest getting the Git for Windows Portable [32bit](https://github.com/git-for-windows/git/releases/download/v2.10.1.windows.1/PortableGit-2.10.1-32-bit.7z.exe)/[64bit](https://github.com/git-for-windows/git/releases/download/v2.10.1.windows.1/PortableGit-2.10.1-64-bit.7z.exe)
  - for Mac users, one can do the installation by following the instructions [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

- GitHub is a web-based Git repository hosting service. It offers all of the distributed version control and source code management (SCM) functionality of Git as well as adding its own features. You can think of Github as a Dropbox for codes instead of general files and folders. If you have have a Github account, sign in to your account, otherwise you can signup for a Github account [here](https://github.com/).




## How to Git?

Assuming that you have a Github account (and signed in) and Git distribution on your machine we are ready to start! Start up your Terminal or PortableGit for Mac and Windows system respectively. We shall go through some simple commands required to maneuver around Terminal or PortableGit.

**Basics**

|  Command            | Function                                               |
|:-------------------:|--------------------------------------------------------|
| `pwd`               | Returns the present working directory.                 |
| `cd`                | Goes back to the home directory.                       |
| `cd ..`             | Jumps back up one directory.                           |
| `ls`                | List the files in the directory you are in.            |

Tip: `pwd` is used to check which directory you are in, `cd` to change to the directory that you want to access, `ls` is for you to check if the file you are trying to access is in that directory. Use them to navigate around the directories and find your files :)

Protip: Use `tab` to auto-complete your file names.

**Forking a repository**

A *fork* is a copy of a repository. Forking a repository belongs to you and thus allows you to freely experiment with changes without affecting the original project. You might fork a repository in order to propose changes to the original project, build on something new based on the project. Here we will fork this repository and propose changes to this project. To fork this project, click on the `Fork` on the top right hand corner below your profile picture.


**Cloning a repository**

Once you fork a repository, it will bring you to a repository that now **belongs to you** but contains exactly the same files the repository that you forked. This allows you to clone it to your machine and edit/experiment with the files in it any way you like till your hearts content.

```git
git clone https://github.com/*yourusername*/*nameofrepo* *foldername*
```
if `*foldername*` is left empty, the folder name will be `*nameofrepo*`. After cloning a repository, you need to `cd *foldername*` to enter the directory/repository.

**Checking the status of the repository**

Once inside you can,

```git
$ git status
```
which you will see

```git
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Nothing to commit, working tree clean
```

**Making changse to your files**

Notice the typo in the above? Access the `README.md` file in the repository that you cloned to your machine, rectify the spelling mistake and save!
Now if you do a `git status` again, you will get:

```git
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be commited)
  (use "git checkout -- <file>..." to discard changes in working directory)
      modified:     README.md
no changes added to commit (use "git add" and/or "git commit -a")      
```

this means that you have made some changes to your files and have not commited it. One can think of committing as double confirming that the changes you have made is really what you want. But before committing your files, you have to stage them first, [which is to prepare your files for commit](http://programmers.stackexchange.com/questions/119782/what-does-stage-mean-in-git). Lastly, whenever you are in doubt about the status of your *local repository* (since it is on your machine), `git status` is the command to use.

**Staging modified files**

Staging you files is very simple, if you want to stage all the files in that repository

```git
$ git add *
```
But if you only have a specific file to be staged, say `README.md`

```git
$ git add README.md
```

this functionality allows you to stage selected files for commit which is useful if you are working on two different files in the same repository but you only want to commit one of them. Staging only the file that you want to commit will effectively commit that file when we commit later.


----
Ignore everything below for now.





**Committing your changes**

to be continued...
