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
uid: 5e8b108b-e5fd-9320-8fe7-cd8bd5420c69
video_metadata:
  youtube_id: null
---
## Quick Question

For each tweet, we computed an overall score by averaging all five scores assigned by the Amazon Mechanical Turk workers. However, Amazon Mechanical Turk workers might make significant mistakes when labeling a tweet. The mean could be highly affected by this.

Which of the three alternative metrics below would best capture the typical opinion of the five Amazon Mechanical Turk workers, would be less affected by mistakes, and is well-defined regardless of the five labels?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="true" >}} An overall score equal to the median (middle) score {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} An overall score equal to the majority score {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} An overall score equal to the minimum score {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

The correct answer is the first one - the median would capture the typical opinion of the workers and tends to be less affected by significant mistakes. The majority score might not have given a score to all tweets because they might not all have a majority score (consider a tweet with scores 0, 0, 1, 1, and 2). The minimum score does not necessarily capture the typical opinion and could be highly affected by mistakes (consider a tweet with scores -2, 1, 1, 1, 1).{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "f8520c5e-c3cf-3c3f-e046-72b8a73ae3a5" "Back: Video 3: Creating the Dataset" %}}
- {{% resource_link "d4dd2919-7499-fdd3-dac1-bca9ea53d04c" "Continue: Video 4: Bag of Words" %}}