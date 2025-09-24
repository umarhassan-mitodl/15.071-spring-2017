---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '8.2 Airline Revenue Management: An Introduction to Linear Optimization '
parent_type: CourseSection
parent_uid: 2900efa7-1aff-756d-feba-74c6d16f2d3d
title: '8.2 Airline Revenue Management: An Introduction to Linear Optimization'
uid: 866b08a8-38d4-f694-786a-619e9ebff44b
video_metadata:
  youtube_id: null
---
## Quick Question

In this quick question, we'll perform some sensitivity analysis on the connecting flights problem.

Previously, we said that American Airlines could market their fares to increase demand. It costs $200 in advertising to increase demand by one unit.

Is it worth it to market the discount fares from JFK to DFW?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} Yes. American Airlines should market the discount fares from JFK to DFW to increase demand by 50. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Yes. American Airlines should market the discount fares from JFK to DFW to increase demand by 10. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} No. American Airlines should not market the discount fares from JFK to DFW because even though the revenue increases, it does not exceed the costs. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} No. American Airlines should not market the discount fares from JFK to DFW because the revenue does not increase at all by increasing the demand for these tickets. {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

You can answer this question without re-solving the model by noticing that we are not meeting the demand for discount fares from JFK to DFW at all. The demand could increase by 100, and we still would not offer more than 11 discount fares.

Alternatively, you could change the demand for discount fares, and re-solve the model. The solution does not change, regardless of how much you increase the demand.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

Is it worth it to market the regular fares from JFK to LAX?

{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} Yes. American Airlines should market the regular fares from JFK to LAX to increase demand by 50. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} Yes. American Airlines should market the regular fares from JFK to LAX to increase demand by 10. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} No. American Airlines should not market the regular fares from JFK to LAX because even though the revenue increases, it does not exceed the costs. {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} No. American Airlines should not market the regular fares from JFK to LAX because the revenue does not increase at all by increasing the demand for these tickets. {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

In the current solution, we are meeting the demand for regular tickets from JFK to LAX. If we increase the demand by 10, we offer 10 more regular tickets, but our revenue only increases by $140, which does not exceed the cost of $2000. If we increase the demand by 50, to 130, we only offer 91 seats. Therefore, American Airlines should not market the regular fares from JFK to LAX because even though the revenue increases, it does not exceed the costs.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "80f150bc-38fd-0f84-75f7-ccfe876f7744" "Back: Video 7: Connecting Flights" %}}
- {{% resource_link "0cd767eb-f8c6-279f-86f2-16e785139b90" "Continue: Video 8: The Edge of Revenue Management" %}}