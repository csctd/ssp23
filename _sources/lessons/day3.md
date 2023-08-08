---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.1
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Replicating Propbulica's COMPAS Audit

```{code-cell} ipython3
import numpy as np
import pandas as pd
import scipy
import matplotlib.pyplot as plt
import seaborn as sns
import itertools
from sklearn.metrics import roc_curve
import warnings
warnings.filterwarnings('ignore')
```

We will relaod the cleaned data
```{code-cell} ipython3
clean_data_url = 'https://raw.githubusercontent.com/ml4sts/outreach-compas/main/data/compas_c.csv'
df = pd.read_csv(clean_data_url).set_index('id')
```

and look at the top to remmeber what it looks like. 
```{code-cell} ipython3
df.head(1) # only 1 line to save space, on zoomed in
```

## What does the `set_index` do? 

How can you figure out what it does from code only?

To figure out, we can re-run the load data without `set_index`

```{code-cell} ipython3
pd.read_csv(clean_data_url).head(1)
```

If we compare this to the one above, we note that when we use `set_index('id')` the `'id'` column is treated idffeerntly 

## Computing Statistics 


```{code-cell} ipython3
df['decile_score'].mean()
```

And we can get that for each group using `groupby`

```{code-cell} ipython3
df.groupby('race')['decile_score'].mean()
```

## Plotting by race

```{code-cell} ipython3
df.groupby('race')['decile_score'].value_counts().plot(kind='bar')
```

```{code-cell} ipython3
df.groupby('race')['decile_score'].value_counts().unstack().plot(kind='bar')
```

```{code-cell} ipython3
df.groupby('race')['decile_score'].value_counts().unstack().T.plot(kind='bar')
```

```{code-cell} ipython3
df.groupby('decile_score')['race'].value_counts().unstack().plot(kind='bar')
```

```{code-cell} ipython3
race_score_counts = df.groupby('decile_score')['race'].value_counts().unstack()
```

```{code-cell} ipython3
race_score_counts.plot(kind='bar',figsize=(12,7))
```

```{code-cell} ipython3
df.groupby('priors_count')['race'].value_counts().unstack().plot(kind='bar',figsize=(12,7))
```

```{code-cell} ipython3
df.groupby(['race','decile_score'])['two_year_recid'].mean()
```

```{code-cell} ipython3
race_score_recid = df.groupby(['race','decile_score'])['two_year_recid'].mean().unstack()
```

```{code-cell} ipython3
race_score_recid
```

```{code-cell} ipython3
race_score_recid.T.plot(kind='bar',figsize=(12,7))
```

```{code-cell} ipython3
race_score_recid
```

```{code-cell} ipython3
race_counts_df = df.groupby(['race','decile_score'])['two_year_recid'].count().reset_index().rename(
    columns={'two_year_recid':'count'})
race_counts_df
```

```{code-cell} ipython3
sns.set_theme(palette='colorblind',context='poster')
```

```{code-cell} ipython3
sns.catplot(data=race_counts_df,x='decile_score',row='race',y='count',
           kind='bar',hue='race',aspect=2)
```

```{code-cell} ipython3
df.groupby(['race','decile_score'])['two_year_recid'].apply(pd.Series.mode)
```

```{code-cell} ipython3
dfQ = pd.read_csv('https://raw.githubusercontent.com/ml4sts/outreach-compas/main/data/compas_cq.csv')
```

```{code-cell} ipython3
dfQ.head()
```

```{code-cell} ipython3
df.head(1)
```

```{code-cell} ipython3
dfQ[['two_year_recid','score_text']].corr()
```

```{code-cell} ipython3
dfQ.groupby('race')[['two_year_recid','score_text']].corr()
```

```{code-cell} ipython3
dfQ.groupby(['race','score_text'])[['two_year_recid']].mean()
```

```{code-cell} ipython3

```
