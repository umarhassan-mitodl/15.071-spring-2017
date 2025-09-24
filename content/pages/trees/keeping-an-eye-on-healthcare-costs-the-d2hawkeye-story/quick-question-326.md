---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '4.3 Keeping an Eye on Healthcare Costs: The D2Hawkeye Story '
parent_type: CourseSection
parent_uid: 52a221dd-c011-90a4-45b1-a393b15cb810
title: '4.3 Keeping an Eye on Healthcare Costs: The D2Hawkeye Story'
uid: c679795e-ed4f-1bd8-079e-7f008721cf38
video_metadata:
  youtube_id: null
---
## Quick Question

The image below shows the penalty error matrix that we discussed in the previous video.

{{< resource uuid="2d20a1e4-50f8-bd62-006b-f8e20477eb64" >}}

We can interpret this matrix as follows. Suppose the actual outcome for an observation is 3, and we predict 2. We find 3 on the top of the matrix, and go down to the second row (since we forecasted 2). The penalty error for this mistake is 2. If for another observation we predict (forecast) 4, but the actual outcome is 1, that is a penalty error of 3.

What is the worst mistake we can make, according to the penalty error matrix?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} We predict 5 (very high cost), but the actual outcome is 1 (very low cost). {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="true" >}} We predict 1 (very low cost), but the actual outcome is 5 (very high cost). {{< /quiz_choice >}}{{< /quiz_choices >}}   
{{< quiz_solution >}}Explanation

The highest cost is 8, which occurs when the forecast is 1 (very low cost), but the actual cost is 5 (very high cost). It would be much worse for us to ignore an actual high cost observation than to accidentally predict high cost for someone who turns out to be low cost

{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

What are the "best" types of mistakes we can make, according to the penalty error matrix?

{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="true" >}} Mistakes where we predict one cost bucket HIGHER than the actual outcome. {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} Mistakes where we predict one cost bucket LOWER than the actual outcome. {{< /quiz_choice >}}{{< /quiz_choices >}}   
{{< quiz_solution >}}Explanation

We are happier with mistakes where we predict one cost bucket higher than the actual outcome, since this just means we are being a little overly cautious.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "d35731b0-1c7f-7810-2382-bc22abd10118" "Back: Video 4: Error Measures" %}}
- {{% resource_link "41da33e5-8a10-b265-e28e-4f6bd320913a" "Continue: Video 5: CART to Predict Cost" %}}