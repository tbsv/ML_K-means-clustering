# Machine Learning // K-Means Clustering

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tbsv/ML_K-means-clustering/master?filepath=K-means-clustering_solution.ipynb) [![nbviewer](https://img.shields.io/badge/nb-viewer-orange?logo=jupyter)](https://nbviewer.jupyter.org/github/tbsv/ML_K-means-clustering/blob/master/K-means-clustering_solution.ipynb)

This is Binder-compatible repo with a `requirements.txt` file.

## Summary

In this project, we will try to use K-Means-Clustering to divide US universities into two groups: private and public.

## Contents

There is 1 notebook in this repository:

- [K-means-clustering_solution.ipynb](K-means-clustering_solution.ipynb) : runs a K-means clustering exercise that is taken from a Udemy course (see details in the *About* section below).

In addition, the following ressources are in this repository:

- [requirements.txt](requirements.txt) : lists all Python libraries that the notebook depends on.
- [DATA](DATA) : contains all data sets and further ressources that are used within the Jupyter Notebook.

## Usage

Dependencies are specified in [requirements.txt](/requirements.txt) :

```
pip install -r requirements.txt
```

You can access this repo via **Binder** at the following URL 
https://mybinder.org/v2/gh/tbsv/ML_K-means-clustering/master or via the Binder badge above.

For a quick look into the notebook, you can use the **NBViewer** badge above.

Alternatively, you can run the notebook locally. Therefore, you will need to have python installed,
preferably through [Anaconda](https://www.anaconda.com/download/).

## Run the notebook

Each cell of code can be run with `shift + enter` or you can run the entire notebook by selecting `Cell` -> `Run All` in the toolbar.

![Screenshot](DATA/jn_run-all.png?raw=true "Screenshot")

For more information on running Jupyter notebooks, see the [Jupyter Documentation](https://jupyter.readthedocs.io/en/latest/).

## Example (for reproduction)

### Import libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
```

### Import data set
```python
df = pd.read_csv('./DATA/College_Data',index_col=0)
```

### Create a scatter plot with Grad.Rate vs Room.Board
```python
sns.set_style('whitegrid')
sns.lmplot('Room.Board','Grad.Rate',data=df, hue='Private',
           palette='coolwarm',height=6,aspect=1,fit_reg=False)
```

### Result plot
![plot](DATA/K-means-clustering_private.png?raw=true "Plot")

## Issues

Please [open an issue](https://github.com/tbsv/ML_K-means-clustering/issues) if you encounter any problems while trying to run the notebooks.

## About
This data science exercise is part of the Digital Business Engineering Master at HHZ.

The given example was taken from the Udemy course [Python for Data Science, Machine Learning & Visualization](https://www.udemy.com/course/python-data-science-machine-learning/).

Adaptions to the jupyter notebook are made by [Tobias Vetter](mailto:tobias.vetter@student.reutlingen-university.de).