# Add Pictures to your site 

1. Complete your Web Critic Worksheet and Submit
2. Pull your updates from GitHub into your Codespace (on the git tab in Codespace, under the 3 dots menu)
3. Run your site (`nox -s docs-live`) in the terminal on CodeSpaces
4. Add a new file called `pechakucha.md` and add a title (markdown H1) to it
5. use the [markdown cheatsheet](https://www.markdownguide.org/cheat-sheet/) to add images to your `pechakucha.md`
6. In `index.md` uncomment lines about the menu
7. Commit and sync your changes on GitHub so that they go through to your rendered website. 


## Index.md example

Find the part that looks like
```HTML
<!-- ```{toctree}
:maxdepth: 2
:hidden:

pechakucha
``` -->
```

and remove the comments (remember ctrl/cmd + `/` toggles comments in any language) so it looks like: 

````HTML
```{toctree}
:maxdepth: 2
:hidden:

pechakucha
```
````