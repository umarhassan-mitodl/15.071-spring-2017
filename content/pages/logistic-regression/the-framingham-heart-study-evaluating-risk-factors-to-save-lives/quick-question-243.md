---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '3.3 The Framingham Heart Study: Evaluating Risk Factors to Save Lives '
parent_type: CourseSection
parent_uid: 58bb6065-48df-9c3a-8c14-8318a4e0e5c7
title: '3.3 The Framingham Heart Study: Evaluating Risk Factors to Save Lives'
uid: 332c772a-c343-1943-e27c-0bb91f073b40
video_metadata:
  youtube_id: null
---
## Quick Question

For which of the following models should external validation be used? Consider both the population used to train the model, and the population that the model will be used on. (Select all that apply.)

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="true" >}} A model to predict obesity risk. Data from a random sample of California residents was used to build the model, and we want to use the model to predict the obesity risk of all United States residents. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} A model to predict the stress of MIT students. Data from a random sample of MIT students was used to build the model, and we want to use the model to predict the stress level of all MIT students. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} A model to predict the probability of a runner winning a marathon. Data from all runners in the Boston Marathon was used to build the model, and we want use the model to predict the probability of winning for all people who run marathons.  {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

In the first and third models, we are using a special sub-population to build the model. While we can use the model for that sub-population, we should use external validation to test the model on other populations. The second model uses data from a special sub-population, but the model is only intended for that sub-population, so external validation is not necessary.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "4f9a84c3-4f7f-3867-891d-be7fae75a149" "Back: Video 4: Validating the Model" %}}
- {{% resource_link "4d65e763-1a9d-6885-f511-959c8382aa48" "Continue: Video 5: Interventions" %}}