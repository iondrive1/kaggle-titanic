# kaggle-titanic
Jupyter Notebook for Kaggle Titanic Competition
# Diagnostics to Improve Models in the Titanic Kaggle Competition

[Douglas Friesen, PhD](https://www.linkedin.com/in/douglas-friesen-phd/), April 2021

The sinking of the Titanic, which happened on April 15, 1912, is one of the most famous shipwrecks in history. It forms the basis of the introductory [machine learning competition](https://www.kaggle.com/c/titanic) on Kaggle. The basis of this competition is the binary classification problem: Given features of the passengers on the Titanic, predict whether or not they survived when the Titanic sunk.

In this notebook, I go through the process of designing an optimal model to predict survival:
* Understanding of Problem
* Exploration of Data
* Cleaning of Data
* Feature Engineering
* Model Selection
* Hyperparameter optimization for models
* Model Testing

I supplement these common elements of machine learning problems in Kaggle competitions with a focus on the following:
1. Evaluating the model predictions using Confusion Matrices, ROC curves, and Area under the curve (AUC) scores. This allows insight into modifying the threshold of a binary classifier in order to reduce false positives or false negatives (Type I and Type II error), which is applicable to many binary classification problems, such as those in healthcare.
2. Diagnostics to point to the most efficient way to improve predictions, based on evidence of bias or variability in the models. Having models overfit and underfit data are common problems, and being able to diagnose which problem a model has can lead to pursuing efforts that improve a model.

The motivation of this guide is to explore the suggestions made by Andrew Ng in his Stanford class CS229 lecture entitled: [Lecture 13 - Debugging ML Models and Error Analysis | Stanford CS229: Machine Learning (Autumn 2018)](https://www.youtube.com/watch?v=ORrStCArmP4). The main question explored in this lecture is that after a model has been created, what is the most efficient use of time to improve the model? There are many ways to improve an algorithm, and figuring out the best way involves diagnostics to understand what the main problem the model is encountering. Common problems are:
* High bias
* High variance
* Problem with the optimization algorithm
* Problem with the optimization objective

Professor Ng indicates a strong understanding of these elements can save months in a tough data science problem by targeting what will actually improve performance in an underperforming model.

As well, the lecture explores error analysis and ablative analysis when multiple learning components form a pipeline, to understand which part of the pipeline is key to the algorithm's success, and which parts have the most potential to improve the algorithm. We will perform ablative analysis on our features in classifying survival in this project as a step to identifying ways to improve the model developed.

This notebook takes elements from other Kaggle notebooks in the setup of the features and the models.
