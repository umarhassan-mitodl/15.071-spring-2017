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
uid: 578178b9-992b-b5c4-e6a9-8dc2f7c1ad78
video_metadata:
  youtube_id: null
---
## Quick Question

Redo the map from Video 6, but this time fill each state with the variable GunOwnership. This shows the percentage of people in each state who own a gun.

Which of the following states has the highest gun ownership rate? To see the state labels, take a look at {{% resource_link "0651aecd-b481-42bc-9a4a-903adecb4819" "the World Atlas map" %}}.

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} California {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} Montana {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Texas {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Louisiana {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Missouri {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

You can generate the gun ownership plot using the following command:

ggplot(murderMap, aes(x = long, y = lat, group=group, fill = GunOwnership)) + geom\_polygon(color="black") + scale\_fill\_gradient(low = "black", high = "red", guide="legend")

Of these five states, the one that is the most red is Montana.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "50eab6cd-164e-035d-9470-dc118924f686" "Back: Video 6: A Heatmap on the United States" %}}
- {{% resource_link "d2e3fa0c-b97e-d8cd-0b39-1b4b43303794" "Continue: Video 7: The Analytics Edge" %}}