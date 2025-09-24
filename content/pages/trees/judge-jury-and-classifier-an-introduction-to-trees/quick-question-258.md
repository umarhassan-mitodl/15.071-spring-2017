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
uid: 076a36dd-c951-926f-d5c9-9ccb41e476d9
video_metadata:
  youtube_id: null
---
## Quick Question

Suppose that you have the following CART tree:

{{< resource uuid="b2eea6fb-a57d-b424-a484-4f679aee4bc9" >}}

How many splits are in this tree?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

For which data observations should we predict "Red", according to this tree? Select all that apply.

Exercise 2

&nbsp;If X is less than 60, and Y is any value.&nbsp;

&nbsp;If X is greater than or equal to 60, and Y is greater than or equal to 20.&nbsp;

&nbsp;If X is greater than or equal to 85, and Y is less than 20.&nbsp;

&nbsp;If X is greater than or equal to 60 and less than 85, and Y is less than 20.&nbsp;

 

Explanation

This tree has three splits. The first split says to predict "Red" if X is less than 60, regardless of the value of Y. Otherwise, we move to the second split. The second split says to check the value of Y - if it is greater than or equal to 20, predict "Gray". Otherwise, we move to the third split. This split checks the value of X again. If X is less than 85 (and greater than or equal to 60 by the first split) and Y is less than 20, then we predict "Red". Otherwise, we predict "Gray".

CheckShow Answer

- {{% resource_link "fbeabfb3-e0a4-b479-efe5-ffb5d7cf5d4a" "Back: Video 2: CART" %}}
- {{% resource_link "ca1564b0-9178-66a3-a00e-801c8c9fdbbc" "Continue: Video 3: Splitting and Predictions" %}}