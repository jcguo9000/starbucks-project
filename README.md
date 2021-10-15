# starbucks-offers

# Starbucks Capstone Challenge
## Project in Data Scientist Nanodegree of Udacity

## Table of Contents
1. [Installation](#installation)
2. [Project Motivation](#project-motivation)
3. [File Descriptions](#file-descriptions)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing-authors-acknowledgements)

## Installation

Download all the files from the repository and run the starbucks_caperstone.ipynb using Jupter Notebook

## Project Motivation

This is the Starbuck's Capstone Challenge from Udacity. We get the dataset from the program that shows the offer information that Starbuks send to users, the user demographics and their transactions with the offer and purchases. We want to perform exploratory analysis and build a classifier to predict how different users interact with different offers

We are interested to answer the following questions:

How the offer type and delivery channels affects how people interact with the offer?
How each demographic groups of users interact with different offers?
Can we build a classifier to predict how users interact with offers?

## File Descriptions
The notebook available here showcases work related to the above questions.

The data is contained in three files:

portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
profile.json - demographic data for each customer
transcript.json - records for transactions, offers received, offers viewed, and offers completed
Here is the schema and explanation of each variable in the files:

**Data**

**portfolio.json**

- id (string) - offer id
- offer_type (string) - the type of offer ie BOGO, discount, informational
- difficulty (int) - the minimum required to spend to complete an offer
- reward (int) - the reward is given for completing an offer
- duration (int) - time for the offer to be open, in days
- channels (list of strings)

**profile.json**

- age (int) - age of the customer
- became_member_on (int) - the date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

**transcript.json**

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since the start of the test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record

**starbucks-caperstone.ipynb**

Jupyter notebook to analyze data and build the classifier

**pic1.png, pic2.png**

Picture files used in the Jupyter notebook


## Results
The main findings of the code can be found at the post available [here](https://jcguo.medium.com/how-a-customer-reacts-to-a-starbucks-offer-53a3a40a7bcb).

From the anaysis, we concluded that offer #2 is the most successful offer and offer # 7 is the least successful in terms of revenue vs. cost. Social media is a powerful tool to reach users, because based on the data, the offers that was not delivered through social media, have a relatively low view rate. Another observation is that offers with longer duration seems to have a better completion rate than shorter durations. Besides these, the influnece of offer difficulty, offer type and rewards amount is not very clear from exloratory analysis. From the user aspect, users in older age groups, with higer income, female and other gender users, users with longer membership age are more likely to view the offer and complete the offer. On the other hand, users with higer income, female users, and users with membership age between 4-6 years are more likely to complete an offer without viewing the offer. 

Here we categorized the user and offer interaction into 3 categories: 1. did not complete the offer (category 0), 2. complete the offer without view (category 1) and 3. complete the offer with view (category 2). We tested using different subset of the data and differnet classifers. And finally determine that the gradientboosting classfier performs the best with using the entire cleaned dataset have the best performance. 

## Licensing, Authors, Acknowledgements
Please credit Starbucks and Udacity for the data

To complete this project, the follow resources were used.

1. [4 Types of Classification Tasks in Machine Learning](https://machinelearningmastery.com/types-of-classification-in-machine-learning/)
2. [Statistical classification](https://en.wikipedia.org/wiki/Statistical_classification#Algorithms)
3. [GaussianNB](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html)
4. [Combining two Series into a DataFrame in pandas](https://stackoverflow.com/questions/18062135/combining-two-series-into-a-dataframe-in-pandas)
5. [Merge, join, concatenate and compare](https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html)
6. [matplotlib.axes.Axes.legend](https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.legend.html)
7. [seaborn.displot](https://seaborn.pydata.org/generated/seaborn.displot.html#seaborn.displot)
8. [Rotate axis text in python matplotlib](https://stackoverflow.com/questions/10998621/rotate-axis-text-in-python-matplotlib)
9. [Basic Syntax-The Markdown elements outlined in John Gruber's design document.](https://www.markdownguide.org/basic-syntax/)
10. [Confusion Matrix Visualization](https://medium.com/@dtuk81/confusion-matrix-visualization-fc31e3f30fea)
11. [sklearn.ensemble.GradientBoostingClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html)
12. [sklearn.linear_model.LogisticRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
13. [Decision Trees](https://scikit-learn.org/stable/modules/tree.html)
14. [sklearn.svm.SVC](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html)
15. [sklearn.metrics.classification_report](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html#sklearn.metrics.classification_report)
16. [Metrics and scoring: quantifying the quality of predictions](https://scikit-learn.org/stable/modules/model_evaluation.html)
17. [pandas.DataFrame.iterrows](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.iterrows.html#pandas.DataFrame.iterrows)
18. [pandas.Series.map](https://pandas.pydata.org/docs/reference/api/pandas.Series.map.html)
19. [pandas.DataFrame.unstack](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.unstack.html)
20. [pandas.cut](https://pandas.pydata.org/docs/reference/api/pandas.cut.html)
