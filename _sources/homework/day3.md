# Extending Your Analysis

1. review the class materials and annotate your notebook from this morning. 
2. extend your analysis in one of the three options below
3. Prepare for class tomorrow by creating a GitHub account or adding your URI email to your existing one. Make sure you know (or have saved) your password. 

<!-- ``````{tab-set}

```{tab-item} Experiment with plots -->

## Extension Option A: customize your plots

1. read about seaborn's [set_theme](https://seaborn.pydata.org/generated/seaborn.set_theme.html)
2. customize your pandas plots to be styled for a poster and use a colorblind friendly color palett
3. use seaborn's [catplot](https://seaborn.pydata.org/generated/seaborn.catplot.html) to make your plot of the distribution of the scores more like the ones in the article (two separate subplots with African-American on the top and Caucasion on the bottom)
4. Make 2 additional plots of different types and include 3 new customizations
<!-- ```

```{tab-item} Practice with Statistics -->
## Extension Option B: more statistics 


1. Use the mode to find the most common compas score per race group. 
1. Find the most common outcome (re-arrested or not) for each compas score (1-10) and each race
1. Create a new column that is 1 or 0 if the high/low compas score matches if the person was re-arrested or not use `df['new_column_name'] = new value` to create a column and use `==` to compare two values to see if they are equal or not
1. Compute the percent correct predictions of the compas algorithm overall
1. Compute the percent correct predictions of the compas algorithm per race
1. Compute the percent correct predictions of the compas algorithm per race and for high/low scores


<!-- 
```

````{tab-item} Tutorial on functions -->
## Extension Option C: more criticism of COMPAS 
(tutorial)

Disparate impact is a legal concept used to describe situations when an entity such as an employer *inadvertently* discriminates against a certain protected group. This is distinct from *disparate treatment* where discrimination is intentional.

To demonstrate cases of disparate impact, the Equal Opportunity Commission (EEOC) proposed "rule of thumb" is known as the [The 80% rule](https://en.wikipedia.org/wiki/Disparate_impact#The_80.25_rule).

Feldman et al. adapted a fairness metric from this  principle. For our application, it states that the ratio of the percentage of defendants predicted to be high risk in each protected group (in this case whites and African-Americans) should be above 80%.


### Functions in Python

We define functions in Python like this: 
```Python
def name_of_function(argument): # signature of function
    '''
    decription of function

    Parameters
    ----------
    arguments : type
        description of argument

    Returns
    -------
    value
    '''
    #body of function
    value = argument *3
    return value
```

Write a function to print a greeting like this: 


Hello World! 

```
def greeting(name):
    '''
    greet a specific person

    Parameters
    ----------
    name: string
        name of person to greet
    
    '''
    print('hello', name)
```


Now try to check if it prints the right thing with 

```
assert greeting('sarah') == 'hello sarah'
```

```{dropdown} why did it break? 
That function does not return anything, but it does something, so if we wanted to test it, it's hard. 

It does *do* something so that is called **side effect**. 
```
<!-- ````

`````` -->

A better function would **return** the greeting instead of printing it; this is more versatile (it can be used in more different ways) and easier to write automated tests for. 

```
def greeting(name):
    '''
    greet a specific person

    Parameters
    ----------
    name: string
        name of person to greet
    
    '''
    return 'hello ' +  name
```


Now lets write our disparate impact function. 
I'll give you the template, You fill in the body

```
def disparate_impact_score(advantaged_score, disadvantaged_score):
    '''
    calculate DI ratio of advantaged:disadvantaged

    Parameters
    ----------
    advantaged_score : float
        score for advantaged group
    disadvantaged_score : float
        score for disadvantaged group
    
    Returns
    -------
    di_ratio : float
        disparate impact score
    '''
     
```

Now apply the disparate impact score to the real world outcomes and the COMPAS score.  Does that make you think COMPAS is fair or not? 