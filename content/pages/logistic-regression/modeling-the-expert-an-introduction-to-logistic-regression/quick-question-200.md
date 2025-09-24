---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
parent_type: CourseSection
parent_uid: 3063320a-4175-6b8a-4fa9-892f61b52c0d
title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
uid: d9817f81-c4ac-257a-ed44-548eaa714059
video_metadata:
  youtube_id: null
---
## Quick Question

This question will ask about the following ROC curve:

{{< resource uuid="27296a79-a843-0f35-b099-68891f4d55bc" >}}

Given this ROC curve, which threshold would you pick if you wanted to correctly identify a small group of patients who are receiving the worst care with high confidence?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} t = 0.2 {{< /quiz_choice >}}     
{{< quiz_choice isCorrect="false" >}} t = 0.3 {{< /quiz_choice >}}     
{{< quiz_choice isCorrect="true" >}} t = 0.7 {{< /quiz_choice >}}     
{{< quiz_choice isCorrect="false" >}} t = 0.8 {{< /quiz_choice >}}{{< /quiz_choices >}}     
{{< quiz_solution >}}Explanation

The threshold 0.7 is best to identify a small group of patients who are receiving the worst care with high confidence, since at this threshold we make very few false positive mistakes, and identify about 35% of the true positives. The threshold t = 0.8 is not a good choice, since it makes about the same number of false positives, but only identifies 10% of the true positives. The thresholds 0.2 and 0.3 both identify more of the true positives, but they make more false positive mistakes, so our confidence decreases.

{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

Which threshold would you pick if you wanted to correctly identify half of the patients receiving poor care, while making as few errors as possible?

{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} t = 0.2 {{< /quiz_choice >}}     
{{< quiz_choice isCorrect="true" >}} t = 0.3 {{< /quiz_choice >}}     
{{< quiz_choice isCorrect="false" >}} t = 0.7 {{< /quiz_choice >}}     
{{< quiz_choice isCorrect="false" >}} t = 0.8 {{< /quiz_choice >}}{{< /quiz_choices >}}     
{{< quiz_solution >}}Explanation

The threshold 0.3 is the best choice in this scenerio. The threshold 0.2 also identifies over half of the patients receiving poor care, but it makes many more false positive mistakes. The thresholds 0.7 and 0.8 don't identify at least half of the patients receiving poor care.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "f6216265-1257-bdbe-4826-8a5e5b311096" "Back: Video 6: ROC Curves" %}}
- {{% resource_link "1e61720e-cc15-0a7b-0c5e-b3fe60c5ffa1" "Continue: Video 7: Interpreting the Model" %}}