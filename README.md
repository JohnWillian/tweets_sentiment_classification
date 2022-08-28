# Introduction

In the program, we implemented 5 different machine learning algorithms: Baseline model (0-R), KNN, GNB, K-Means, and Self-Training. All of the models were using **skleran ** library to help implement.

# Data Preprocess

We use **pandas** to help us read the **pickle** data, after reading the data to the pd dataframe, we convert the 'Sentiment' labels into 0 and 1 (negative = 0, positive = 1), which helps us reduce the workload when evaluating the model.

# Models

## Baseline Model

We use **DummyClassifier** from sklearn, the strategy we choose is "most_frequent", which is same as 0-R strategy.

## K-Nearest Neighbors

We use **KNeighborsClassifier** from sklearn. We use a uniform majority vote for our implementation.

We also build a program to help KNN to find the best **k** value for KNN model.

## Gaussian Naive Bayes

We use **GaussianNB** from sklearn.

## K-Means

We use **KMeans** from sklearn. The clusters we chose is 2, random_state is 0.

## Self-Training

We use **SelfTrainingClassifier** from sklearn.

### Self-Training GNB

We use GNB as our Self-Training classifier, we sample the 100,000 unlabeled data into the train dataset.

### Self-Training KNN

We use KNN as our Self-Training classifier, we sample the 100,000 unlabeled data into the train dataset.

# Analysis

We use sklearn.metrics to help us run evaluations.

Evaluation matrixes: accuracy, precision, recall, and f1. (The model also return a confusion matrix.)

We matplotlib.pyplot to help us draw the graph.

## The effect of different amounts of unlabeled data on the accuracy of semi-supervised models

We separate the 100,000 unlabeled datasets into 10 different batches. Each loop adds 10,000 of data and draws a line graph according to the change in the accuracy of the model.

## Confusion Matrix

Just print the confusion matrix for different models.

>
>
>RNN Version link: https://colab.research.google.com/drive/11gTt2jECZSwcP5XFjUuL03p6vy3xAsBt?usp=sharing