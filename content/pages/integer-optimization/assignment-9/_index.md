---
content_type: page
description: Even' Star Organic Farm Revisited
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: 9 Integer Optimization
parent_type: CourseSection
parent_uid: db42b40a-d705-f431-a7e2-3a1d11cec341
title: 9.5 Assignment 9
uid: 2dbce7a6-bb37-17df-55b4-be0179616ad6
video_metadata:
  youtube_id: null
---
## Even' Star Organic Farm Revisited

Last week in the "Even' Star Organic Farm" optional homework problem, we formulated and solved the problem faced by Brett Grohsgal, the founder of the organic farm in southern Maryland. This week, we'll use integer optimization to improve the formulation and model some new decisions faced by Brett. We'll be using the spreadsheet {{% resource_link "6cd223a1-4aec-5eb0-c21e-45ff237283bb" "EvenStarFarmRevisited (ODS)" %}} for LibreOffice or OpenOffice, and {{% resource_link "040348f2-170d-8719-fb18-74e9a3e484ce" "EvenStarFarmRevisited (XLSX)" %}} for Microsoft Excel.

## Problem 1.1 - Adjusting the Formulation

Last week, we saw that Brett has to pay an entry fee for each channel that he participates in. He could instead choose to not participate in a certain channel, and therefore not have to pay the entry fee. This week, we'll model this choice using binary variables to see if we can increase Brett's profit.

Add three new decision variables to your model: one for whether or not Brett participates in the restaurant channel, one for whether or not he participates in the farmers' market channel, and one for whether or not he participates in the CSA channel. (HINT: It will be easy to input your model into Solver if you add these decision variables in the row right below the current decision variable table.)

If Brett chooses not to participate in a channel, two things need to change in our model: (1) he does not have to pay the fixed cost to enter that channel, and (2) he can't sell any cases in that channel.

To remove the fixed cost, take a look at the objective function equation. You should see three terms each subtracting the fixed cost value from the total profit for one of the channels. Multiply each of these terms by the corresponding binary variable you just defined for that channel. Now, if the binary variable is equal to 1, Brett pays the fixed cost, but if the binary variable is equal to 0, Brett does not pay the fixed cost.

Set the value of each of your binary variables equal to 1 (Brett participates in all channels). You should see that the objective value is the same as our best objective value without the binary variables ($49,956.39).

Now, we need to add constraints to make sure that if Brett does not enter a channel (doesn't pay the entry cost), then he also does not sell any cases in this channel. And if he does enter a channel, then he can sell as many cases as he wants in that channel. We'll model this with a special type of logical constraint.

We know that Brett can’t sell more cases than he produced. What is the total number of cases Brett produced?

## *Problem 1.2 - Adjusting the Formulation*

*In the optimal solution, which channels does Brett enter? Select all that apply.*

 *Restaurants* 

 *CSA* 

 *Farmers' Market* 

## Problem 1.3 - Adjusting the Formulation

How much extra profit does he gain now compared to before, when he was always entering all of the channels?

## Problem 1.4 - Adjusting the Formulation

How many total cases of produce does Brett sell in the restaurant channel?

## Problem 2.1 - Sensitivity Analysis

To maximize his profit, we saw in the optimal solution that Brett should not enter the Farmers' Market channel. However, Brett feels that having a booth at the farmers' market increases his visibility in the community, and is important to his business. Which of the following actions could he take to try to make the farmers' market channel more profitable so that it is worth re-entering? Select all that apply.

 He could increase his prices. 

 He could reduce the entry cost. 

 He could reduce the variable costs. 

 He could buy a bigger truck to increase the number of cases he can sell. 

## Problem 2.2 - Sensitivity Analysis

In LibreOffice, which of the following adjustments makes Brett enter the farmers' market channel in the optimal solution? Select all that apply.

 Increasing his prices at the farmers' market by 10% 

 Increasing his prices at the farmers' market by 25% 

 Reducing his entry cost to $5,000.00 

 Reducing his entry cost to $3,000.00 

## Problem 2.3 - Sensitivity Analysis

Suppose that Brett finds it easier to increase his prices than to reduce his entry cost, so he decides to increase his prices in the farmers' market by 25%. Make this adjustment in LibreOffice, and re-solve the model (remember to change any other values back to their original values if you have adjusted them to answer any previous questions).

What is the objective value in the new solution?

## Problem 2.4 - Sensitivity Analysis

Which types of produce does he sell at the farmers' market? Select all that apply.

 Tomatoes (large) 

 Tomatoes (small) 

 Watermelon 

 Okra 

 Basil 

 Cucumbers 

 Sweet Potatoes 

 Winter Squash 

## Problem 2.5 - Sensitivity Analysis

Which channels does Brett enter now? Select all that apply.

 Restaurants 

 CSA 

 Farmers' Market 

## Problem 2.6 - Sensitivity Analysis

The decision variables for the number of cases can take fractional values. It seems impractical for Brett to sell a fractional number of cases of any produce at the farmers' market, and he would prefer to always sell an integer number of cases. Restrict the cases decision variables to be integer, and resolve the model. Does the objective value change?

Note that you might need to set the time limit in Solver for this problem. Remember that you can set the time limit by opening up the Solver, and then clicking on Options. If you are using Excel, you want to set "Max Time" to 100. If you are using OpenOffice or LibreOffice, you want to check that "Solving time limit" says 100. If not, click on it and hit "Edit". Change it to 100 and click Okay.

 Yes 

 No 

Acknowledgements: This problem is based on the case study *Introducing Integer Modeling with Excel Solver* by Dessislava Pachamanova, *INFORMS Transactions on Education* 7(1), p.88-98, 2006.

- {{% resource_link "6e8bdbce-3ea9-e644-0e2b-66d90a657d47" "Back: Video 4: The Solution" %}}
- {{% resource_link "1ab3f4de-f050-7a6b-6327-b8e7dfa4fb69" "Continue: Gerrymandering New Mexico" %}}