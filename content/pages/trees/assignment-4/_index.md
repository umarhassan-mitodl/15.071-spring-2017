---
content_type: page
description: Predicting Earnings from Census Data
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: 4 Trees
parent_type: CourseSection
parent_uid: 19c8cf92-e31d-034a-1ea1-5ad53194d892
title: 4.5 Assignment 4
uid: 11ad34c8-1083-2b18-6afa-cd57f2616109
video_metadata:
  youtube_id: null
---
## Predicting Earnings from Census Data

The United States government periodically collects demographic information by conducting a census.

In this problem, we are going to use census information about an individual to predict how much a person earns -- in particular, whether the person earns more than $50,000 per year. This data comes from the {{% resource_link "2b66ae28-e696-46f7-9ee8-2e4dfcb0918d" "UCI Machine Learning Repository" %}}.

The file {{% resource_link "23bdcd00-33c0-4ce7-b2ea-204f161b30e0" "census (CSV - 3.3MB)" %}} contains 1994 census data for 31,978 individuals in the United States.

The dataset includes the following 13 variables:

- *age =* the age of the individual in years
- *workclass =* the classification of the individual's working status (does the person work for the federal government, work for the local government, work without pay, and so on)
- *education =* the level of education of the individual (e.g., 5th-6th grade, high school graduate, PhD, so on)
- *maritalstatus =* the marital status of the individual
- *occupation =* the type of work the individual does (e.g., administrative/clerical work, farming/fishing, sales and so on)
- *relationship =* relationship of individual to his/her household
- *race =* the individual's race
- *sex =* the individual's sex
- *capitalgain =* the capital gains of the individual in 1994 (from selling an asset such as a stock or bond for more than the original purchase price)
- *capitalloss =* the capital losses of the individual in 1994 (from selling an asset such as a stock or bond for less than the original purchase price)
- *hoursperweek =* the number of hours the individual works per week
- *nativecountry =* the native country of the individual
- *over50k =* whether or not the individual earned more than $50,000 in 1994

## Problem 1.1 - A Logistic Regression Model

Let's begin by building a logistic regression model to predict whether an individual's earnings are above $50,000 (the variable "over50k") using all of the other variables as independent variables. First, read the dataset census.csv into R.

Then, split the data randomly into a training set and a testing set, setting the seed to 2000 before creating the split. Split the data so that the training set contains 60% of the observations, while the testing set contains 40% of the observations.

Next, build a logistic regression model to predict the dependent variable "over50k", using all of the other variables in the dataset as independent variables. Use the training set to build the model.

Which variables are significant, or have factors that have at least one significant dummy variable? (Use 0.1 as your significance threshold, so variables with a period or dot in the stars column should be counted too. You might see a warning message here - you can ignore it and proceed. This message is a warning that we might be overfitting our model to the training set.) Select all that apply.

 age 

 workclass 

 education 

 maritalstatus 

 occupation 

 relationship 

 race 

 sex 

 capitalgain 

 capitalloss 

 ¨C10Choursperweek 

 ¨C11Cnativecountry 

## Problem 1.2 - A Logistic Regression Model

What is the accuracy of the model on the testing set? Use a threshold of p = 0.5. (You might see a warning message when you make predictions on the test set - you can safely ignore it.)

## Problem 1.3 - A Logistic Regression Model

What is the accuracy of the baseline model on the testing set?

## Problem 1.4 - A Logistic Regression Model

What is the area under the curve (AUC) for the logistic regression model on the test set?

## Problem 2.1 - A CART Model

We have just seen how a logistic regression model for this data achieves a high accuracy. Moreover, the significances of the variables give us a way to gauge which variables are relevant for this prediction task. However, it is not immediately clear which variables are more important than the others, especially due to the large number of factor variables in this problem.

Let us now build a CART model to predict "over50k". Use the training set to build the model, with all of the other variables as independent variables. Use the default parameters (with the default loss table), so don't set a value for minbucket or cp and do not specify a loss table. Remember to specify method="class" as an argument to rpart, since this is a classification problem. After you are done building the model, plot the resulting tree.

How many splits does the tree have in total?

## Problem 2.2 - A CART Model

Which variable does the tree split on at the first level (the very first split of the tree)?

 age 

 workclass 

 education 

 maritalstatus 

 occupation 

 relationship 

 race 

 sex 

 capitalgain 

 capitalloss 

 ¨C34Choursperweek 

 ¨C35Cnativecountry 

## Problem 2.3 - A CART Model

Which variables does the tree split on at the second level (immediately after the first split of the tree)? Select all that apply.

 age 

 workclass 

 education 

 maritalstatus 

 occupation 

 relationship 

 race 

 sex 

 capitalgain 

 capitalloss 

 ¨C46Choursperweek 

 ¨C47Cnativecountry 

