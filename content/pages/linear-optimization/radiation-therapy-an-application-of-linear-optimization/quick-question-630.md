---
content_type: page
description: '8.3 Radiation Therapy: An Application of Linear Optimization

  '
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '8.3 Radiation Therapy: An Application of Linear Optimization '
parent_type: CourseSection
parent_uid: 7a59278a-134c-5085-244c-381fc6090890
title: '8.3 Radiation Therapy: An Application of Linear Optimization'
uid: 12e6da56-9931-1c83-7bce-67f78b499ef3
video_metadata:
  youtube_id: null
---
## Quick Question

In the next video, we'll be formulating the IMRT problem as a linear optimization problem. What do you think the decision variables in our problem will be?

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} The amount of radiation to deliver to the tumor {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} The intensities of the beams {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="true" >}} The intensities of the beamlets {{< /quiz_choice >}}   
{{< quiz_choice isCorrect="false" >}} The shape of the tumor {{< /quiz_choice >}}{{< /quiz_choices >}}   
{{< quiz_solution >}}Explanation

We get to decide the beamlet intensities - these will be the decision variables in our optimization problem. The amount of radiation to the tumor will be computed using the beamlet intensities, but we also want to make sure we know the amount of radiation to healthy tissue. The intensities of the beams would have been the decision variables in traditional radiation therapy, and the shape of the tumor is data.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

{{% resource_link "98a5789b-a203-1300-ac3e-513ddaf88866" "Continue: Video 2: An Optimization Problem" %}}