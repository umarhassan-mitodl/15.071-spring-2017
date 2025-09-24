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
uid: 9cb7a258-ad19-0f7f-84e5-89aad47092b1
video_metadata:
  youtube_id: null
---
## Quick Question

 

Suppose the coefficients of a logistic regression model with two independent variables are as follows:

( \\beta\_{()} = -1.5 , \\enspace \\beta\_1 = 3 , \\enspace \\beta\_2 = -0.5 )

 

And we have an observation with the following values for the independent variables:

( x\_1 = 1 , \\enspace x\_2 = 5 )

 

What is the value of the Logit for this observation? Recall that the Logit is log(Odds).

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

The Logit is just log(Odds), and looks like the linear regression equation. So the Logit is -1.5 + 3*1 - 0.5*5 = -1.

What is the value of the Odds for this observation? Note that you can compute e^x, for some number x, in your R console by typing exp(x). The function exp() computes the exponential of its argument.

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

Using the value of the Logit from the previous question, we have that Odds = e^(-1) = 0.3678794.

What is the value of P(y = 1) for this observation?

Exercise 3

&nbsp;Numerical Response&nbsp;

 

Explanation

Using the Logistic Response Function, we can compute that P(y = 1) = 1/(1 + e^(-Logit)) = 1/(1 + e^(1)) = 0.2689414.

CheckShow Answer

- {{% resource_link "8099bebb-d4e8-1ce0-9baa-3ede1f3ec357" "Back: Video 3: Logistic Regression" %}}
- {{% resource_link "8fc17cbb-03cd-ce23-b588-0c21e7dc33e8" "Continue: Video 4: Logistic Regression in R" %}}