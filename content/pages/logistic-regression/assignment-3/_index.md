---
content_type: page
description: Popularity of Music Records
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: 3 Logistic Regression
parent_type: CourseSection
parent_uid: c4464cf4-9ddb-1a4b-c78c-faa6f93b74de
title: 3.5 Assignment 3
uid: d4a650ea-930c-2c8c-0f98-9b353a5a342e
video_metadata:
  youtube_id: null
---
## Popularity of Music Records

The music industry has a well-developed market with a global annual revenue around $15 billion. The recording industry is highly competitive and is dominated by three big production companies which make up nearly 82% of the total annual album sales. 

Artists are at the core of the music industry and record labels provide them with the necessary resources to sell their music on a large scale. A record label incurs numerous costs (studio recording, marketing, distribution, and touring) in exchange for a percentage of the profits from album sales, singles and concert tickets.

Unfortunately, the success of an artist's release is highly uncertain: a single may be extremely popular, resulting in widespread radio play and digital downloads, while another single may turn out quite unpopular, and therefore unprofitable. 

Knowing the competitive nature of the recording industry, record labels face the fundamental decision problem of which musical releases to support to maximize their financial success. 

How can we use analytics to predict the popularity of a song? In this assignment, we challenge ourselves to predict whether a song will reach a spot in the Top 10 of the Billboard Hot 100 Chart.

Taking an analytics approach, we aim to use information about a song's properties to predict its popularity. The dataset {{% resource_link "0657f55b-10c0-9785-3d2b-ee6e5186764d" "songs (CSV)" %}} consists of all songs which made it to the Top 10 of the Billboard Hot 100 Chart from 1990-2010 plus a sample of additional songs that didn't make the Top 10. This data comes from three sources: {{% resource_link "05db9b2d-4c6f-4dd1-a6fe-38bb521ea816" "Wikipedia" %}}, {{% resource_link "2ba6940e-bf40-4dcf-87a4-233aa222fd8c" "Billboard.com" %}}, and {{% resource_link "5c03d32a-ea97-4754-84a3-46007ba416e1" "EchoNest" %}}.

The variables included in the dataset either describe the artist or the song, or they are associated with the following song attributes: time signature, loudness, key, pitch, tempo, and timbre.

Here's a detailed description of the variables:

