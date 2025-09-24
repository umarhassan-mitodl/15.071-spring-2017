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
uid: 20a0ee2d-c563-bbc1-243a-facac65c21f3
video_metadata:
  youtube_id: null
---
## Quick Question

Use the dataset wine.csv to create a linear regression model to predict Price using HarvestRain and WinterRain as independent variables, like you did in the previous quick question. Using the summary output of this model, answer the following questions:

Is the coefficient for HarvestRain significant?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="true" >}} Yes {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} No {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} I can't answer this question using the summary output.

 {{< /quiz_choice >}}{{< /quiz_choices >}}   
{{< quiz_solution >}}Explanation

You can create the model and look at the summary output with the following command:

model = lm(Price ~ WinterRain + HarvestRain, data=wine)

summary(model)

From the summary output, you can see that HarvestRain is significant (two stars), but WinterRain is not (no stars).{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

Is the coefficient for WinterRain significant?

{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} Yes {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="true" >}} No {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} I can't answer this question using the summary output. {{< /quiz_choice >}}{{< /quiz_choices >}}   
{{< quiz_solution >}}Explanation

You can create the model and look at the summary output with the following command:

model = lm(Price ~ WinterRain + HarvestRain, data=wine)

summary(model)

From the summary output, you can see that HarvestRain is significant (two stars), but WinterRain is not (no stars).{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

Note that you will need to answer both questions before checking your answers.

- {{% resource_link "6111ddea-9e02-70be-a097-8feb66c8bf60" "Back: Video 5: Understanding the Model" %}}
- {{% resource_link "1ab830be-7abc-5468-421c-996f95e8e252" "Continue: Video 6: Correlation and Multicollinearity" %}}