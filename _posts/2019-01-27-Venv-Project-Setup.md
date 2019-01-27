---
title: 'Project setup with Virtual Environment'
date: 2019-01-27
permalink: /posts/2019/01/27/Venv-Project-Setup/

tags:
  - Development
  - Project
  - Virtual Environment
  - Venv
  - Virtualenvwrapper
---

## Virtaulize your Environment ##

When managing or just simply creating new projects, it can easily become a chore installing/uninstalling dependencies or libraries depending on what your project will be trying to solve.
This process will soon break your package repo's, or at the very least, cause alot of wasted time, sorting out broken dependencies.

Enter the concept of **Virtaul Environments** (From the Software develpment viewpoint, atleast).

This is to idea around, keeping your projects seperate, and contained, holding all there unique and specific dependencies and libraries to themselves, away from the rest of your projects and global environment settings.

*Note: All commands here are for install and setup in linux*

### Installing Venv ###

You can use PIP to simply install.
```
$ pip install --user virtualenv
```

There are also a couple of additional tools wich makes this process even easier.


