---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '8.3 Radiation Therapy: An Application of Linear Optimization '
parent_type: CourseSection
parent_uid: 7a59278a-134c-5085-244c-381fc6090890
title: '8.3 Radiation Therapy: An Application of Linear Optimization'
uid: 2194bcb2-4c12-fa9a-11f3-457666bd1bee
video_metadata:
  youtube_id: null
---
## Quick Question

 

In your spreadsheet from Video 3, make sure that you have solved the original small example problem (change the spinal cord limit back to 5 and re-solve if you have changed it, and make sure the objective value is 22.75).

Now, change the weight for the spinal cord term in the objective to 5.

Without re-solving, what does the objective value of the current solution change to?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

The term SUMPRODUCT(B14:B19;F5:F10) in the objective (corresponding to Voxel 5) should now be 5\*SUMPRODUCT(B14:B19;F5:F10). This changes the objective value to 42.75.

Now re-solve the model. What does the objective change to?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

You can resolve the model by going to Solver, and just hitting Solve. The new optimal objective function value is 25.666667.

Notice how we are now giving a smaller dose to the spinal cord!

CheckShow Answer

 

- {{% resource_link "a10ced6c-1f0f-3ddc-aa30-efb14db63365" "Back: Video 5: Sensitivity Analysis" %}}
- {{% resource_link "eaf609cc-c68c-36a2-cb16-5b923543a1c7" "Continue: Video 6: The Analytics Edge" %}}