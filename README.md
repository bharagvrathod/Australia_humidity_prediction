## Objective 
The objective of this project is to gain familiarity with classification models using R.
We want to obtain a model that may be used to predict whether or not it will be more humid
tomorrow than it is today for 10 locations in Australia.
You will be using a modified version of the Kaggle competition data: Predict rain tomorrow in
Australia. https://www.kaggle.com/jsphyg/weather-dataset-rattle-package. The data contains
meteorological observations as attributes, and the class attribute “more humid tomorrow”. 

## Dataset creation

1. Explore the data: What is the proportion of days when it is more humid than the previous
day compared to those where it is less humid? Obtain descriptions of the predictor
(independent) variables – mean, standard deviations, etc. for real-valued attributes. Is
there anything noteworthy in the data? Are there any attributes you need to consider
omitting from your analysis?

3. Document any pre-processing required to make the data set suitable for the model fitting
that follows.

5. Divide your data into a 70% training and 30% test set by adapting the following code
(written for the iris data). Use your student ID as the random seed.
set.seed(XXXXXXXX) #Student ID as random seed
train.row = sample(1:nrow(iris), 0.7*nrow(iris))
iris.train = iris[train.row,]
iris.test = iris[-train.row,]

7. Implement a classification model using each of the following techniques. For this question
you may use each of the R functions at their default settings if suitable.
• Decision Tree
• Naïve Bayes
• Bagging
• Boosting
• Random Forest

9. Using the test data, classify each of the test cases as ‘more humid tomorrow’ or ‘less
humid tomorrow’. Create a confusion matrix and report the accuracy of each model.
10. Using the test data, calculate the confidence of predicting ‘more humid tomorrow’ for
each case and construct an ROC curve for each classifier. You should be able to plot all the
curves on the same axis. Use a different colour for each classifier. Calculate the AUC for
each classifier.

12. Create a table comparing the results in Questions 5 and 6 for all classifiers. Is there a
single “best” classifier?

## Data Analysis and predictive modeling
14. Examining each of the models, determine the most important variables in predicting
whether it will be more humid tomorrow or not. Which variables could be omitted from
the data with very little effect on performance? Give reasons.

16. Starting with one of the classifiers you created in Question 4, create a classifier that is
simple enough for a person to be able to classify whether it will be more humid tomorrow
or not by hand. Describe your model, either with a diagram or written explanation. What
factors were important in your decision? State why you chose the attributes you used.
Using the test data created in Question 3, evaluate model performance using the
measures you calculated for Questions 5 and 6. How does it compare to those in Question
4? 

17. Create the best tree-based classifier you can. You may do this by adjusting the
parameters, and/or cross-validation of the basic models in Question 4. Show that your
model is better than the others using the measures you calculated for Questions 5 and 6.
Describe how you created your improved model, and why you chose that model. What
factors were important in your decision? State why you chose the attributes you used.

19. Using the insights from your analysis so far, implement an Artificial Neural Network
classifier and report its performance. Comment on attributes used and your data preprocessing required. How does this classifier compare with the others? Can you give any
reasons?

21. Fit a new classifier to the data, test and report its performance in the same way as for
previous models. You can choose a new type of classifier not covered in the course, or a
new version of any of the classifiers we have studied. Either way, you will be
implementing a new R package. As a starting point, you might refer to James et al. (2021),
or look online. When writing up, state the new classifier and package used. Include a web
link to the package details. Give a brief description of the model type and how it works.
Comment on the performance of your new model. 
