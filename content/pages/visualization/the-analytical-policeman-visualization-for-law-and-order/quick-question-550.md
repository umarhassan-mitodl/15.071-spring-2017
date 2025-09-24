---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '7.3 The Analytical Policeman: Visualization for Law and Order'
parent_type: CourseSection
parent_uid: 716f78f6-1fe6-c5f4-7370-d7a3c4127827
title: '7.3 The Analytical Policeman: Visualization for Law and Order'
uid: e685ba71-8462-a41f-dc85-159d8c6cd469
video_metadata:
  youtube_id: null
---
## Quick Question

Create a new line plot, like the one in Video 3, but add the argument "linetype=2". So the geom\_line part of the plotting command should look like:

geom\_line(aes(group=1), linetype=2)

What does this do?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} Makes the line thicker {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Changes the color of the line to blue {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} Makes the line dashed {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Makes the line lighter in color {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

The linetype parameter makes the line dashed, and the alpha parameter makes the line lighter in color, or more transparent. The two plots can be generated with the following commands:

ggplot(WeekdayCounts, aes(x = Var1, y = Freq)) + geom\_line(aes(group=1), linetype=2) + xlab("Day of the Week") + ylab("Total Motor Vehicle Thefts")

ggplot(WeekdayCounts, aes(x = Var1, y = Freq)) + geom\_line(aes(group=1), alpha=0.3) + xlab("Day of the Week") + ylab("Total Motor Vehicle Thefts"){{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

Now, change the alpha parameter to 0.3 by replacing "linetype=2" with "alpha=0.3" in the plot command. What does this do?

{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} Makes the line thicker {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Changes the color of the line to blue {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Makes the line dashed {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} Makes the line lighter in color {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

The linetype parameter makes the line dashed, and the alpha parameter makes the line lighter in color, or more transparent. The two plots can be generated with the following commands:

ggplot(WeekdayCounts, aes(x = Var1, y = Freq)) + geom\_line(aes(group=1), linetype=2) + xlab("Day of the Week") + ylab("Total Motor Vehicle Thefts")

ggplot(WeekdayCounts, aes(x = Var1, y = Freq)) + geom\_line(aes(group=1), alpha=0.3) + xlab("Day of the Week") + ylab("Total Motor Vehicle Thefts"){{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "1bd0d7e9-c5ce-0101-823b-0faa796ad873" "Back: Video 3: A Line Plot" %}}
- {{% resource_link "7a8ce8b6-91e9-92d1-00a8-3e4b86041a1a" "Continue: Video 4: A Heatmap" %}}