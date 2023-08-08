# Static Sites 

# Static site generation

1. make final repo 
2. modify a few pages

goals: 
1. learn about separating content and design
2. prepare for final repo
3. practice with github and peer review

+++

# Hello World

[hello world](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program) is usually how we start teaching new programming languages. 
+++

Python can be used many ways.  Instead of a new notebook, click on console of python

+++

```
print('hello world')
```

+++

We could also put that in a cell inside of a notebook

+++

Or a regular terminal if we call the python program first

```
python
```

then enter our code

```
print('hello world')
```

+++
then we use 
```
exit()
```

to leave the python interpreter 

+++

Or we can make a new python file, put code there and then tell the python interpter to use that file

```
python hello_world.py
```

+++

Python is a **language** that we can use in different contexts as long as we have **an** interpreter, but there are many interpreters, and multiple ways to access them,  

Jupyter lab is a data science focused tool and Jupyterhub is a server for accessing it. 

Outside of Data science we usually use other **I**ntegrated **D**evelopment **E**nvironments to work.  

Today we will use a browser-based version of [VS Code](https://code.visualstudio.com/) via GitHub CodeSpaces and we will work with both a website and some Python.  

+++

# GitHub and Static Site Generation

GitHub actions allow us to run programs that process our code.  

Typically this is something like: 
- running automated tests to see if it is correct
- checking formatting
- building from one format to another (compiling C, markdown to html, etc)

GitHub Pages only serve **static** (no database) websites (aka static sites)

Static sites are good because they load fast for viewers

+++

The main reason websites use databases is to store content separate from formatting

**static site generators** allow us to separate the content from the formatting without a database 

+++

Yesterday we used Jupyter-book. Jupyter Book is an [opinionated distribution of sphinx](https://jupyterbook.org/en/stable/explain/sphinx.html)

this means it *uses* sphinx, but makes different things the defaults, so things that require some work with sphinx, are automatic with jupyterbook. 

also, some things that are available are sphinx are kind of blocked or hard to use in Jupyterbook.  

+++

Today we'll use a site that is build with sphinx directly based on some customizations of it made by one of the developers at Jupyter, [Chris Holdgraf](https://github.com/choldgraf/choldgraf.github.io). 
+++
```{important}
see prismia for the link to create your repo
```


- edit the `info.yml` to have your info in it
- write a descriptive commit message
- **select create a new branch and open a PR**

[about pull requestions](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
+++

Merge the PR

+++

Codespaces 

+++ 

local buildng

+++
Push to GitHub on a branch
Leave your PR there, we'll come back next week

+++

## Codespaces theme settings

In the very bottom left, click the gear, choose Theme, then color theme.  You can select a theme from the list, or search for others. 

You can also [set your default theme for all projects](https://docs.github.com/en/codespaces/customizing-your-codespace/setting-your-default-editor-for-github-codespaces)

+++
## Homework 

add any two images to you `_static/img/` folder in your `profile-website` repo 

