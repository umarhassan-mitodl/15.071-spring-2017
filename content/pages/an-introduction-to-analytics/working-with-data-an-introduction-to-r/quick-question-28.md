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
uid: 85a26423-d9d7-5842-c382-af54b0eaaadd
video_metadata:
  youtube_id: null
---
## Quick Question

 

Please answer the following questions using the entire data frame WHO (and not one of the subsets we have created in R).

What is the mean value of the "Over60" variable?

Exercise 1

 Numerical Response 

 

Explanation

You can compute this value by either typing mean(WHO$Over60) in your R console, or by typing summary(WHO$Over60) in your R console. The output is 11.16.

Which country has the smallest percentage of the population over 60?

Exercise 2

 Japan 

 United Arab Emirates (UAE) 

 Sierra Leone 

 Cuba 

 Luxembourg 

 Mali 

Explanation

To get this value, you should type which.min(WHO$Over60) in your R console. The output is 183. Then, to see the name of the 183rd country in your data frame, type WHO$Country\[183\] in your R console. The output is United Arab Emirates.

Which country has the largest literacy rate?

Exercise 3

 Japan 

 United Arab Emirates (UAE) 

 Sierra Leone 

 Cuba 

 Luxembourg 

 Mali 

Explanation

To get this value, you should type which.max(WHO$LiteracyRate) in your R console. The output is 44. Then, to see the name of the 44th country in your data frame, type WHO$Country\[44\] in your R console. The output is Cuba.

CheckShow Answer

 

- {{% resource_link "eeb22344-b682-07d4-d7b6-e8fcc1cd06b6" "Back: Video 5: Data Analysis - Summary Statistics and Scatterplots" %}}
- {{% resource_link "050acd52-9f55-fd87-a5c2-98728b4daa03" "Continue: Video 6: Data Analysis - Plots and Summary Tables" %}}