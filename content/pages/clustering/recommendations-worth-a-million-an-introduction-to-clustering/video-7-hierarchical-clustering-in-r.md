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
uid: c0ef063d-c722-b998-a530-922a135bd19e
video_metadata:
  youtube_id: null
---
## Video 7: Hierarchical Clustering in R

**Important Note:** In this video, we use the "ward" method to do hierarchical clustering. This method was recently renamed in R to "ward.D". If you are following along in R while watching the video, you will need to use the following command when doing the hierarchical clustering ("ward" is replaced with "ward.D"):

clusterMovies = hclust(distances, method = "ward.D")

{{< resource uuid="586e592d-afc4-55b0-19b2-7dd6d67ab5bb" >}}

## An Advanced Approach to Finding Cluster Centroids

In this video, we explain how you can find the cluster centroids by using the function "tapply" for each variable in the dataset. While this approach works and is familiar to us, it can be a little tedious when there are a lot of variables. An alternative approach is to use the colMeans function. With this approach, you only have one command for each cluster instead of one command for each variable. If you run the following command in your R console, you can get all of the column (variable) means for cluster 1:

colMeans(subset(movies\[2:20\], clusterGroups == 1))

You can repeat this for each cluster by changing the clusterGroups number. However, if you also have a lot of clusters, this approach is not that much more efficient than just using the tapply function.

A more advanced approach uses the "split" and "lapply" functions. The following command will split the data into subsets based on the clusters:

spl = split(movies\[2:20\], clusterGroups)

Then you can use spl to access the different clusters, because

spl\[\[1\]\]

is the same as

subset(movies\[2:20\], clusterGroups == 1)

so colMeans(spl\[\[1\]\]) will output the centroid of cluster 1. But an even easier approach uses the lapply function. The following command will output the cluster centroids for all clusters:

lapply(spl, colMeans)

The lapply function runs the second argument (colMeans) on each element of the first argument (each cluster subset in spl). So instead of using 19 tapply commands, or 10 colMeans commands, we can output our centroids with just two commands: one to define spl, and then the lapply command.

Note that if you have a variable called "split" in your current R session, you will need to remove it with rm(split) so that you can use the split function.

In this video, we use the spreadsheet {{% resource_link "f5d06b43-b7c6-dffc-2755-2d12924b69ee" "ClusterMeans (ODS" %}}). This file can be opened in LibreOffice or OpenOffice. 

- {{% resource_link "47a1cfac-748d-6647-732e-f8b91e90cc4f" "Back: Quick Question" %}}
- {{% resource_link "4d3cfab6-9136-623b-888a-5451d2fad159" "Continue: Quick Question" %}}