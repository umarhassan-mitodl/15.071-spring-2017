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
uid: d97e0bd0-54ac-d9a6-df59-9f1b2e2daf73
video_metadata:
  youtube_id: null
---
## Quick Question

Suppose we add another variable, Average Winter Temperature, to our model to predict wine price. Is it possible for the model's R² value to go down from 0.83 to 0.80?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} No, the model's R² value can only decrease to 0.81 by adding new variables. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} No, the model's R² value can not decrease at all by adding new variables.  {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Yes, the R² value could decrease to 0.80. {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

The model's R² value can never decrease from adding new variables to the model. This is due to the fact that it is always possible to set the coefficient for the new variable to zero in the new model. However, this would be the same as the old model. So the only reason to make the coefficient non-zero is if it improves the R² value of the model, since linear regression picks the coefficients to minimize the error terms, which is the same as maximizing the R².{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "505bba75-964b-7b2c-74d8-ebcee23c8259" "Back: Video 3: Multiple Linear Regression" %}}
- {{% resource_link "9f456e81-561b-ed0d-7c0a-516cd7739d20" "Continue: Video 4: Linear Regression in R" %}}