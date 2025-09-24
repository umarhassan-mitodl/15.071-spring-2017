---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '5.2 Turning Tweets into Knowledge: An Introduction to Text Analytics'
parent_type: CourseSection
parent_uid: aea3bc9c-07f7-3648-65c4-6fec93dd8515
title: '5.2 Turning Tweets into Knowledge: An Introduction to Text Analytics'
uid: c08c448d-ba2f-6d4e-4aa3-a930b6c97c07
video_metadata:
  youtube_id: null
---
## Quick Question

 

In the previous video, we used CART and Random Forest to predict sentiment. Let's see how well logistic regression does. Build a logistic regression model (using the training set) to predict "Negative" using all of the independent variables. You may get a warning message after building your model - don't worry (we explain what it means in the explanation).

Now, make predictions using the logistic regression model:

predictions = predict(tweetLog, newdata=testSparse, type="response")

where "tweetLog" should be the name of your logistic regression model. You might also get a warning message after this command, but don't worry, it is due to the same problem as the previous warning message.

Build a confusion matrix (with a threshold of 0.5) and compute the accuracy of the model. What is the accuracy?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

You can build a logistic regression model in R by using the command:

tweetLog = glm(Negative ~ ., data=trainSparse, family="binomial")

Then you can make predictions and build a confusion matrix with the following commands:

predictLog = predict(tweetLog, newdata=testSparse, type="response")

table(testSparse$Negative, predictLog > 0.5)

The accuracy is (254+37)/(254+46+18+37) = 0.8197183, which is worse than the baseline. If you were to compute the accuracy on the training set instead, you would see that the model does really well on the training set - this is an example of over-fitting. The model fits the training set really well, but does not perform well on the test set. A logistic regression model with a large number of variables is particularly at risk for overfitting.

Note that you might have gotten a different answer than us, because the glm function struggles with this many variables. The warning messages that you might have seen in this problem have to do with the number of variables, and the fact that the model is overfitting to the training set. We'll discuss this in more detail in the Homework Assignment.

Is this worse or better than the baseline model accuracy of 84.5%? Think about the properties of logistic regression that might make this the case!

CheckShow Answer

- {{% resource_link "6faa3dc6-2c17-bf81-844b-b5d994e997d9" "Back: Video 7: Predicting Sentiment" %}}
- {{% resource_link "f3a415ff-eba9-ca2d-622f-58bcb8aea03c" "Continue: Video 8: Conclusion" %}}