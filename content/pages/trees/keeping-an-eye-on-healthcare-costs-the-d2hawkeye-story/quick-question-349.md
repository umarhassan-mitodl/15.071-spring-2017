---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '4.3 Keeping an Eye on Healthcare Costs: The D2Hawkeye Story '
parent_type: CourseSection
parent_uid: 52a221dd-c011-90a4-45b1-a393b15cb810
title: '4.3 Keeping an Eye on Healthcare Costs: The D2Hawkeye Story'
uid: 09222225-3a2b-5d3f-b68d-5398ca2111a9
video_metadata:
  youtube_id: null
---
## Quick Question

 

Suppose that instead of the baseline method discussed in the previous video, we used the baseline method of predicting the most frequent outcome for all observations. This new baseline method would predict cost bucket 1 for everyone.

What would the accuracy of this baseline method be on the test set?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

What would the penalty error of this baseline method be on the test set?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

To compute the accuracy, you can create a table of the variable ClaimsTest$bucket2009:

table(ClaimsTest$bucket2009)

According to the table output, this baseline method would get 122978 observations correct, and all other observations wrong. So the accuracy of this baseline method is 122978/nrow(ClaimsTest) = 0.67127.

For the penalty error, since this baseline method predicts 1 for all observations, it would have a penalty error of:

(0\*122978 + 2\*34840 + 4\*16390 + 6\*7937 + 8\*1057)/nrow(ClaimsTest) = 1.044301

CheckShow Answer

 

- {{% resource_link "9f0c1981-6b4e-786a-4cb9-64211da05bf8" "Back: Video 7: Baseline Method and Penalty Matrix" %}}
- {{% resource_link "42af8e9a-43f3-ab0e-231b-e7ab1d08c0ca" "Continue: Video 8: Predicting Healthcare Cost in R" %}}