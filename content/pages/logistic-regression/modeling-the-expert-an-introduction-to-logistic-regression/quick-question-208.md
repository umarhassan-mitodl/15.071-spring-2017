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
uid: 8809159b-6e06-0da2-d386-90c7900fdd67
video_metadata:
  youtube_id: null
---
## Quick Question

 

**Important Note:** This question uses the original model with the independent variables "OfficeVisits" and "Narcotics". Be sure to use this model, instead of the model you built in Quick Question 4.

Compute the test set predictions in R by running the command:

predictTest = predict(QualityLog, type="response", newdata=qualityTest)

You can compute the test set AUC by running the following two commands in R:

ROCRpredTest = prediction(predictTest, qualityTest$PoorCare)

auc = as.numeric(performance(ROCRpredTest, "auc")@y.values)

What is the AUC of this model on the test set?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

If you run the commands given above in your R console, you can see the value of the AUC of this model on the test set by just typing auc in your console. The value should be 0.7994792.

CheckShow Answer

 

The AUC of a model has the following nice interpretation: given a random patient from the dataset who actually received poor care, and a random patient from the dataset who actually received good care, the AUC is the perecentage of time that our model will classify which is which correctly.

- {{% resource_link "1e61720e-cc15-0a7b-0c5e-b3fe60c5ffa1" "Back: Video 7: Interpreting the Model" %}}
- {{% resource_link "81d5d93d-77c2-b8fc-0b85-d9cbcdc418a5" "Continue: Video 8: The Analytics Edge" %}}