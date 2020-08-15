# startercode
For a nicely formatted version of this file, go to: https://github.com/psu-ds410/startercode/blob/master/README.md

This repository contains the starter code for all of the homeworks for DS 410 to be used with Github Classroom.

# First use

The first time you clone a github classroom repository, type the following in a linux shell:
```source ./setup```
This will allow you to receive updates to this repository. If you are not using linux, type the following into the git shell:
```git remote add staff git@github.com:psu-ds410/startercode```

# Updates

Whenever you are notified to update the starter code, type the following in a linux shell:
```source ./updatestater```
This will pull the updates from the startercode repository. If you are not using linux, type the following into the git shell:
```git pull staff master --allow-unrelated-histories```
These actions may require you to merge any conflicts (so make sure you are familiar with the git instructions later in this README file).

If you mess up the merge and want to download the updates manually, visit https://github.com/psu-ds410/startercode to find the recently changed code and download it.

# Git basics

Git is a popular distributed version control system. There is a very nice online book that explains how to use it https://git-scm.com/book/en/v2 . A distributed version control system allows you to update your code so you **don't** have to create mycode.py,  mycode_v2.py, mycode_v3.py, etc. to keep track of your code's history. Git manages the history of your code.

If you are using a non-linux system, make sure to install git and then use the git shell to type in commands.

A typical basic workflow in git is:
* Initialization: use **git clone** to download the repository on your computer the first time.
* Edit your files
* **git status** to see which files you have changed (in case you forget)
* **git add** to stage the files you changed
* **git commit** to update your local repository with the staged files
* **git push** to update your remote repository (the one that is stored on github.com). This will ensure your work is saved even if your computer explodes in a freak accident involving coffee, division by 0, and an asteroid impact.

You can clone a repository on many computers and use them to push changes to the remote repository. In order to synchronize all of these local repositories, you can use **git pull** to download the latest changes. If these changes conflict with yours, you will need to **merge** the changes.

## Cloning a repository (git clone)

Cloning a repository is basically the same as downloading it to your computer for the first time.
The command is 
```git clone [source] [destination]```

For this course, your repository will be created after you accept the assignment at https://classroom.github.com/a/BxfdfYPH .
The source will be git@github.com:psu-ds410/ds410-hw-[github username].git and you can use ds410-hw as the destination. For example, I would clone the homework repository as:

```git clone git@github.com:psu-ds410/ds410-hw-dkifer.git ds410-hw```
(obviously you need to change this a little since your github user name is different than mine).

Once you have cloned a repository, you don't need to clone it again (unless you deleted it from your computer).

## Staging files (git status and git add)

Let's say I edited some files such as hello.py and world.py. These files need to be staged. This can be done by typing
```git add hello.py world.py```
If you don't remember which files you edited, type
```git status``` to see the list.

**Important:** only stage the files you really need (i.e., your source code). **Do not** stage auto-generated files like hello.pyc (since these files are automatically generated by python) and do not stage binary files (i.e., only stage text files like source code).

**Important #2** if you stage a file, and then edit it, you need to stage it again. When you later commit your changes, git will only look at what has been staged. If you edit a file, stage the file, then edit it again (and forget to stage again), ony the first set of edits will be committed.

## Committing files (git commit)

After files are staged, you can use git commit to update (save to) your local repository.
Simpy type
```git commit -m "commit message"```
Make the commit message informative to describe what your recent file edits did.
**Important** you are not listing the files to commit. That has already been done when you staged the files.

## Pushing updates (git push)

Committing a your changes only updates your file history on your local machine. In order to save it on the github servers, you need to push the changes using
``` git push origin master```
(sometimes just typing **git push** is enough)

## Pulling updates (git pull)



## Merging conflicts (merge)
