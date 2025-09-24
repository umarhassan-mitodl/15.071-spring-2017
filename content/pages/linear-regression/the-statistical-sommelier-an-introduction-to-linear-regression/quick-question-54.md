---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '2.2 The Statistical Sommelier: An Introduction to Linear Regression'
parent_type: CourseSection
parent_uid: 4495fb48-3934-3c33-23b2-2ef2104af559
title: '2.2 The Statistical Sommelier: An Introduction to Linear Regression'
uid: a15d356c-50bc-b55a-2cbd-e1c66378ef25
video_metadata:
  youtube_id: null
---
## Quick Question

 

The following figure shows three data points and the best fit line

( y = 3x + 2 . )

The x-coordinate, or "x", is our independent variable and the y-coordinate, or "y", is our dependent variable.

{{< resource uuid="0c812c31-8c89-3954-3d90-1b0f954da36a" >}}

Please answer the following questions using this figure.

What is the baseline prediction?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

The baseline prediction is the average value of the dependent variable. Since our dependent variable takes values 2, 2, and 8 in our data set, the average is (2+2+8)/3 = 4.

What is the Sum of Squared Errors (SSE) ?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

The SSE is computed by summing the squared errors between the actual values and our predictions. For each value of the independent variable (x), our best fit line makes the following predictions:

If x = 0, y = 3(0) + 2 = 2,

If x = 1, y = 3(1) + 2 = 5.

Thus we make an error of 0 for the data point (0,2), an error of 3 for the data point (1,2), and an error of 3 for the data point (1,8). So we have

SSE = 0² + 3² + 3² = 18.

What is the Total Sum of Squares (SST) ?

Exercise 3

&nbsp;Numerical Response&nbsp;

 

Explanation

The SST is computed by summing the squared errors between the actual values and the baseline prediction. From the first question, we computed the baseline prediction to be 4. Thus the SST is:

SST = (2 - 4)² + (2 - 4)² + (8 - 4)² = 24.

What is the R² of the model?

Exercise 4

&nbsp;Numerical Response&nbsp;

 

Explanation

The R² formula is:

R² = 1 - SSE/SST

Thus using our answers to the previous questions, we have that

R² = 1 - 18/24 = 0.25.

CheckShow Answer

- {{% resource_link "1f0b61bb-a29b-5ee7-5d26-5ed940cc2d1d" "Back: Video 2: One-Variable Linear Regression" %}}
- {{% resource_link "505bba75-964b-7b2c-74d8-ebcee23c8259" "Continue: Video 3: Multiple Linear Regression" %}}