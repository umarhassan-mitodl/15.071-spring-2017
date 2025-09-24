---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '9.2 Sports Scheduling: An Introduction to Integer Optimization '
parent_type: CourseSection
parent_uid: fbf2b704-9246-466e-f247-36bff248b7c3
title: '9.2 Sports Scheduling: An Introduction to Integer Optimization'
uid: bc55ff56-182e-b4ef-aaab-2b01313266a2
video_metadata:
  youtube_id: null
---
## Quick Question

Suppose we want to add a constraint that teams A and B must play in week 4 (we want the last game to be a divisional one). Given the current model, which of the following constraints would model this correctly? Select all that apply.

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} \\(x\_{AB4} = 0\\) {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} \\(x\_{AB4} = 1\\) {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} \\(x\_{AB1} + x\_{AB2} + x\_{AB3} = 1\\) {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} \\(x\_{AB2} = 1\\) {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} \\(x\_{AB1} + x\_{AB2} = 1\\) {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

The second and third constraints would both model this correctly. We can either force the decision variable for week 4 to 1, or we can make sure that only one game is played in the earlier weeks.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "209100b3-8ec9-d10b-5925-656d460ca2ad" "Back: Video 4: Logical Constraints" %}}
- {{% resource_link "2da01ab4-3598-cf28-401d-952436b11f42" "Continue: Video 5: The Edge" %}}