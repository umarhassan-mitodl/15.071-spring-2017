---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '5.2 Turning Tweets into Knowledge: An Introduction to Text Analytics'
parent_type: CourseSection
parent_uid: aea3bc9c-07f7-3648-65c4-6fec93dd8515
title: '5.2 Turning Tweets into Knowledge: An Introduction to Text Analytics'
uid: 2199fef8-1de9-2125-4a61-069ec69f588e
video_metadata:
  youtube_id: null
---
## Quick Question

 

Given a corpus in R, how many commands do you need to run in R to clean up the irregularities (removing capital letters and punctuation)?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

How many commands do you need to run to stem the document?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

In R, you can clean up the irregularities with two lines:

corpus = tm\_map(corpus, tolower)

corpus = tm\_map(corpus, removePunctuation)

And you can stem the document with one line:

corpus = tm\_map(corpus, stemDocument)

CheckShow Answer

 

- {{% resource_link "6cb54a0c-457f-eabd-e1b7-dd4d95399d8c" "Back: Video 5: Pre-Processing in R" %}}
- {{% resource_link "b8c9ec48-67a6-977e-b31d-b490c342ef38" "Continue: Video 6: Bag of Words in R" %}}