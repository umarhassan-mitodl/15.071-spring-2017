---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '4.2 Judge, Jury, and Classifier: An Introduction to Trees '
parent_type: CourseSection
parent_uid: 11f9b44d-c296-0689-414b-8c313764a18d
title: '4.2 Judge, Jury, and Classifier: An Introduction to Trees'
uid: ff7dc49d-2cde-fc1a-c3e5-d01f07046ac1
video_metadata:
  youtube_id: null
---
## Quick Question

**Important Note:** When creating random forest models, you might still get different answers from the ones you see here even if you set the random seed. This has to do with different operating systems and the random forest implementation.

Let's see what happens if we set the seed to two different values and create two different random forest models.

First, set the seed to 100, and the re-build the random forest model, exactly like we did in the previous video (Video 5). Then make predictions on the test set. What is the accuracy of the model on the test set?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Now, set the seed to 200, and then re-build the random forest model, exactly like we did in the previous video (Video 5). Then make predictions on the test set. What is the accuracy of this model on the test set?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

You can create the models and compute the accuracies with the following commands in R:

set.seed(100)

StevensForest = randomForest(Reverse ~ Circuit + Issue + Petitioner + Respondent + LowerCourt + Unconst, data = Train, ntree=200, nodesize=25)

PredictForest = predict(StevensForest, newdata = Test)

table(Test$Reverse, PredictForest)

and then repeat it, but with set.seed(200) first.

As we see here, the random component of the random forest method can change the accuracy. The accuracy for a more stable dataset will not change very much, but a noisy dataset can be significantly affected by the random samples.

CheckShow Answer

- {{% resource_link "d818f062-0c7e-3cee-9435-07c440503537" "Back: Video 5: Random Forests" %}}
- {{% resource_link "aed8634b-040d-d1af-7abb-68e999cb9c43" "Continue: Video 6: Cross-Validation" %}}