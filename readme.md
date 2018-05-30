# Machine learnings - Basics of machine learning

Last year i followed a coursera course on machine learning and several courses on
statistics and data analysis. After that i've started participating in kaggle
machine learning competitions and picked up data analysis and machine learning
tasks at work. 

In this repository i'm sharing an overview of the subject and i'm giving links to
code snippets that you can reuse. I'm hoping this is interesting and helpfull
to others that are learning about data analysis and/or machine learning.


## Running

To run the notebooks and/or extend them, you can run them using this command in a docker container (requires docker):

```
docker run -it --rm --user root -e NB_UID=1000 -e NB_GID=1000 -v `realpath .`:/home/jovyan/work -p 8888:8888 jupyter/datascience-notebook
```

Alternatively you can setup a python virtual environment, install the required packages in there and run:

```
virtualenv .
bin/pip install -r requirements.txt
bin/jupyter notebook
```


## Overview

I find there are several important activities in an machine learning effort, often i
start with exploratory data analysis, then data preparation, feature engineering
and preprocessing. Then comes selecting, tuning and evaluating models. This is not
a linear process though, i often revisit earlier steps to improve the final model.

I've tried to display the process in the chart below:

![Machine Learning Process](https://github.com/EikeDehling/machine-learnings/raw/master/img/process.png "Machine Learning Process")

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
- [Loans Acceptance Data Analysis & Modelling](https://github.com/EikeDehling/machine-learnings/blob/master/loans_acceptance.ipynb)
- [Black Friday](https://github.com/EikeDehling/machine-learnings/blob/master/black_friday.ipynb)


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
- [Encoding categorical data (One-hot / Label encoding](https://github.com/EikeDehling/machine-learnings/blob/master/preprocessing_encoding.ipynb)
- feature selection


## Evaluation

Evaluation means training and then seeing how well it performs. Generally you train
on one dataset and then evaluate on another, to ensure your model generalizes to new
data also and doesn't just work for the training data.

There is many approaches to evaluating models, here are some notebooks with examples:

- [Evaluation & cross validation Approaches](https://github.com/EikeDehling/machine-learnings/blob/master/evaluating.ipynb)
- [Loans Acceptance Data Analysis & Modelling](https://github.com/EikeDehling/machine-learnings/blob/master/loans_acceptance.ipynb)


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
- [Black Friday - Tuning model params with validation plots](https://github.com/EikeDehling/machine-learnings/blob/master/black_friday.ipynb)


## Comparing and choosing between model(s)

Different models can perform better or worse on various problems as each model is more
or less suited to certain types of prolems. It often makes sense to train and evaluate
multiple models to see which work best and/or where to spend tuning efforts. Note this
is not neccessarily the case, different algorithms can also perform similarly good or bad.

I've prepared [this notebook](https://github.com/EikeDehling/machine-learnings/blob/master/comparing_models.ipynb)
to show how you can compare models.


## Overfitting, underfitting and diagnosing

Overfitting and underfitting are the most common ways for models to fail. In the notebooks
below i'll show how that could look, how to diagnose and some solutions.

- [Overfitting and Underfitting](https://github.com/EikeDehling/machine-learnings/blob/master/underfit_overfit.ipynb)


## Stacking, ensembling & averaging

... TODO ...


## Working with textual data (NLP)

Working with textual data is a special area - because machine learning models normally
only work on numbers. That means before any modelling happens we need to convert the text
into numbers. Also there is various modeling approaches, from linear models to neural
networks that have proven successful and work in different scenarios.

In these notebooks you can find some ideas on processing textual data:
- [NLP with NLTK](https://github.com/EikeDehling/machine-learnings/blob/master/nlp_nltk.ipynb)
- [Hate speech - Logistic Regression and TfIdf features](https://github.com/EikeDehling/machine-learnings/blob/master/nlp_hate_speech.ipynb)
- [Hate speech - Deep learning](https://github.com/EikeDehling/machine-learnings/blob/master/nlp_hate_speech_neural.ipynb)
- [Twitter sentiment - Airlines Data](https://github.com/EikeDehling/machine-learnings/blob/master/nlp_airline_sentiment.ipynb)
- [NLP with Neural Networks](https://github.com/EikeDehling/machine-learnings/blob/master/nlp_neural_networks.ipynb)
- [NLP Textual Similarity / Search Ranking](https://github.com/EikeDehling/machine-learnings/blob/master/nlp_similarity_crowdflower.ipynb)


## Finishing remarks

It's been really interesting to learn all these new things! Also very helpfull for myself
to try and write it down in a structured way. I'm hoping this is interesting to others...
