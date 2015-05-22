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


## Committing
Before commiting you need to add your files, so that it can be picked while committing. Once  you have created the file, do a ```git status``` you'll see the untracked files. you can add them using ```git add <files or pattern>```
Once you have added the files, you can commit using: ```git commit -m "<Comments>"```

## Pushing your changes to remote
Git basically works in a distributed fashion, all the changes you commit reside in your local repository. Unless you want to push it to your server (refer to them as remote)

### For this first you need to create a remote repository on Github.
- Go to github.com, log in, and click the '+' in the top right to create a new repository.
- Give it a name that matches your local repository's name, 'hello-world', and a short description.
- Make it public.
- You can choose to create a default [readme.md](markdown) or create it later.
- Leave .gitignore and license on 'none'.
- Click create repository!

### Now connect your local repository to remote repository
- You can have multiple remotes so each requires a name. For your main one, this is commonly named ```origin```
```git remote add origin "<url of the github repo, that you created in previous steps>"```

> In Windows system, an ```origin``` is automatically created. So you you just need to run the following command: ```git remote set origin "<url of the github repo, created in previous step>"```

### Pushing the changes
Once we have added the remote repo, next thing is to push all the changes you have done to GitHub.

> we should push our changes regularly to remote to keep in sync.

Git has branching system, you can create branches whenever you want. All the changes you push should be against a branch. By default a branch is created is ```master```
So we can push it to a ```master``` using : ```git push origin master```

## Now the Fun part - Forking
Forking is creating a copy of a project (a public project of some other github account) in your github account. Forks are used to create your own version of a project or contributing a back fixes or features to the original project.

For forking follow the following steps:
  - On the top of this site click on fork, and done that's it :) So much of the talks

Now what to do with your forked projects ? You **Clone it**

Cloning is like pulling a code from the remote repository, and creating a local repository. Use the following command to clone the forked project onto your local.
```git clone "<url of the project copy of your account>"```
> Few Points to note:
- Do no clone it within an existing git project.
- ```git clone``` creates the directory automatically, so no need to create one.


As mentioned earlier that we fork for contributing a back fix or features, how does my changes merge back to original repository ( from which I copied ). For this you need to connect to the original repository, by adding a remote. This is also needed to continuously be in sync with the original repo.
Here is how to do it: ```git remote add <repo-name:usually named as upstream> <url to the original repo>```
