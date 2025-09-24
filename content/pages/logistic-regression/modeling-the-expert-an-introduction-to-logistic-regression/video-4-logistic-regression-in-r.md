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
uid: 8fc17cbb-03cd-ce23-b588-0c21e7dc33e8
video_metadata:
  youtube_id: null
---
## Video 4: Logistic Regression in R

In this video, we'll be using the dataset {{% resource_link "6343d35a-6e78-1756-0160-a4ea9dc9bd2e" "quality (CSV)" %}} to build a logistic regression model in R. Please download this file to follow along.

An R script file with all of the commands used in this lecture can be downloaded here: {{% resource_link "b6bc9877-49db-0911-1285-d5a2a287e733" "Unit3_ModelingExpert (R)" %}}.

{{< resource uuid="d56beae6-5d3e-cccc-adba-697fc8c6288b" >}}

The variables in the dataset quality.csv are as follows:

- **MemberID** numbers the patients from 1 to 131, and is just an identifying number.
- **InpatientDays** is the number of inpatient visits, or number of days the person spent in the hospital.
- **ERVisits** is the number of times the patient visited the emergency room.
- **OfficeVisits** is the number of times the patient visited any doctor's office.
- **Narcotics** is the number of prescriptions the patient had for narcotics.
- **DaysSinceLastERVisit** is the number of days between the patient's last emergency room visit and the end of the study period (set to the length of the study period if they never visited the ER). 
- **Pain** is the number of visits for which the patient complained about pain.
- **TotalVisits** is the total number of times the patient visited any healthcare provider.
- **ProviderCount** is the number of providers that served the patient.
- **MedicalClaims** is the number of days on which the patient had a medical claim.
- **ClaimLines** is the total number of medical claims.
- **StartedOnCombination** is whether or not the patient was started on a combination of drugs to treat their diabetes (TRUE or FALSE).
- **AcuteDrugGapSmall** is the fraction of acute drugs that were refilled quickly after the prescription ran out.
- **PoorCare** is the outcome or dependent variable, and is equal to 1 if the patient had poor care, and equal to 0 if the patient had good care.

In this video we learned how to use the sample.split() function from the caTools package to split data for a classification problem, balancing the positive and negative observations in the training and testing sets.

If you wanted to instead split a data frame *data,* where the dependent variable is a continuous outcome (this was the case for all the datasets we used last week), you could instead use the sample() function. Here is how to select 70% of observations for the training set (called "train") and 30% of observations for the testing set (called "test"):

`spl = sample(1:nrow(data), size=0.7 * nrow(data))`

`train = data[spl,]`

`test = data[-spl,]`

- {{% resource_link "9cb7a258-ad19-0f7f-84e5-89aad47092b1" "Back: Quick Question" %}}
- {{% resource_link "8c080206-9993-5e2b-b0c5-0c4cd73fd74c" "Continue: Quick Question" %}}