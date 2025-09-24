---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '1.3 Working with Data: An Introduction to R '
parent_type: CourseSection
parent_uid: 1ac933da-13d1-3dfa-2e38-03abf2d6971f
title: '1.3 Working with Data: An Introduction to R'
uid: e3496fee-bb68-27a9-7779-dea4bd50cc77
video_metadata:
  youtube_id: null
---
## Quick Question

If you want to know the mean value of a numerical variable, which function could you use?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} str {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="true" >}} summary {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} I can't figure out this information using either of these functions. {{< /quiz_choice >}}{{< /quiz_choices >}}    
{{< quiz_solution >}}Explanation

If you using the summary function (in the video, we typed summary(WHO) in our R console) you can see a statistical summary of each variable. For numerical variables, the mean value is listed.

{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

If you want to know the standard deviation of a numerical variable, which function could you use?

{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} str {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} summary {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="true" >}} I can't figure out this information using either of these functions. {{< /quiz_choice >}}{{< /quiz_choices >}}    
{{< quiz_solution >}}Explanation

Neither the str function nor the summary function provides the standard deviation value of a variable. We'll see how to compute this value in the next video.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "70fe7ef6-c257-30ef-b982-22eac766dbc4" "Back: Video 4: Loading Data Files" %}}
- {{% resource_link "eeb22344-b682-07d4-d7b6-e8fcc1cd06b6" "Continue: Video 5: Data Analysis - Summary Statistics and Scatterplots" %}}