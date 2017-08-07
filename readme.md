# Machine learnings - Basics of machine learning

Last year i followed a coursera course on machine learning and several courses on
statistics and data analysis. After that i've started participating in kaggle
machine learning competitions, first tutorial competitions and now also some
serious competitions.

In here i'll share an overview of what i've learned and give links to code snippets
that you can reuse. I'm hoping this is interesting and helpfull to others that are
starting to learn about this subject!


## Overview

There is several important activities in a machine learning effort, often it starts
at some exploratory data analysis, there can be data preparation, feature engineering
and preprocessing. Then comes selecting and tuning models. Finally there is evaluation
of the completed model.

I've tried to display the process in the chart below:

![Machine Learning Process](https://github.com/EikeDehling/machine-learnings/raw/master/process.png "Machine Learning Process")

The picture intends to show that there is a back-and-forth between the various
activities. Often it all starts at exploratory analysis and then trying to make a
basic model, leading to a first score. Then the result is improved from there
by revisiting each of the steps, for example adding some more features tuning the
model more, picking a stronger model etc.


## Exploratory Analysis & Data Preparation

Data analysis and preparation serves to get an understanding of data and prepare it for
modelling efforts. Good understanding of data can be very advantageous, for example
allowing you to engineer better features or understanding why your model performs
bad.

During the exploratory analysis you can for example plot distributions, correlation
of numeric features and influence of categorical variables to help yourself understand
the data.

Data preparation means more filling in missing values and/or converting string values
to numeric ones.

See here for examples: ... TODO: Make notebook(s) ...


## Feature engineering

I would describe feature engineering as efforts to present data in such a way that a
machine learning algorithm can use it best for predictions. This can be smart
combinations of existing features, parsing textual data, calculated features etc.

See here for some examples and inspiration: ... TODO: Make notebook(s) ...


## Preprocessing

- scaling/normalization
- transforms (one-hot ; labelencoder)
- feature selection
- etc


## Evaluation

Evaluation means training and then seeing how well it performs. Generally you train
on one dataset and then evaluate on another, to ensure your model generalizes to new
data also and doesn't just work for the training data.

There is many approaches to evaluating models, i'm demonstrating and describing several in
[this notebook](https://github.com/EikeDehling/machine-learnings/blob/master/evaluating.ipynb)


## Tuning model(s) parameters
## Comparing and choosing between model(s)
## Finishing remarks
