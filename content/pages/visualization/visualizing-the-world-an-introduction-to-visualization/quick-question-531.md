---
content_type: page
description: '7.2 Visualizing the World: An Introduction to Visualization

  '
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '7.2 Visualizing the World: An Introduction to Visualization'
parent_type: CourseSection
parent_uid: 274ac6b9-daf6-cd65-874e-c643ab327953
title: '7.2 Visualizing the World: An Introduction to Visualization'
uid: a7c29773-2c9a-e308-c35b-598232cd91c6
video_metadata:
  youtube_id: null
---
## Quick Question

Create the fertility rate versus population under 15 plot again:

ggplot(WHO, aes(x = FertilityRate, y = Under15)) + geom\_point()

Now, color the points by the Region variable.

Note: You can add scale\_color\_brewer(palette="Dark2") to your plot if you are having a hard time distinguishing the colors (this color palette is often better if you are colorblind). To use this option, you should just add scale\_color\_brewer(palette="Dark2") to your plotting command right after geom\_point().

One region in particular has a lot of countries with a very low fertility rate and a very low percentage of the population under 15. Which region is it?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} Africa {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} Americas {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} Eastern Mediterranean {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="true" >}} Europe {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} South-East Asia {{< /quiz_choice >}}    
{{< quiz_choice isCorrect="false" >}} Western Pacific {{< /quiz_choice >}}{{< /quiz_choices >}}    
{{< quiz_solution >}}Explanation

You can color the points by region if you adjust the command to the following:

ggplot(WHO, aes(x = FertilityRate, y = Under15, color=Region)) + geom\_point()

Most of the countries in Europe have a very low fertility rate and a very low percentage of the population under 15.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

{{% resource_link "be1c12bd-caf2-9b71-c12f-50c42551b8a6" "Back: Video 5: Advanced Scatterplots Using ggplot" %}}