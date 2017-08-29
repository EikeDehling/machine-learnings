# Machine learnings - Basics of machine learning

Last year i followed a coursera course on machine learning and several courses on
statistics and data analysis. After that i've started participating in kaggle
machine learning competitions and picked up data analysis and machine learning
tasks at work. 

In this repository i'm sharing an overview of the subject and i'm giving links to
code snippets that you can reuse. I'm hoping this is interesting and helpfull
to others that are learning about data analysis and/or machine learning.


## Overview

I find there are several important activities in an machine learning effort, often i
start with exploratory data analysis, then data preparation, feature engineering
and preprocessing. Then comes selecting, tuning and evaluating models. This is not
a linear process though, i often revisit earlier steps to improve the final model.

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

Date preparation means more filling in missing values and/or converting string values
to numeric ones.

See here for examples:

- [Exploratory Data Analysis Titanic Survivors](https://github.com/EikeDehling/machine-learnings/blob/master/exploratory_data_analysis_titanic.ipynb)
- [Data Analysis New York Green Taxi data](https://github.com/EikeDehling/machine-learnings/blob/master/feature_engineering_data_analysis_taxi.ipynb)


## Feature engineering

I would describe feature engineering as efforts to present data in such a way that a
machine learning algorithm can use it best for predictions. This can be smart
combinations of existing features, parsing textual data, calculated features etc.

See here for some examples and inspiration:

- [Feature engineering New York Green Taxi data](https://github.com/EikeDehling/machine-learnings/blob/master/feature_engineering_data_analysis_taxi.ipynb)


## Preprocessing

Preprocessing means transformations to make data suitable for further machine learning
algorithms. For example some algorithms require all features to be on a similar scale,
such as (-1, 1). Many algorithms only work with numerical data, meaning categorical
or string features need to be encoded.

I've prepared some notebooks with handy code snippets and explanations:

- [Scaling/normalization using RobustScaler](https://github.com/EikeDehling/machine-learnings/blob/master/preprocessing_scaling.ipynb)
- [Encoding categorical data (One-hot / Label encoding](https://github.com/EikeDehling/machine-learnings/blob/master/preprocessing_scaling.ipynb)
- feature selection


## Evaluation

Evaluation means training and then seeing how well it performs. Generally you train
on one dataset and then evaluate on another, to ensure your model generalizes to new
data also and doesn't just work for the training data.

There is many approaches to evaluating models, i'm demonstrating and describing several in
[this notebook](https://github.com/EikeDehling/machine-learnings/blob/master/evaluating.ipynb)


## Tuning model(s) parameters

Most machine learning algorithms have some parameters that can (should) be tuned for
optimal results. Parameters influence for example regularization strength, tree depth
and many more aspects. Tuning parameters can have strong influence on results in some
alorithms, so it pays off to spend some energy here!

I've prepared a few notebooks with examples of parameter tuning approaches:
- [Exhaustive search using GridSeachCV](https://github.com/EikeDehling/machine-learnings/blob/master/parameter_tuning_gridsearchcv.ipynb)
- [Randomized search using RandomizedSearchCV](https://github.com/EikeDehling/machine-learnings/blob/master/parameter_tuning_randomizedsearchcv.ipynb)
- [Hyperopt library](https://github.com/EikeDehling/machine-learnings/blob/master/parameter_tuning_hyperopt.ipynb)
- PySMAC also works well, i'll add a notebook when i find time.


## Comparing and choosing between model(s)

Different models can perform better or worse on various problems as each model is more
or less suited to certain types of prolems. It often makes sense to train and evaluate
multiple models to see which work best and/or where to spend tuning efforts. Note this
is not neccessarily the case, different algorithms can also perform similarly good or bad.

I've prepared [this notebook](https://github.com/EikeDehling/machine-learnings/blob/master/evaluating.ipynb)
to show how you can compare models.


## Finishing remarks

... TODO ...
