# Git Tutorial
## Introduction
Git is an open source software written by *Linus Torvalds*
who also wrote Linux operating system.

It is a program for keeping track of changes over time, known in programming as version control.

## Installation
* Windows - It's recommended to download GitHub for Windows, which includes Git and has an easier install [here](http://windows.github.com). Use the Git Shell for your terminal.
* Mac - Download it from [here](http://mac.github.com)
* Self - Go to [git hub downloads](http://git-scm.com/downloads) and follow instructions
* Git via git - you can just git your git :) ```git clone https://github.com/git/git```

### Check if it is installed
Git isn't like a normal application, you might not see an icon created
```git --version```
## Set Basic Configurations
Set user name

```git config --global user.name "<Your User Name>"```

Set Your Full Name

```git config --global user.email "<Your email address>"```

If you are behind a corporate proxy set your proxy and https-proxy

```git config --global proxy "<proxy>"```
```git config --global https-proxy "<proxy>"```


## Repository
A **repository** is essentially a project. You can imagine it as a project's folder with all the related files inside of it. In fact, that's what it will look like on your computer anyways.

You tell Git what your project is and Git will start tracking all of the changes to that folder. Files added or subtracted or even a single letter in a single file changed -- all of it's tracked and time stamped by Git. That's **version control**.

### Create a Repository
To create a repository:
```git init```
This will initialize the repository, and enable the git on this location. You can double check if it's setup by running ```git status``` if you don't get errors, Bingo !
