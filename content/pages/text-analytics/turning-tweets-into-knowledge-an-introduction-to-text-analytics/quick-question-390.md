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
uid: ef17614f-a013-2a73-a771-05ff3c4311af
video_metadata:
  youtube_id: null
---
## Quick Question

In the previous video, we showed a list of all words that appear at least 20 times in our tweets. Which of the following words appear at least 100 times? Select all that apply. (HINT: use the findFreqTerms function)

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} app {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} buy {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} freak {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} ipad {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} iphon {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} itun {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} like {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} love {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} new {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} think {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

To answer this question, you need to run the following command in R:

findFreqTerms(frequencies, lowfreq=100)

This outputs the words that appear at least 100 times in our tweets. They are "iphon", "itun", and "new".{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "b8c9ec48-67a6-977e-b31d-b490c342ef38" "Back: Video 6: Bag of Words in R" %}}
- {{% resource_link "6faa3dc6-2c17-bf81-844b-b5d994e997d9" "Continue: Video 7: Predicting Sentiment" %}}