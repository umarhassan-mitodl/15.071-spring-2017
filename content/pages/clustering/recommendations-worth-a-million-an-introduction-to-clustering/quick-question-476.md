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
uid: 4d3cfab6-9136-623b-888a-5451d2fad159
video_metadata:
  youtube_id: null
---
## Quick Question

Run the cutree function again to create the cluster groups, but this time pick k = 2 clusters. It turns out that the algorithm groups all of the movies that only belong to one specific genre in one cluster (cluster 2), and puts all of the other movies in the other cluster (cluster 1). What is the genre that all of the movies in cluster 2 belong to?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} Action {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Adventure {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Animation {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Children's {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Comedy {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Crime {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Documentary {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} Drama {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Fantasy {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Film Noir {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Horror {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Musical {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Mystery {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Romance {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Sci-Fi {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Thriller {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} War {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Western {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

You can redo the cluster grouping with just two clusters by running the following command:

clusterGroups = cutree(clusterMovies, k = 2)

Then, by using the tapply function just like we did in the video, you can see the average value in each genre and cluster. It turns out that all of the movies in the second cluster belong to the drama genre.

Alternatively, you can use colMeans or lapply as explained below Video 7.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "c0ef063d-c722-b998-a530-922a135bd19e" "Back: Video 7: Hierarchical Clustering in R" %}}
- {{% resource_link "9e0e5a25-71bb-afda-ded1-01bdcdce7158" "Continue: Video 8: The Analytics Edge of Recommendation Systems" %}}