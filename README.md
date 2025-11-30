Final Project | Description

The goal of this project is to identify and explore interesting aspects of data in a real-world context, provide extensive explanations about each step, and report on your analysis of the results. The final project will involve communicating results of your analysis and technical results in a group presentation that effectively translates your work. You will work in groups of three to four students to create a presentation and then submit the code that you used.

The project will consist of the following tasks:

Analyzing data and selecting the models best suited to solve the problem;
Implementing and optimizing algorithms discussed in this course;
Using Python to perform computations and analyze the results;
Completing a slide deck for the group presentation; and
Effectively communicating methodology and results during the group presentation.

Project Problem: Classification

You will define a binary classification problem to solve: either an image classification task OR a document classification task. You will only choose one of the options outlined below. Both tasks will require you to first define the problem you are trying to solve, conduct an exploratory data analysis (EDA), identifying any interesting aspects of the data, train various machine learning models to the data, then draw conclusions from the analysis.

Although the goal is to build a good classifier, you are not expected to create the most accurate classifier possible. Instead you will be evaluated on your methodology: how you defined the problem, the process by which you solved the problem (exploratory data analysis, preprocessing, modeling and optimization), and how well you clearly communicate your analysis.

As a data scientist, you should be able to turn an ambiguous problem into a practical problem that you can solve. For this reason, you are not required to use all of the data as it is. Feel free to use a subset of the original data, or use different sized training and test sets, but be able to defend the choices you make in defining the problem. It is better to have an effective solution to your problem, even if it isn’t the optimal one.

Option Two: Document Classification

Given a large set of news articles from , define a document classification problem, and train models to accurately label the news articles. The data consists of 127,600 descriptions of news articles and their titles. The response is one of four category labels: World, Sports, Business, Science/Technology. Each class is split into training (30,000) and testing (1,900), but you do not need to use the entire data set, and you can create your own test sets.

You should construct a fictional, applied problem as background for this task. You will pick two classes of documents for this problem, then optimize algorithms to correctly identify the categories with a low error rate. For example, you may choose to label Sports vs Business. Or you may combine World + Business to contrast with Science/Technology. The dataset also includes titles, so you may want to use these in some way. Feel free to get creative with this part since it can help create an interesting story for your group presentations.

The easiest way to access the raw data is through the tensorflow_datasets package.

import tensorflow_datasets as tfds
train_data, test_data = tfds.load(
  'ag_news_subset',
  split = ['train', 'test'],
  batch_size = -1
)
df_train = pd.DataFrame(train_data)
df_test = pd.DataFrame(test_data)
