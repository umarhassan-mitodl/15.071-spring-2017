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
uid: 2f9da0d0-e4ef-29ad-6861-c462ec145784
video_metadata:
  youtube_id: null
---
## Quick Question

In the previous video, we constructed two CART models. The first CART model, without the loss matrix, predicted bucket 1 for 78.6% of the observations in the test set. Did the second CART model, with the loss matrix, predict bucket 1 for more or fewer of the observations, and why?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} According to the penalty matrix, some of the worst types of errors are to not predict bucket 1 when the actual cost bucket is bucket 1. Therefore, the model with the penalty matrix predicted bucket 1 more frequently.  {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} According to the penalty matrix, some of the worst types of errors are to predict bucket 1 when the actual cost bucket is higher. Therefore, the model with the penalty matrix predicted bucket 1 more frequently. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} According to the penalty matrix, some of the worst types of errors are to not predict bucket 1 when the actual cost bucket is bucket 1. Therefore, the model with the penalty matrix predicted bucket 1 less frequently.  {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} According to the penalty matrix, some of the worst types of errors are to predict bucket 1 when the actual cost bucket is higher. Therefore, the model with the penalty matrix predicted bucket 1 less frequently.  {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

If you look at the classification matrix for the second CART model, we predicted bucket 1 less frequently. This is because, according to the penalty matrix, some of the worst types of errors are to predict bucket 1 when the actual cost bucket is higher.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "42af8e9a-43f3-ab0e-231b-e7ab1d08c0ca" "Back: Video 8: Predicting Healthcare Cost in R" %}}
- {{% resource_link "bc9ba16d-f4b1-d68b-b2a3-dfc6700cfac3" "Continue: Video 9: Results" %}}