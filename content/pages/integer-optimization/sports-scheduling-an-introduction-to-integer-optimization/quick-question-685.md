---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '9.2 Sports Scheduling: An Introduction to Integer Optimization '
parent_type: CourseSection
parent_uid: fbf2b704-9246-466e-f247-36bff248b7c3
title: '9.2 Sports Scheduling: An Introduction to Integer Optimization'
uid: 15f4c72a-4356-c958-e48e-1d8430f4b6f0
video_metadata:
  youtube_id: null
---
## Quick Question

 

Suppose we had two more teams in our tournament (for a total of 6 teams). Each division would have 3 teams. So each team plays **two** teams twice (the teams in their division), and each team plays three teams once (the teams in the other division). This means that the tournament will last for 7 weeks. How many decision variables would we have?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

We would have 105 decision variables because we have 7 weeks, and 15 different pairs of teams.

How many constraints would we have? Don't include the constraints that force the variables to be binary when counting the constraints here. (HINT: We would have 6 division constraints, since each pair in each division needs to play twice.)

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

We would have 6 division constraints, 9 non-division constraints (each of the three teams in one division has to play each of the three teams in the other division), and 42 constraints to make sure each team only plays one team each week (6 teams times 7 weeks).

CheckShow Answer

- {{% resource_link "611ff2e2-25d3-1291-5c17-05e9cd35ede7" "Back: Video 3: Solving the Problem" %}}
- {{% resource_link "209100b3-8ec9-d10b-5925-656d460ca2ad" "Continue: Video 4: Logical Constraints" %}}