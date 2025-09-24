---
content_type: page
description: 2.5 Assignment 2
draft: false
learning_resource_types:
- Assignments
ocw_type: CourseSection
parent_title: 2.5 Assignment 2
parent_type: CourseSection
parent_uid: d3823600-300c-0300-0e79-696e835f8f2f
title: 2.5 Assignment 2
uid: 609cf352-3750-f69e-cb54-c706f04a68c5
video_metadata:
  youtube_id: null
---
## State Data

We often take data for granted. However, one of the hardest parts about analyzing a problem you're interested in can be to find good data to answer the questions you want to ask. As you're learning R, though, there are many datasets that R has built in that you can take advantage of.

In this problem, we will be examining the "state" dataset, which has data from the 1970s on all fifty US states. For each state, the dataset includes the population, per capita income, illiteracy rate, murder rate, high school graduation rate, average number of frost days, area, latitude and longitude, division the state belongs to, region the state belongs to, and two-letter abbreviation.

Load the dataset and convert it to a data frame by running the following two commands in R:

data(state)

statedata = cbind(data.frame(state.x77), state.abb, state.area, state.center,  state.division, state.name, state.region)

If you can't access the state dataset in R, here is a CSV file with the same data that you can load into R using the read.csv function: {{% resource_link "b1ac404f-54b7-a091-4b83-2e21afcb2fac" "statedata (CSV)" %}}.

After you have loaded the data into R, inspect the data set using the command: str(statedata)

This dataset has 50 observations (one for each US state) and the following 15 variables:

- **Population** - the population estimate of the state in 1975
- **Income** - per capita income in 1974
- **Illiteracy** - illiteracy rates in 1970, as a percent of the population
- **Life.Exp** - the life expectancy in years of residents of the state in 1970
- **Murder** - the murder and non-negligent manslaughter rate per 100,000 population in 1976 
- **HS.Grad** - percent of high-school graduates in 1970
- **Frost** - the mean number of days with minimum temperature below freezing from 1931–1960 in the capital or a large city of the state
- **Area** - the land area (in square miles) of the state
- **state.abb** - a 2-letter abreviation for each state
- **state.area** - the area of each state, in square miles
- **x** - the longitude of the center of the state
- **y** - the latitude of the center of the state
- **state.division** - the division each state belongs to (New England, Middle Atlantic, South Atlantic, East South Central, West South Central, East North Central, West North Central, Mountain, or Pacific)
- **state.name** - the full names of each state
- **state.region** - the region each state belong to (Northeast, South, North Central, or West)

## Problem 1.1 - Data Exploration

We begin by exploring the data. Plot all of the states' centers with latitude on the y axis (the "y" variable in our dataset) and longitude on the x axis (the "x" variable in our dataset). The shape of the plot should look like the outline of the United States! Note that Alaska and Hawaii have had their coordinates adjusted to appear just off of the west coast.

In the R command you used to generate this plot, which variable name did you use as the first argument?

 A. statedata$y 

 B. statedata$x 

 C. I used a different variable name. 

## Problem 1.2 - Data Exploration

Using the tapply command, determine which region of the US (West, North Central, South, or Northeast) has the highest average high school graduation rate of all the states in the region:

 West 

 North Central 

 South 

 Northeast 

## Problem 1.3 - Data Exploration

Now, make a boxplot of the murder rate by region (for more information about creating boxplots in R, type ?boxplot in your console).

Which region has the highest median murder rate?

 Northeast 

 South 

 North Central 

 West 

## Problem 1.4 - Data Exploration

You should see that there is an outlier in the Northeast region of the boxplot you just generated. Which state does this correspond to? (Hint: There are many ways to find the answer to this question, but one way is to use the subset command to only look at the Northeast data.)

 Delaware 

 Rhode Island 

 Maine 

 New York 

## Problem 2.1 - Predicting Life Expectancy - An Initial Model

We would like to build a model to predict life expectancy by state using the state statistics we have in our dataset.

Build the model with all potential variables included (Population, Income, Illiteracy, Murder, HS.Grad, Frost, and Area). Note that you should use the variable "Area" in your model, NOT the variable "state.area".

What is the coefficient for "Income" in your linear regression model?

## Problem 2.2 - Predicting Life Expectancy - An Initial Model