## Problem 2.4 - A CART Model

What is the accuracy of the model on the testing set?

## Problem 3.1 - A Random Forest Model

Before building a random forest model, we'll down-sample our training set. While some modern personal computers can build a random forest model on the entire training set, others might run out of memory when trying to train the model since random forests is much more computationally intensive than CART or Logistic Regression. For this reason, before continuing we will define a new training set to be used when building our random forest model, that contains 2000 randomly selected obervations from the original training set. Do this by running the following commands in your R console (assuming your training set is called "censusTrain"):

set.seed(1)

trainSmall = censusTrain\[sample(nrow(censusTrain), 2000), \]

Let us now build a random forest model to predict "over50k", using the dataset "trainSmall" as the data used to build the model. Set the seed to 1 again right before building the model, and use all of the other variables in the dataset as independent variables. (If you get an error that random forest "can not handle categorical predictors with more than 32 categories", re-build the model without the nativecountry variable as one of the independent variables.)

Then, make predictions using this model on the entire test set. What is the accuracy of the model on the test set, using a threshold of 0.5? (Remember that you don't need a "type" argument when making predictions with a random forest model if you want to use a threshold of 0.5. Also, note that your accuracy might be different from the one reported here, since random forest models can still differ depending on your operating system, even when the random seed is set. )

To generate the random forest model with all of the variables, just run:

library(randomForest)

set.seed(1)

censusrf = randomForest(over50k ~ . , data = trainSmall)

And then you can make predictions on the test set by using the following command:

predictTest = predict(censusrf, newdata=censusTest)

And to compute the accuracy, you can create the confusion matrix:

table(censusTest$over50k, predictTest)

The accuracy of the model should be around

(9614+1050)/nrow(censusTest) = 0.8337112

You may be surprised that the test-set accuracy of the random forest model is lower than the test-set accuracies of some of the other, simpler models we've trained. This can occur when the parameters of the random forest have not been tuned via cross-validation and the default parameters are ill suited for the dataset.

## Problem 4.1 - Selecting cp by Cross-Validation

We now conclude our study of this data set by looking at how CART behaves with different choices of its parameters.

Let us select the cp parameter for our CART model using k-fold cross validation, with k = 10 folds. Do this by using the train function. Set the seed beforehand to 2. Test cp values from 0.002 to 0.092 in 0.01 increments, by using the following command:

cartGrid = data.frame( .cp = seq(0.002,0.092,0.01))

After you create the cartGrid variable, you can pass it on to the train function by letting tuneGrid = cartGrid.

Also, remember to use the entire training set "censusTrain" when building this model. The train function might take some time to run.

Which value of cp does the train function recommend?

Before doing anything, load the caret package:

library(caret)

Set the seed to 2:

set.seed(2)

Specify that we are going to use k-fold cross validation with 10 folds:

fitControl = trainControl( method = "cv", number = 10 )

Specify the grid of cp values that we wish to evaluate:

cartGrid = data.frame( .cp = seq(0.002,0.092,0.01))

Finally, run the train function and view the result:

## Problem 4.2 - Selecting cp by Cross-Validation

Recall that the caret package causes categorical independent variables to be split into factor levels. To generate a version of the test set with dummy variables, please run the following command (which assumes your test set is stored in variable "censusTest"):

censusTestMM = as.data.frame(model.matrix(over50k~.+0, data=censusTest))

Use the final model selected via cross-validation to make predictions on censusTestMM. What is the prediction accuracy on the test set?

Assuming you stored the cross-validation results in a variable called "cartCV", you can access the final selected model with the following command:

model = cartCV$finalModel

You can make predictions on the test set using the following commands:

censusTestMM = as.data.frame(model.matrix(~.+0, data=censusTest))

predictTest = predict(model, newdata=censusTestMM, type="class")

Then you can generate the confusion matrix with the command

table(censusTest$over50k, predictTest)

The accuracy is (9167+1821)/(9167+546+1257+1821) = 0.8590415.

## Problem 4.3 - Selecting cp by Cross-Validation

Compared to the original accuracy using the default value of cp, this new CART model is an improvement, and so we should clearly favor this new model over the old one -- or should we? Plot the CART tree for this model. How many splits are there?

This highlights one important tradeoff in building predictive models. By tuning cp, we improved our accuracy, but our tree became significantly more complex. In some applications, such an improvement in accuracy would be worth the loss in interpretability. In others, we may prefer a less accurate model that is simpler to understand and describe over a more accurate -- but more complicated -- model.

-  
- {{% resource_link "e4031315-c29e-d0c6-413f-d2bd77d67b94" "Continue: Understanding Why People Vote" %}}