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
uid: 6cb54a0c-457f-eabd-e1b7-dd4d95399d8c
video_metadata:
  youtube_id: null
---
## Video 5: Pre-Processing in R

**Note:**  the dataset "tweets.csv" used in the rest of this lecture is not available to OCW users.

In the following video, we ask you to install the "tm" package to perform the pre-processing steps. Due to function changes that occurred after this video was recorded, you will need to run the following command immediately after converting all of the words to lowercase letters (it converts all documents in the corpus to the PlainTextDocument type):

corpus = tm\_map(corpus, PlainTextDocument)

Then you can continue with the R commands as they are in the video.

{{< resource uuid="27420fff-8aba-cd00-e9e0-b59405fc71cc" >}}

## Non-Standard Stop Word Lists

If the code length(stopwords("english")) does not return 174 for you, then please run the line of code in {{% resource_link "cdd1dacd-338e-5346-32e1-cc15dec3e47d" "stopwords (TXT) file" %}}, which will store the standard stop words in a variable called sw. When removing stop words, use tm\_map(corpus, removeWords, sw) instead of tm\_map(corpus, removeWords, stopwords("english")). 

## Language Settings

If you downloaded and installed R in a location other than the United States, you might encounter some issues when using the bag of words approach (since the pre-processing tasks used here depend on the English language). To fix this, you will need to type in your R console:

Sys.setlocale("LC\_ALL", "C")

This will only change the locale for your current R session, so please make a note to run this command when you are working on any lectures or exercises that might depend on the English lanugage (for example, removing stop words).

- {{% resource_link "820047e7-15d4-d347-40e0-11a49546196a" "Back: Quick Question" %}}
- {{% resource_link "2199fef8-1de9-2125-4a61-069ec69f588e" "Continue: Quick Question" %}}