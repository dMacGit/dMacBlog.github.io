---
title: 'Some Git Basics'
date: 2019-05-30
permalink: /posts/2019/05/30/Some-Git-Basics/

tags:
  - Development
  - Project
  - Git
  - Github
  - Repositories
  - Linux
---

# Some Git versionings basics

Here are some Git versioning basic how to's for creating and updating a new project or repository.
More detailed guides and reference materials can be viewed at __https://git-scm.com__.
More specifically first time setup can be found on this guide: [**here**](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)

## Setting up git on your machine
Once git is installed (See [Here](https://git-scm.com/downloads) if you have not done so yet),
we need to setup your username, and email details, as well as the repo's upstream remote origin location.

To setup your username and email for every repository:
``` bash
$ git config --global user.name "my name"
$ git config --global user.email "my.email@example.com"
```
And to check or view username once set:
``` bash
$ git config --global user.name 
> my name
```
And to check or view email once set:
``` bash
$ git config --global user.email
> my.email@example.com
```
To setup your username and email for a single repository:
``` bash
$ git config user.name "my name"
$ git config user.email "my.email@example.com"
```
And to check or view username once set:
``` bash
$ git config user.name 
> my name
```
And to check or view email once set:
``` bash
$ git config user.email 
> my.email@example.com
```

## Creating a new Repository

Creating a repository can be done in a few clicks. Simple to follow guide [Here](https://help.github.com/en/articles/create-a-repo)
from the Github help docs page.

Once the repo is created on the remote side, we can pull/push updates from our local machine.

### Pulling from remote

To pull an existing project from the remote (github) location to you local machine, you can use the "clone" command.

Using "Https"

``` bash
$ git clone "https://github.com/your_name/your_remote_repo/"
```

Using "SSH"

``` bash
$ git clone "git@github.com:user_name/your_remote_repo.git"
```

### Pushing from the Local machine 
To setup a folder to hold/manage a new git project, you can call 'git init' when in the target directory.
``` bash
$ git init
```
This should generate a ".git" folder.

## Creating a git tag.

Sometimes its helpfull to keep track of particular commits.
One of the ways to do this, is the use of a Git Tag.

#### You can easily create one, using some basics commands:

This should list any existing tags that have been created for the project/repo.

``` bash
$ git tag
```

The following creates a new anotated (-a flag) tag of v1.0, with the description (-m "text here" flag) "my version v1.0":

``` bash
$ git tag -a v1.0 -m "my version v1.0"
```

Once created, this can be pushed to the master origin branch by:
``` bash
$ git push origin v1.0
```



 