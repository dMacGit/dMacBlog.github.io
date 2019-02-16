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
  - Linux
  - Pip
---

## Virtaulize your Environment ##

When managing or just simply creating new projects, it can easily become a chore installing/uninstalling dependencies or libraries depending on what your project will be trying to solve.
This process will soon break your package repo's, or at the very least, cause alot of wasted time, sorting out broken dependencies.

Enter the idea of **Virtaul Environments** (From the Software develpment viewpoint, atleast).

This is the concept of keeping your projects seperate, and contained, while holding all there unique and specific dependencies and libraries to themselves, away from the rest of your projects and global environment settings.

*Note: All commands here are for installing and setting up in linux*

### Installing Virtual Environment ###

You can use PIP to install.
```
$ pip install --user virtualenv
```

### Using Virtual Environment ###

Once installed, you can create a virtual environment for/in a particular directiory
```
$ virtualenv /path/to/your/virtual/evn/
```
Now you can activate the environment.

```
$ source /path/to/venv/bin/activate
```
Note the ```/bin/activate```, this is the script to enter the environment.
Once in the environment (or venv) you can do whatever you like to it, without breaking your global environemnt.
Install Python, Django packages etcetera, etcetera.

To exit the environment, use the ``` $ deactivate ``` command

And thats it. Simple, fast, yet powerfull.

### Time for Venv Wrapper ###

There is one additional tool wich makes creating and using venv's even easier. Virtualenvwrapper.

This takes venv's to the next level, where you can hop in and out of multiple venv's with ease.

Using Pip you can install with:

``` $ pip install virtualenvwrapper ```

Then we need to do some initial configuration before we can use it.

You will want to add the command ``` source /usr/local/bin/virtualenvwrapper.sh ``` to your shell startup file, changing the path to ```virtualenvwrapper.sh``` depending on where it was installed by pip or your package manager.

``` 
$ export WORKON_HOME=~/Envs
$ mkdir -p $WORKON_HOME
$ source /usr/local/bin/virtualenvwrapper.sh
``` 

### Creating your First Venv ###

There are only a few commands you need to get familiar with in order to craete and maintain your virtual environments.

To get started run the ``` $ workon ``` command.
This will list all environments. Since you have non, this will be empty.

In order to creat your first venv, simply run ``` $ mkvirtualenv yourEnvName ```.
Now when you run ``` $ workon ``` your venv will be returned in the list.

To switch to a particular venv you simply run ``` $ workon yourEnvName ```

By default this will also **Activate** that venv.
You can **Activate** or **Deactivate** your venv at will, by simply using ``` $ activate ``` or ``` $ deactivate ```.
You can tell if you are in an active venv from the shell or command line.

For example:

```
(emgee_core) phantom@Phantom-PC:/
```

Here its is showing that I am in an active **emgee_core** venv.

The next step is to link your venv with your project home folder.
Before we do this, it would be good to deactivate from any activated venv.

Next simply navagate to your project home folder ``` $ cd /home/myProjectdir/  ```

Once in the project home, activate the venv for that project, then set the projectdir with ``` $ setvirtualenvproject ```:

```
$ workon yourEnvName
$ setvirtualenvproject
```

The ``` $ setvirtualenvproject ``` command will set the current working directory as the project home folder for the venv.

You can switch from the venv home folder to the prject folder with the command ``` cdproject ```