- **year** = the year the song was released
- **songtitle** = the title of the song
- **artistname** = the name of the artist of the song
- **songID** and **artistID** = identifying variables for the song and artist
- **timesignature** and **timesignature\_confidence** = a variable estimating the time signature of the song, and the confidence in the estimate
- **loudness** = a continuous variable indicating the average amplitude of the audio in decibels
- **tempo** and **tempo\_confidence** = a variable indicating the estimated beats per minute of the song, and the confidence in the estimate
- **key** and **key\_confidence** = a variable with twelve levels indicating the estimated key of the song (C, C#, . . ., B), and the confidence in the estimate
- **energy** = a variable that represents the overall acoustic energy of the song, using a mix of features such as loudness
- **pitch** = a continuous variable that indicates the pitch of the song
- **timbre\_0\_min**, **timbre\_0\_max**, **timbre\_1\_min**, **timbre\_1\_max**, . . . , **timbre\_11\_min**, and **timbre\_11\_max** = variables that indicate the minimum/maximum values over all segments for each of the twelve values in the timbre vector (resulting in 24 continuous variables)
- **Top10** = a binary variable indicating whether or not the song made it to the Top 10 of the Billboard Hot 100 Chart (1 if it was in the top 10, and 0 if it was not)

## Problem 1.1 - Understanding the Data

Use the read.csv function to load the dataset "songs.csv" into R.

How many observations (songs) are there in total?

## Problem 1.2 - Understanding the Data

How many songs does the dataset include for which the artist name is "Michael Jackson"?

One way to compute this would be using table():

table(songs$artistname == "Michael Jackson")

We can also get this information using the dplyr package. We will first load the dplyr package:

library(dplyr)

and then filter the data frame to artistname == "Michael Jackson" and summarize the number of observations:

songs %>% filter(artistname == "Michael Jackson") %>% summarize(count = n())

## Problem 2.1 - Creating Our Prediction Model

We wish to predict whether or not a song will make it to the Top 10. To do this, first use the filter function to split the data into a training set "SongsTrain" consisting of all the observations up to and including 2009 song releases, and a testing set "SongsTest", consisting of the 2010 song releases.

How many observations (songs) are in the training set?

## Problem 2.2 - Creating our Prediction Model

In this problem, our outcome variable is "Top10" - we are trying to predict whether or not a song will make it to the Top 10 of the Billboard Hot 100 Chart. Since the outcome variable is binary, we will build a logistic regression model.

We will only use the variables in our dataset that describe the numerical attributes of the song in our logistic regression model. So we won't use the variables "year", "songtitle", "artistname", "songID", or "artistID".

We have seen in the lecture that, to build the logistic regression model, we would normally explicitly input the formula including all the independent variables in R. However, in this case, this is a tedious amount of work since we have a large number of independent variables.

There is a nice trick to avoid doing so by using the symbol "." that represents all the remaining variables. You can follow the steps below:

**Step 1:** we want to exclude some of the variables in our dataset from being used as independent variables ("year", "songtitle", "artistname", "songID", and "artistID"). To do this, we can use the following trick. First define a vector of variable names called nonvars - these are the variables that we won't use in our model.

nonvars = c("year", "songtitle", "artistname", "songID", "artistID")

To remove these variables from your training and testing sets, type the following commands in your R console:

SongsTrain = SongsTrain\[ , !(names(SongsTrain) %in% nonvars) \]

SongsTest = SongsTest\[ , !(names(SongsTest) %in% nonvars) \]

**Step 2:** build a logistic regression model to predict Top10 using the training data. We can now use "." in place of enumerating all the remaining independent variables in the following way:

SongsLog1 = glm(Top10 ~ ., data=SongsTrain, family=binomial)

(Also, keep in mind that you can choose to put quotes around binomial, or leave out the quotes. R can understand this argument either way.)

Looking at the summary of your model, excluding the intercept, how many variables are significant at the 5% significance level?

To answer this question, you first need to run the three given commands to remove the variables that we won't use in the model from the datasets:

nonvars = c("year", "songtitle", "artistname", "songID", "artistID")

SongsTrain = SongsTrain\[ , !(names(SongsTrain) %in% nonvars) \]

SongsTest = SongsTest\[ , !(names(SongsTest) %in% nonvars) \]

Then, you can create the logistic regression model with the following command:

SongsLog1 = glm(Top10 ~ ., data=SongsTrain, family=binomial)

## Problem 2.3 - Creating Our Prediction Model

Let's now think about the variables in our dataset related to the confidence of the time signature, key, and tempo (timesignature\_confidence, key\_confidence, and tempo\_confidence). Our model seems to indicate that these confidence variables are significant (rather than the variables timesignature, key, and tempo themselves). What does the model suggest?

 The lower our confidence about time signature, key and tempo, the more likely the song is to be in the Top 10 

 The higher our confidence about time signature, key and tempo, the more likely the song is to be in the Top 10 

## Problem 2.4 - Creating Our Prediction Model

In general, if the confidence is low for the time signature, tempo, and key, then the song is more likely to be complex. What does our model suggest in terms of complexity?

 Mainstream listeners tend to prefer more complex songs 

 Mainstream listeners tend to prefer less complex songs 

## Problem 2.5 - Creating Our Prediction Model

Songs with heavier instrumentation tend to be louder (have higher values in the variable "loudness").

By inspecting the coefficient of the variable "loudness", what does our model suggest?

 Mainstream listeners prefer songs with heavy instrumentation 

 Mainstream listeners prefer songs with light instrumentation 

## Problem 3.1 - Validating Our Model

Make predictions on the test set using our model. What is the accuracy of our model on the test set, using a threshold of 0.45? (Compute the accuracy as a number between 0 and 1.)

To get the accuracy after you make the predictions, you can use the table(variable1, variable2) command to generate a summary table that counts the number of observations for each of the possible combination of values in variable1 and variable2. You can also do so by using the group\_by and summarize commands in dplyr package.

You can make predictions on the test set by using the command:

testPredict = predict(SongsLog1, newdata=SongsTest, type="response")

Then, you can create a confusion matrix with a threshold of 0.45 by using the table command:

table(SongsTest$Top10, testPredict >= 0.45)

Or, alternatively, use the group\_by and summarize functions in dplyr package:

SongsTest$Pred = testPredict >= 0.45

SongsTest %>% group\_by(Top10, Pred) %>% summarize(count = n())

## Problem 3.2 - Validating Our Model

Let's check if there's any incremental benefit in using our model instead of a baseline model. Given the difficulty of guessing which song is going to be a hit, an easier model would be to pick the most frequent outcome (a song is not a Top 10 hit) for all songs. What would the accuracy of the baseline model be on the test set? (Give your answer as a number between 0 and 1.)

You can compute the baseline accuracy by summarizing the outcome variable in the test set. One way to do this is with table():

table(SongsTest$Top10)

Another approach would be to use dplyr:

SongsTest %>% group\_by(Top10) %>% summarize(count = n())

## Problem 3.3 - Validating Our Model

What is the True Positive Rate of our model on the test set, using a threshold of 0.45?

What is the False Positive Rate of our model on the test set, using a threshold of 0.45?

- {{% resource_link "bafc7d56-02f9-e47a-53ea-0d210aa17805" "Back: Video 5: Test Set Predictions" %}}
- {{% resource_link "3b462833-7389-a83d-6609-7f7597856e56" "Continue: Predicting the Baseball World Series Champion" %}}