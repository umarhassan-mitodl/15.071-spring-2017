---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '6.2 Recommendations Worth a Million: An Introduction to Clustering '
parent_type: CourseSection
parent_uid: b091b1be-c85a-85e0-60a8-3b7905c9dcce
title: '6.2 Recommendations Worth a Million: An Introduction to Clustering'
uid: 47a1cfac-748d-6647-732e-f8b91e90cc4f
video_metadata:
  youtube_id: null
---
## Quick Question

 

Using the table function in R, please answer the following questions about the dataset "movies".

How many movies are classified as comedies?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

How many movies are classified as westerns?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

How many movies are classified as romance AND drama?

Exercise 3

&nbsp;Numerical Response&nbsp;

 

Explanation

You can answer these questions by using the following commands:

table(movies$Comedy)

table(movies$Western)

table(movies$Romance, movies$Drama)

CheckShow Answer

 

- {{% resource_link "97456de3-0891-98f1-c51a-a74e3d11930c" "Back: Video 6: Getting the Data" %}}
- {{% resource_link "c0ef063d-c722-b998-a530-922a135bd19e" "Continue: Video 7: Hierarchical Clustering in R" %}}