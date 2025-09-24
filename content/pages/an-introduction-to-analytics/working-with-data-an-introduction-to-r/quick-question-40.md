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
uid: 64119b70-3f1d-42bf-97ce-9f87d64a094c
video_metadata:
  youtube_id: null
---
## Quick Question

Use the tapply function to find the average child mortality rate of countries in each region.

Which region has the lowest average child mortality rate across all countries in that region?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} Africa {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} Americas {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} Eastern Mediterranean {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="true" >}} Europe {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} South-East Asia {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} Western Pacific {{< /quiz_choice >}}{{< /quiz_choices >}}    
{{< quiz_solution >}}Explanation

You can find the average child mortaility rate of countries in each region by using the following command:

tapply(WHO$ChildMortality, WHO$Region, mean)

The output tells us that Europe has the lowest average child mortality rate across all countries, with an average of 10.05.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "050acd52-9f55-fd87-a5c2-98728b4daa03" "Back: Video 6: Data Analysis - Plots and Summary Tables" %}}
- {{% resource_link "5b9fe301-be29-cb46-df9f-edbbf748fc62" "Continue: Video 7: Saving with Script Files" %}}