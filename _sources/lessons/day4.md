# Git, GitHub, and a Jupyter Book

## What we're going to do

Today, we're going to focus on an important tool in programming, git, and we'll use it via GitHub.

## What is GitHub?


Let's learn from the source: [about](https://github.com/about)

````{margin}
```{note}
 I know this material, but I want you to see the official refernce. Other internet sources will give all sorts of other interpretations, but what GitHub says, is the most official*
 ```
 ````


## What is git?


[git](https://git-scm.com/) is:
- free 
- open source
- distributed version control system
- designed to be fast
- flexible and can be used many ways 
- not tied only to github! 



## Distributed Version Control 

### Version Control
- ~like history on a google doc
- keeps "versions" at points in time you get to pick
- lets you make test changes without breaking your main copy
- 

### Distributed 
- good for collaboration
- everyone gets their own copy
- programatic tools **and** social conventions to help you not mess it up 


## Sharing your notebooks

We will make a repository for your notebooks that allows them to become a portfolio. 

```{important}
If you are making up class, see prismia for the links
```

## Examining the repo

- [YAML](https://yaml.org/) files contain settings for various tools.  ours have extenstion .yml and are used to tell GitHub how to turn this repo into a website. One is written for GitHub specifically and the other is for a program called [jupyter book](https://jupyterbook.org/) that can convert markdown and notebooks to HTML and provide helpful CSS for them. 
- README.md is a special markdown file for GitHub
- index.md is the first content file for your project
- .gitignore is a list of files and type of files that the git program should not track changes in



## Making an issue. 

Make the title: `Portfolio Start`

put this in the body
```
## By noon on Friday: 
- [ ] upload each notebook file
- [ ] edit the intro
- [ ] turn on "pages" to deploy from branch

## When you want
- [ ] clean up your notebooks by adding more text
- [ ] *optionally* [transfer ownership](https://docs.github.com/en/repositories/creating-and-managing-repositories/transferring-a-repository) of the repo to yourself and keep adding to it
```
+++

GitHub issues use a special flavor of markdown, the `[ ]` is not supported the same way everywhere, for example in prismia, that is how I make multiple choice questions for you. 

+++

this [markdown cheatsheet](https://www.markdownguide.org/cheat-sheet/) is a good reference while you get used to it. 

+++

## Make your site your own

Edit the top of the `_config.yml` file to have your own information in it

Set your site to [serve from the `gh-pages` branch](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-from-a-branch)



## Adding Notebooks

1. On JupyterHub, download one of your notebooks
2. Upload it to GitHub

## GitHub Codespaces

Enter the Codespace