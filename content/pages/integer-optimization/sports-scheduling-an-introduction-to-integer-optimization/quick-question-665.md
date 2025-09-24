---
content_type: page
description: '9.2 Sports Scheduling: An Introduction to Integer Optimization

  '
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '9.2 Sports Scheduling: An Introduction to Integer Optimization '
parent_type: CourseSection
parent_uid: fbf2b704-9246-466e-f247-36bff248b7c3
title: '9.2 Sports Scheduling: An Introduction to Integer Optimization'
uid: d7c69cd7-0f13-ee07-7976-805c01b4a9e2
video_metadata:
  youtube_id: null
---
## Quick Question

Suppose that you are trying to schedule 3 games between 6 teams (A, B, C, D, E, and F) that will occur simultaneously. Which of the following are feasible schedules? Select all that apply.

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="true" >}} A plays B, C plays D, and E plays F {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} A plays C, B plays D, and C plays F {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="true" >}} A plays F, B plays E, and C plays D {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} A plays B, B plays C, and C plays D {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="true" >}} A plays D, B plays E, and C plays F {{< /quiz_choice >}}{{< /quiz_choices >}}   
{{< quiz_solution >}}Explanation

Each of the teams has to play exactly one of the other teams for the games to occur simultaneously. In the second option, C is playing twice, which is impossible. In the fourth option, B and C are both playing twice.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

How many different feasible schedules are there?

{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} 5 {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} 10 {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="true" >}} 15 {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} 20 {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} 25 {{< /quiz_choice >}}{{< /quiz_choices >}}   
{{< quiz_solution >}}Explanation

There are 15 different feasible schedules. We can count them by observing that A can play any of the 5 teams. Once this is fixed, we have 4 teams left. There are 3 ways to make two pairs out of 4 teams. So in total, there are 5\*3 = 15 different schedules. Here is a list of all of them:

A plays B, C plays D, E plays F

A plays B, C plays E, D plays F

A plays B, C plays F, D plays E

A plays C, B plays D, E plays F

A plays C, B plays E, D plays F

A plays C, B plays F, D plays E

A plays D, B plays C, E plays F

A plays D, B plays E, C plays F

A plays D, B plays F, C plays E

A plays E, B plays C, D plays F

A plays E, B plays D, C plays F

A plays E, B plays F, C plays D

A plays F, B plays C, D plays E

A plays F, B plays D, C plays E

A plays F, B plays E, C plays D{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

{{% resource_link "30848359-f3cc-9abb-7ae9-95a7ade4fd97" "Continue: Video 2: The Optimization Problem" %}}