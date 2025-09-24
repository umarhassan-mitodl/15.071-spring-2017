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
uid: 04ad6920-c418-b28f-1259-8538cd8136cf
video_metadata:
  youtube_id: null
---
## Quick Question

Which of the following are NOT valid values for an out-of-sample (test set) R² ? Select all that apply.

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} -7.0 {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} -0.3 {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} 0.0 {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} 0.6 {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} 1.0 {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} 2.4 {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

The formula for R² is

R² = 1 - SSE/SST,

where SST is calculated using the average value of the dependent variable on the training set.

Since SSE and SST are the sums of squared terms, we know that both will be positive. Thus SSE/SST must be greater than or equal to zero. This means it is not possible to have an out-of-sample R² value of 2.4.

However, all other values are valid (even the negative ones!), since SSE can be more or less than SST, due to the fact that this is an out-of-sample R², not a model R².{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "9b500b6f-7f1d-17af-5de0-ab9946895858" "Back: Video 7: Making Predictions" %}}
- {{% resource_link "df5ef364-59d3-2e3f-98ec-9d920d6c5e1d" "Continue: Video 8: Comparing the Model to the Experts" %}}