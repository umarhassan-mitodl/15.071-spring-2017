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
uid: 8f336b6d-3260-d3a1-28f2-88e99dda1c42
video_metadata:
  youtube_id: null
---
## Quick Question

 

Compute the AUC of the CART model from the previous video, using the following command in your R console:

as.numeric(performance(pred, "auc")@y.values)

What is the AUC?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

If you run the command given above after going through the commands in Video 4, you get an AUC of 0.6927.

Now, recall that in Video 4, our tree had 7 splits. Let's see how this changes if we change the value of minbucket.

First build a CART model that is similar to the one we built in Video 4, except change the minbucket parameter to 5. Plot the tree.

How many splits does the tree have?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

You can build a CART model with minbucket=5 by using the following command:

StevensTree = rpart(Reverse ~ Circuit + Issue + Petitioner + Respondent + LowerCourt + Unconst, method="class", data = Train, minbucket=5)

If you plot the tree with prp(StevensTree), you can see that the tree has 16 splits! This tree is probably overfit to the training data, and is not as interpretable.

Now build a CART model that is similar to the one we built in Video 4, except change the minbucket parameter to 100. Plot the tree.

How many splits does the tree have?

Exercise 3

&nbsp;Numerical Response&nbsp;

 

Explanation

You can build a CART model with minbucket=100 by using the following command:

StevensTree = rpart(Reverse ~ Circuit + Issue + Petitioner + Respondent + LowerCourt + Unconst, method="class", data = Train, minbucket=100)

If you plot the tree with prp(StevensTree), you can see that the tree only has one split! This tree is probably not fit well enough to the training data.

CheckShow Answer

 

- {{% resource_link "a0af0b83-fff4-3d63-4dfe-02e15106f92d" "Back: Video 4: CART in R" %}}
- {{% resource_link "d818f062-0c7e-3cee-9435-07c440503537" "Continue: Video 5: Random Forests" %}}