Call the coefficient for income x (the answer to Problem 2.1). What is the interpretation of the coefficient x?

 For a one unit increase in income, predicted life expectancy increases by |x| 

 For a one unit increase in income, predicted life expectancy decreases by |x| 

 For a one unit increase in predicted life expectancy, income decreases by |x| 

 For a one unit increase in predicted life expectancy, income increases by |x| 

## Problem 2.3 - Predicting Life Expectancy - An Initial Model

Now plot a graph of life expectancy vs. income using the command:

plot(statedata$Income, statedata$Life.Exp)

Visually observe the plot. What appears to be the relationship?

 Life expectancy is somewhat positively correlated with income. 

 Life expectancy is somewhat negatively correlated with income. 

 Life expectancy is not correlated with income. 

## Problem 2.4 - Predicting Life Expectancy - An Initial Model

The model we built does not display the relationship we saw from the plot of life expectancy vs. income. Which of the following explanations seems the most reasonable?

 Income is not related to life expectancy. 

 Multicollinearity 

## Problem 3.1 - Predicting Life Expectancy - Refining the Model and Analyzing Predictions

Recall that we discussed the principle of simplicity: that is, a model with fewer variables is preferable to a model with many unnnecessary variables. Experiment with removing independent variables from the original model. Remember to use the significance of the coefficients to decide which variables to remove (remove the one with the largest "p-value" first, or the one with the "t value" closest to zero), and to remove them one at a time (this is called "backwards variable selection"). This is important due to multicollinearity issues - removing one insignificant variable may make another previously insignificant variable become significant.

You should be able to find a good model with only 4 independent variables, instead of the original 7. Which variables does this model contain?

 Income, HS.Grad, Frost, Murder 

 HS.Grad, Population, Income, Frost 

 Frost, Murder, HS.Grad, Illiteracy 

 Population, Murder, Frost, HS.Grad 

## Problem 3.2 - Predicting Life Expectancy - Refining the Model and Analyzing Predictions

Removing insignificant variables changes the Multiple R-squared value of the model. By looking at the summary output for both the initial model (all independent variables) and the simplified model (only 4 independent variables) and using what you learned in class, which of the following correctly explains the change in the Multiple R-squared value?

 We expect the "Multiple R-squared" value of the simplified model to be slightly worse than that of the initial model. It can't be better than the "Multiple R-squared" value of the initial model. 

 We expect the "Multiple R-squared" value of the simplified model to be slightly better than that of the initial model. It can't be worse than the "Multiple R-squared" value of the initial model.  

 We expect the "Multiple R-squared" of the simplified model to be about the same as the intial model (we have no way of knowing if it will be slightly worse or slightly better than the Multiple R-squared of the intial model). 

## Problem 3.3 - Predicting Life Expectancy - Refining the Model and Analyzing Predictions

Using the simplified 4 variable model that we created, we'll now take a look at how our predictions compare to the actual values.

Take a look at the vector of predictions by using the predict function (since we are just looking at predictions on the training set, you don't need to pass a "newdata" argument to the predict function).

Which state do we predict to have the lowest life expectancy? (Hint: use the sort function)

 South Carolina 

 Mississippi 

 Alabama 

 Georgia 

Which state actually has the lowest life expectancy? (Hint: use the which.min function)

 South Carolina 

 Mississippi 

 Alabama 

 Georgia 

## Problem 3.4 - Predicting Life Expectancy - Refining the Model and Analyzing Predictions

Which state do we predict to have the highest life expectancy?

 Massachusetts 

 Maine 

 Washington 

 Hawaii 

Which state actually has the highest life expectancy?

 Massachusetts 

 Maine 

 Washington 

 Hawaii 

## Problem 3.5 - Predicting Life Expectancy - Refining the Model and Analyzing Predictions

Take a look at the vector of residuals (the difference between the predicted and actual values).

For which state do we make the smallest absolute error?

 Maine 

 Florida 

 Indiana 

 Illinois 

For which state do we make the largest absolute error?

 Hawaii 

 Maine 

 Texas 

 South Carolina 

{{% resource_link "d64b9247-3ae1-fb23-50f1-b27dc8fbde0b" "Back: Detecting Flu Epidemics via Search Engine Query Data" %}}