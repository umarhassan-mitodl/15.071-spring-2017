---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '5.4 Predictive Coding: Bringing Text Analytics to the Courtroom  (Recitation)'
parent_type: CourseSection
parent_uid: d4b1a3b9-42ed-98d1-94fe-b3777ba22595
title: '5.4 Predictive Coding: Bringing Text Analytics to the Courtroom  (Recitation)'
uid: 1924c416-bffb-7319-6622-8542170e6c66
video_metadata:
  youtube_id: null
---
## Video 3: Pre-Processing

**Important Note:** In the following video, we ask you to use the "tm" package to perform the pre-processing steps. Due to function changes that occurred after this video was recorded, you will need to run the following command immediately after converting all of the words to lowercase letters (it converts all documents in the corpus to the PlainTextDocument type):

corpus = tm\_map(corpus, PlainTextDocument)

Then you can continue with the R commands as they are in the video.

{{< resource uuid="4e41dd76-b35c-6d67-c10d-2253c4352758" >}}

If the code length(stopwords("english")) does not return 174 for you, then please run the line of code in {{% resource_link "fe588eb6-9d66-3b5e-0fbd-f6c8a2564dfd" "stopwords (TXT) file" %}}, which will store the standard stop words in a variable called sw. When removing stop words, use tm\_map(corpus, removeWords, sw) instead of tm\_map(corpus, removeWords, stopwords("english")). 

- {{% resource_link "d2b6e4bc-cf8f-0017-b1fc-3de36e683c9a" "Back: Video 2: The Data" %}}
- {{% resource_link "8a96d7cd-01b9-50c8-be68-959be293ab00" "Continue: Video 4: Bag of Words" %}}