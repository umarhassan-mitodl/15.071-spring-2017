---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '2.3 Moneyball: The Power of Sports Analytics '
parent_type: CourseSection
parent_uid: fcb6a63f-4737-920a-80bf-15309d3ee7b6
title: '2.3 Moneyball: The Power of Sports Analytics'
uid: 213159bb-6e06-797c-4852-59579c290272
video_metadata:
  youtube_id: null
---
## Quick Question

In 2012 and 2013, there were 10 teams in the MLB playoffs: the six teams that had the most wins in each baseball division, and four "wild card" teams. The playoffs start between the four wild card teams - the two teams that win proceed in the playoffs (8 teams remaining). Then, these teams are paired off and play a series of games. The four teams that win are then paired and play to determine who will play in the World Series. 

We can assign rankings to the teams as follows:

 

- **Rank 1**: the team that won the World Series
- **Rank 2**: the team that lost the World Series
- **Rank 3**: the two teams that lost to the teams in the World Series
- **Rank 4**: the four teams that made it past the wild card round, but lost to the above four teams
- **Rank 5**: the two teams that lost the wild card round

In your R console, create a corresponding rank vector by typing

teamRank = c(1,2,3,3,4,4,4,4,5,5)

In this quick question, we'll see how well these rankings correlate with the regular season wins of the teams. In 2012, the ranking of the teams and their regular season wins were as follows:

- **Rank 1**: San Francisco Giants (Wins = 94)
- **Rank 2**: Detroit Tigers (Wins = 88)
- **Rank 3**: New York Yankees (Wins = 95), and St. Louis Cardinals (Wins = 88)
- **Rank 4**: Baltimore Orioles (Wins = 93), Oakland A's (Wins = 94), Washington Nationals (Wins = 98), Cincinnati Reds (Wins = 97)
- **Rank 5**: Texas Rangers (Wins = 93), and Atlanta Braves (Wins = 94) 

Create a vector in R called wins2012, that has the wins of each team in 2012, in order of rank (the vector should have 10 numbers).

In 2013, the ranking of the teams and their regular season wins were as follows:

- **Rank 1**: Boston Red Sox (Wins = 97)
- **Rank 2**: St. Louis Cardinals (Wins = 97)
- **Rank 3**: Los Angeles Dodgers (Wins = 92), and Detroit Tigers (Wins = 93)
- **Rank 4**: Tampa Bay Rays (Wins = 92), Oakland A's (Wins = 96), Pittsburgh Pirates (Wins = 94), and Atlanta Braves (Wins = 96)
- **Rank 5**: Cleveland Indians (Wins = 92), and Cincinnati Reds (Wins = 90) 

Create another vector in R called wins2013, that has the wins of each team in 2013, in order of rank (the vector should have 10 numbers).

What is the correlation between teamRank and wins2012?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

You should have typed the following three lines in your R console:

teamRank = c(1,2,3,3,4,4,4,4,5,5)

wins2012 = c(94,88,95,88,93,94,98,97,93,94)

cor(teamRank, wins2012)

The output of the last line is 0.3477129, which is the correlation between teamRank and wins2012.

What is the correlation between teamRank and wins2013?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

You should have typed the following three lines in your R console:

teamRank = c(1,2,3,3,4,4,4,4,5,5)

wins2013 = c(97,97,92,93,92,96,94,96,92,90)

cor(teamRank, wins2013)

The output of the last line is -0.6556945, which is the correlation between teamRank and wins2013.

Since one of the correlations is positive and the other is negative, this means that there does not seem to be a pattern between regular season wins and winning the playoffs. We wouldn't feel comfortable making a bet for this year given this data!

CheckShow Answer

- {{% resource_link "a7a0fe58-cf53-ad2e-8a48-00f4efacbaed" "Back: Video 5: Winning the World Series" %}}
- {{% resource_link "9694655b-1331-2f40-a587-b03a675d6122" "Continue: Video 6: The Analytics Edge in Sports" %}}