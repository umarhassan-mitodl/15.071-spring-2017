---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
parent_type: CourseSection
parent_uid: 3063320a-4175-6b8a-4fa9-892f61b52c0d
title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
uid: 8c080206-9993-5e2b-b0c5-0c4cd73fd74c
video_metadata:
  youtube_id: null
---
## Quick Question

 

In R, create a logistic regression model to predict "PoorCare" using the independent variables "StartedOnCombination" and "ProviderCount". Use the training set we created in the previous video to build the model.

Note: If you haven't already loaded and split the data in R, please run these commands in your R console to load and split the data set. Remember to first navigate to the directory where you have saved "quality.csv".

quality = read.csv("quality.csv")

install.packages("caTools")

library(caTools)

set.seed(88)

split = sample.split(quality$PoorCare, SplitRatio = 0.75)

qualityTrain = subset(quality, split == TRUE)

qualityTest = subset(quality, split == FALSE)

Then recall that we built a logistic regression model to predict PoorCare using the R command:

QualityLog = glm(PoorCare ~ OfficeVisits + Narcotics, data=qualityTrain, family=binomial)

You will need to adjust this command to answer this question, and then look at the summary(QualityLog) output.

What is the coefficient for "StartedOnCombination"?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

To construct this model in R, use the command:

Model = glm(PoorCare ~ StartedOnCombination + ProviderCount, data=qualityTrain, family=binomial)

If you look at the output of summary(Model), the value of the coefficient (Estimate) for StartedOnCombination is 1.95230.

CheckShow Answer

 

## Quick Question

 

StartedOnCombination is a binary variable, which equals 1 if the patient is started on a combination of drugs to treat their diabetes, and equals 0 if the patient is not started on a combination of drugs. All else being equal, does this model imply that starting a patient on a combination of drugs is indicative of poor care, or good care?

Exercise 2

&nbsp;Poor Care&nbsp;

&nbsp;Good Care&nbsp;

Explanation

The coefficient value is positive, meaning that positive values of the variable make the outcome of 1 more likely. This corresponds to Poor Care.

CheckShow Answer

 

- {{% resource_link "8fc17cbb-03cd-ce23-b588-0c21e7dc33e8" "Back: Video 4: Logistic Regression in R" %}}
- {{% resource_link "7bf86a6c-2bb6-629e-d20e-4dd216833197" "Continue: Video 5: Thresholding" %}}