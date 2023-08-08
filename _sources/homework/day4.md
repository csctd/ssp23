# Data Science Portfolio

````{margin}
```{important}
see prismia for links to the vocab
```
```{hint}
Use the preview when editing markdown files
Markdown uses [HTML comments](https://www.w3schools.com/html/html_comments.asp) A common programming practice is to put template content in comments. 
```
````
1. Review Github vocab in your GitHub vocab repo
2. Update your [GitHub Profile README](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme) to practice GitHub 
3. Upload the rest of your notebooks and clean them up so that they are how you want your portfolio to look
4. Try at least one customization from [jupyterbook](https://jupyterbook.org/).  You can choose your own from the documentation or use one of the recommendations below. 


## Recommended Customizations



### a glossary
```{tip}
This is recommended
```

1. Add a [glossary](https://jupyterbook.org/en/stable/content/content-blocks.html?highlight=glossary#glossaries) in a new file with at least 3 terms you learned 
2. Reference at least two terms to where those terms are used in your portfolio. 
3. add your glossary file to your toc

````{margin}
```{hint}
Right below the example it tells you how to reference a term
```
````

### Add another page

1. Create a markdown file
2. add content 
3. link it to your ToC
4. update your [TOC](https://jupyterbook.org/en/stable/structure/toc.html) to have parts, not only a list of chapters
5. put your notebooks in one part and your new page in a different part

### Jupytext and special content blocks 

```{warning}
this one sometimes (but not always, so I did not know in advance) breaks jupyterhub
```

1. in a terminal on jupyterlab, run `pip install jupytext`
2. use [jupytext](https://jupytext.readthedocs.io/en/latest/install.html) to save your notebook as myst markdown
3. upload the markdown version of your notebook
4. edit on github to add [special content block](https://jupyterbook.org/en/stable/content/content-blocks.html)