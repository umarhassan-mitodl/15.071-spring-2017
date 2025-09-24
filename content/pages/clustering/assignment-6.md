---
content_type: page
description: Document Clustering with Daily Kos
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: 6 Clustering
parent_type: CourseSection
parent_uid: 6e343503-94a0-f948-51f4-8f324b5f657f
title: 6.5 Assignment 6
uid: 940f7353-62c6-3a66-1b04-174a40036c29
video_metadata:
  youtube_id: null
---
## Document Clustering with Daily Kos

Document clustering, or text clustering, is a very popular application of clustering algorithms. A web search engine, like Google, often returns thousands of results for a simple query. For example, if you type the search term "jaguar" into Google, around 200 million results are returned. This makes it very difficult to browse or find relevant information, especially if the search term has multiple meanings. If we search for "jaguar", we might be looking for information about the animal, the car, or the Jacksonville Jaguars football team. 

Clustering methods can be used to automatically group search results into categories, making it easier to find relavent results. This method is used in the search engines PolyMeta and Helioid, as well as on FirstGov.gov, the official Web portal for the U.S. government. The two most common algorithms used for document clustering are Hierarchical and k-means. 

In this problem, we'll be clustering articles published on {{% resource_link "8b4b56cd-4dd5-4e2e-baab-058da5bde1f4" "Daily Kos" %}}, an American political blog that publishes news and opinion articles written from a progressive point of view. Daily Kos was founded by Markos Moulitsas in 2002, and as of September 2014, the site had an average weekday traffic of hundreds of thousands of visits. 

The file {{% resource_link "543653c0-7a59-7591-b020-24d3658f8d07" "dailykos (CSV - 10.1MB)" %}} contains data on 3,430 news articles or blogs that have been posted on Daily Kos. These articles were posted in 2004, leading up to the United States Presidential Election. The leading candidates were incumbent President George W. Bush (republican) and John Kerry (democratic). Foreign policy was a dominant topic of the election, specifically, the 2003 invasion of Iraq. 

Each of the variables in the dataset is a word that has appeared in at least 50 different articles (1,545 words in total). The set of  words has been trimmed according to some of the techniques covered in the previous week on text analytics (punctuation has been removed, and stop words have been removed). For each document, the variable values are the number of times that word appeared in the document. 

## Problem 1.1 - Hierarchical Clustering

Let's start by building a hierarchical clustering model. First, read the data set into R. Then, compute the distances (using method="euclidean"), and use hclust to build the model (using method="ward.D2"). You should cluster on all of the variables.

Running the dist function will probably take you a while. Why? Select all that apply.

 We have a lot of observations, so it takes a long time to compute the distance between each pair of observations. 

 We have a lot of variables, so the distance computation is long. 

 Our variables have a wide range of values, so the distances are more complicated. 

 The euclidean distance is known to take a long time to compute, regardless of the size of the data. 

## Problem 1.2 - Hierarchical Clustering

In this problem, we are trying to cluster news articles or blog posts into groups. This can be used to show readers categories to choose from when trying to decide what to read. Just thinking about this application, what are good choices for the number of clusters? Select all that apply.

 2 

 3 

 7 

 8 

## Problem 1.3 - Hierarchical Clustering

Let's pick 7 clusters. This number is reasonable according to the dendrogram, and also seems reasonable for the application. Use the cutree function to split your data into 7 clusters, calling the grouping variable "hierGroups".

Create 7 new datasets, each containing the observations from one of the clusters, using the following commands:

library(dplyr)

HierCluster1 = dailykos %>% filter(hierGroups == 1)

HierCluster2 = dailykos %>% filter(hierGroups == 2)

HierCluster3 = dailykos %>% filter(hierGroups == 3)

HierCluster4 = dailykos %>% filter(hierGroups == 4)

HierCluster5 = dailykos %>% filter(hierGroups == 5)

HierCluster6 = dailykos %>% filter(hierGroups == 6)

HierCluster7 = dailykos %>% filter(hierGroups == 7)

How many observations are in cluster 3?

Which cluster has the most observations?

 Cluster 1 

 Cluster 2 

 Cluster 3 

 Cluster 4 

 Cluster 5 

 Cluster 6 

 Cluster 7 

Which cluster has the fewest observations?

 Cluster 1 

 Cluster 2 

 Cluster 3 

 Cluster 4 

 Cluster 5 

 Cluster 6 

 Cluster 7 

You can split your data into clusters by first using the cutree function to compute the cluster numbers:

hierGroups = cutree(kosHierClust, k = 7)

Then, you can compute the subset associated with each cluster with the provided calls to the filter() function.

If you use the nrow function on each of these new datasets, you can see that cluster 3 has 324 observations, cluster 1 has the most observations, and cluster 7 has the fewest number of observations.

Alternatively, you could answer these questions by looking at the output of table(hierGroups).

More Advanced Approach:

There is a very useful function in R called the "split" function. Given a vector assigning groups like hierGroups, you could split dailykos into the clusters by typing:

HierCluster = split(dailykos, hierGroups)

