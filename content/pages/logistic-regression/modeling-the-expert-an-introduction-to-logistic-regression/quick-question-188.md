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
uid: d565e093-b63d-b842-9332-eabcb8503b85
video_metadata:
  youtube_id: null
---
## Quick Question

This question asks about the following two confusion matrices:

Confusion Matrix #1:

{{< tableopen >}}{{< tbodyopen >}}{{< tropen >}}{{< thopen >}}
 
{{< thclose >}}{{< thopen >}}
Predicted = 0
{{< thclose >}}{{< thopen >}}
Predicted = 1
{{< thclose >}}{{< trclose >}}{{< tropen >}}{{< thopen >}}
Actual = 0
{{< thclose >}}{{< thopen >}}
15
{{< thclose >}}{{< thopen >}}
10
{{< thclose >}}{{< trclose >}}{{< tropen >}}{{< thopen >}}
Actual = 1
{{< thclose >}}{{< thopen >}}
5
{{< thclose >}}{{< thopen >}}
20
{{< thclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}

 

Confusion Matrix #2:

{{< tableopen >}}{{< tbodyopen >}}{{< tropen >}}{{< thopen >}}
 
{{< thclose >}}{{< thopen >}}
Predicted = 0
{{< thclose >}}{{< thopen >}}
Predicted = 1
{{< thclose >}}{{< trclose >}}{{< tropen >}}{{< thopen >}}
Actual = 0
{{< thclose >}}{{< thopen >}}
20
{{< thclose >}}{{< thopen >}}
5
{{< thclose >}}{{< trclose >}}{{< tropen >}}{{< thopen >}}
Actual = 1
{{< thclose >}}{{< thopen >}}
10
{{< thclose >}}{{< thopen >}}
15
{{< thclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}

What is the sensitivity of Confusion Matrix #1?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

The sensitivity of a confusion matrix is the true positives, divided by the true positives plus the false negatives. In this case, it is 20/(20+5) = 0.8

What is the specificity of Confusion Matrix #1?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

The specificity of a confusion matrix is the true negatives, divided by the true negatives plus the false positives. In this case, it is 15/(15+10) = 0.6

CheckShow Answer

## Quick Question

To go from Confusion Matrix #1 to Confusion Matrix #2, did we increase or decrease the threshold value?

Exercise 3

&nbsp;We increased the threshold value.&nbsp;

&nbsp;We decreased the threshold value.&nbsp;

Explanation

We predict the outcome 1 less often in Confusion Matrix #2. This means we must have increased the threshold.

CheckShow Answer

- {{% resource_link "7bf86a6c-2bb6-629e-d20e-4dd216833197" "Back: Video 5: Thresholding" %}}
- {{% resource_link "f6216265-1257-bdbe-4826-8a5e5b311096" "Continue: Video 6: ROC Curves" %}}