Then cluster 1 can be accessed by typing HierCluster\[\[1\]\], cluster 2 can be accessed by typing HierCluster\[\[2\]\], etc. If you have a variable in your current R session called "split", you will need to remove it with rm(split) before using the split function.

## Problem 1.4 - Hierarchical Clustering

Instead of looking at the average value in each variable individually, we'll just look at the top 6 words in each cluster. To do this for cluster 1, type the following in your R console (where "HierCluster1" should be replaced with the name of your first cluster subset):

tail(sort(colMeans(HierCluster1)))

This computes the mean frequency values of each of the words in cluster 1, and then outputs the 6 words that occur the most frequently. The colMeans function computes the column (word) means, the sort function orders the words in increasing order of the mean values, and the tail function outputs the last 6 words listed, which are the ones with the largest column means.

What is the most frequent word in this cluster, in terms of average value? Enter the word exactly how you see it in the output:

## Problem 1.5 - Hierarchical Clustering

Now repeat the command given in the previous problem for each of the other clusters, and answer the following questions.

Which cluster could best be described as the cluster related to the Iraq war?

 Cluster 1 

 Cluster 2 

 Cluster 3 

 Cluster 4 

 Cluster 5 

 Cluster 6 

 Cluster 7 

In 2004, one of the candidates for the Democratic nomination for the President of the United States was Howard Dean, John Kerry was the candidate who won the democratic nomination, and John Edwards with the running mate of John Kerry (the Vice President nominee). Given this information, which cluster best corresponds to the democratic party?

 Cluster 1 

 Cluster 2 

 Cluster 3 

 Cluster 4 

 Cluster 5 

 Cluster 6 

 Cluster 7 

You can repeat the command on each of the clusters by typing the following:

tail(sort(colMeans(HierCluster2)))

tail(sort(colMeans(HierCluster3)))

tail(sort(colMeans(HierCluster4)))

tail(sort(colMeans(HierCluster5)))

tail(sort(colMeans(HierCluster6)))

tail(sort(colMeans(HierCluster7)))

## Problem 2.1 - K-Means Clustering

Now, run k-means clustering, setting the seed to 1000 right before you run the kmeans function. Again, pick the number of clusters equal to 7. You don't need to add the iters.max argument.

Subset your data into the 7 clusters (7 new datasets) by using the "cluster" variable of your kmeans output.

How many observations are in Cluster 3?

Which cluster has the most observations?

 Cluster 1 

 Cluster 2 

 Cluster 3 

 Cluster 4 

 Cluster 5 

 Cluster 6 

 Cluster 7 

Which cluster has the fewest number of observations?

 Cluster 1 

 Cluster 2 

 Cluster 3 

 Cluster 4 

 Cluster 5 

 Cluster 6 

 Cluster 7 

## Problem 2.2 - K-Means Clustering

Now, output the six most frequent words in each cluster, like we did in the previous problem, for each of the k-means clusters.

Which k-means cluster best corresponds to the Iraq War?

 Cluster 1 

 Cluster 2 

 Cluster 3 

 Cluster 4 

 Cluster 5 

 Cluster 6 

 Cluster 7 

Which k-means cluster best corresponds to the democratic party? (Remember that we are looking for the names of the key democratic party leaders.)

 Cluster 1 

 Cluster 2 

 Cluster 3 

 Cluster 4 

 Cluster 5 

 Cluster 6 

 Cluster 7 

You can output the most frequent words in each of the k-means clusters by using the following commands:

tail(sort(colMeans(KmeansCluster1)))

tail(sort(colMeans(KmeansCluster2)))

tail(sort(colMeans(KmeansCluster3)))

tail(sort(colMeans(KmeansCluster4)))

tail(sort(colMeans(KmeansCluster5)))

tail(sort(colMeans(KmeansCluster6)))

tail(sort(colMeans(KmeansCluster7)))

## Problem 2.3 - K-Means Clustering

For the rest of this problem, we'll ask you to compare how observations were assigned to clusters in the two different methods. Use the table function to compare the cluster assignment of hierarchical clustering to the cluster assignment of k-means clustering. The following will place the k-means clusters on the rows of the table and the hierarchical clusters on the columns:

table(KmeansCluster$cluster, hierGroups)

Which Hierarchical Cluster best corresponds to K-Means Cluster 2?

 Hierarchical Cluster 1 

 Hierarchical Cluster 2 

 Hierarchical Cluster 3 

 Hierarchical Cluster 4 

 Hierarchical Cluster 5 

 Hierarchical Cluster 6 

 Hierarchical Cluster 7 

 No Hierarchical Cluster contains at least half of the points in K-Means Cluster 2.

## Problem 2.4 - K-Means Clustering

Which Hierarchical Cluster best corresponds to K-Means Cluster 3?

 Hierarchical Cluster 1 

 Hierarchical Cluster 2 

 Hierarchical Cluster 3 

 Hierarchical Cluster 4 

 Hierarchical Cluster 5 

 Hierarchical Cluster 6 

 Hierarchical Cluster 7 

 No Hierarchical Cluster contains at least half of the points in K-Means Cluster 3. 

{{% resource_link "f38d14c2-d66c-5504-4b9e-071235d5fdd8" "Back: Video 7: Comparing Methods" %}}