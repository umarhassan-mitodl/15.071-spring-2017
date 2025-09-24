---
content_type: page
description: Even' Star Organic Farm
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: 8 Linear Optimization
parent_type: CourseSection
parent_uid: daafaa58-867c-9765-f1c4-c60a9c0ed426
title: 8.5 Assignment 8
uid: 6a5d4bdb-70f4-48f5-8697-82dbaa8537a8
video_metadata:
  youtube_id: null
---
## Even' Star Organic Farm

Even' Star Organic Farm was founded in 1997 by Brett Grohsgal, a former chef in Washington DC. The company owns a 104-acre farm in southern Maryland, and grows and sells organic produce. For more information, see {{% resource_link "9faa7564-b14a-4fb4-821b-55481c2963e0" "Even' Star's Facebook page" %}}. This problem describes the business issues faced by Brett, and the data is based on actual observations.

Brett has decided to grow eight different types of produce: large tomatoes, small tomatoes, watermelon, okra, basil, cucumbers, sweet potatoes, and winter squash. He distributes his produce through three different channels: Restaurants, Community-Supported Agriculture, and Farmers' Markets. 

Initially, he sold exclusively to restuarants. He knows of 20 restaurants that will buy his produce from his connections as a former chef. As his farm expanded, he also started selling his produce at a local farmers' market, where he can command a higher price. Recently, he has also started selling through Community Supported Agriculture (CSA), a program in which individuals pay a $400 subscription price to get a box of produce each week for 15 weeks. He currently knows of 90 individuals who are interested in buying his produce through the CSA program. 

Brett has a limited amount of produce that he can sell each season, and he needs to decide how much produce to sell through each channel (restaurants, CSA, or farmers' markets). 

## Problem 1.1 - Formulating the Problem

Let's formulate Brett's problem as a linear optimization problem. The spreadsheet {{% resource_link "76d937c2-e04a-d2de-53f9-c971328b5f0e" "EvenStarFarm (ODS)" %}} for LibreOffice or OpenOffice, and {{% resource_link "0dfaed12-f92d-5469-6c28-596520d801a4" "EvenStarFarm (XLSX)" %}} for Microsoft Excel, contains the data for the problem, and has set up the decision variables and objective for you.

The **decision variables** in our problem are the number of cases of each type of produce to sell in each channel (there are 24 decision variables). They are highlighted in yellow in the spreadsheet.

Brett's **objective** is to maximize total profit (total revenue minus total cost). In the spreadsheet EvenStarFarm, the objective is highlighted in blue.

To compute the total revenue, we multiply the number of cases of each type of produce distributed in each channel by the price that Brett sells it for. The price of a case of each type of produce in each of the different channels is listed in cells C6:E13 of the spreadsheet.

The total cost is composed of two parts: a variable cost per client, and an entry cost for being in the particular channel. The entry costs are listed in cells B20:D20.

To compute the total variable cost for each restaurant client, we use the information that each restaurant client will buy 119 cases of produce during the season. So, the total number of restaurant clients served in a season can be computed as the total number of cases sold to restaurants, divided by 119. (Note that the number of restuarant clients Brett gives produce to could be fractional (like 16.57). This is a simplification we'll make for this problem, so please ignore the fact that this number should be integer. We'll see next week how you can add integer restrictions to an optimization model.)

To compute the total variable cost for CSA clients, we need to know that each CSA customer will buy $400 worth of produce during the season. So, the total number of CSA clients served can be computed by dividing the total dollar amount sent to CSA customers by $400. (Note that the number of CSA clients Brett gives produce to could be fractional (like 16.57). This is a simplification we'll make for this problem, so please ignore the fact that this number should be integer. We'll see next week how you can add integer restrictions to an optimization model.)

There is no variable cost for farmers' market clients.

Which of the following spreadsheet formulas computes the total variable cost for the restaurant channel? Use the location of the data and variables in the spreadsheet EvenStarFarm.

 B19*SUM(B26:B33)*

*B19/119*

*B19*(SUM(B26:B33)/119) 

 SUM(B26:B33)/119 

## *Problem 1.2 - Formulating the Problem*

*Which of the following spreadsheet formulas computes the total variable cost for the CSA channel? Use the location of the data and variables in the spreadsheet EvenStarFarm.*

*C19*(SUMPRODUCT(C26:C33;D6:D13)/400) 

 SUMPRODUCT(C26:C33;D6:D13)/400 

 C19*SUMPRODUCT(C26:C33;D6:D13)*

*C19/400*

## Problem 1.3 - Formulating the Problem

Now, let's formulate the constraints for our model. Brett can't sell negative cases, and he can't sell more cases than he produces. Cells B6:B13 in the spreadsheet list the number of available cases of each type of produce. For large tomatoes, which of the following constraints should we add to our model to capture these restrictions? Select all that apply.

 B26:D26 (\\geq) 0 

 B26:D26 (\\leq) 0 

 B26:D26 (=) 0 

 SUM(B26:D26) (\\geq) B6 

 SUM(B26:D26) (\\leq) B6 

 SUM(B26:D26) (=) B6 

## Problem 1.4 - Formulating the Problem

Due to the truck capacity, the number of cases sold at the farmers' market can't be more than 600. Which constraint(s) captures this restriction?

 D26:D33 = 600 

 SUM(D26:D33) = 600 

 D26:D33 (\\leq) 600 

 SUM(D26:D33) (\\leq) 600 

## Problem 1.5 - Formulating the Problem

Brett knows that at most 20 restaurants will buy his produce. Which constraint(s) captures this restriction? HINT: Each restaurant buys 119 cases.

 SUM(B26:B33)/119 (\\leq) 20 

 SUM(B26:B33)/119 = 20 

 B26:B33/119 (\\leq) 20 

 B26:B33/119 = 20 

## Problem 1.6 - Formulating the Problem

Brett knows that at most 90 CSA customers will buy his produce. Which constraint(s) captures this restriction? HINT: Each CSA customer buys $400 worth of produce.

 SUM(C26:C33;D6:D13)/400 (\\leq) 90 

 SUMPRODUCT(C26:C33;D6:D13)/400 (\\leq) 90 

 SUM(C26:C33)/400 (\\leq) 90 

We first need to compute the total number of CSA clients. We saw while computing the objective that this is SUMPRODUCT(C26:C33;D6:D13)/400. This should be less than or equal to 90.

Add all of these constraints to your model in LibreOffice (or in the spreadsheet software you are using). Here is a list of all of the constraints you should be adding:

1) Brett can't sell negative cases, and he can't sell more cases than he produces, for each type of produce.

2) The number of cases sold at the farmer's market can't be more than 600.

3) Brett can't sell produce to more than 20 restaurants.

4) Brett can't sell produce to more than 90 CSA customers.

## Problem 2.1 - Solving the Model

Solve your model, and answer the following questions about the solution:

What is the objective function value (in dollars)?

## Problem 2.2 - Solving the Model

How many cases of large tomatoes are given to CSA customers?

## Problem 2.3 - Solving the Model

How many cases of watermelon are given to farmers' market customers?

## Problem 2.4 - Solving the Model

How many CSA customers does Brett provide produce for? Remember that this might be fractional - go ahead and enter the exact number even though Brett can't really serve "fractional customers".

## Problem 3.1 - Sensitivity Analysis

Suppose that Brett can pay $1,000 to trade in his truck for a larger truck. This would allow him to transport 200 more cases of produce to the farmers' market (for a total of 800 cases). Should he do it? HINT: Adjust the constraints in your model, re-solve it, and compare the increase in objective function value to the cost of buying the larger truck.

## Problem 3.2 - Sensitivity Analysis

One of Brett's workers has offered to use his truck to help Brett transport 200 more cases of produce to the farmer's market (for a total of 800 cases). Which of the following choices would increase Brett's profit? Select all that apply.Exercise 12

 Hire the worker, and pay him $300 for helping. 

 Hire the worker, and pay him $150 for helping. 

 Not hiring the worker. 

## Problem 3.3 - Sensitivity Analysis

Now suppose that Brett has found 10 more customers who would like to join the CSA program, for a total of 100 potential CSA customers. Should he sell produce to these customers? If you have changed any values in the constraints, change them back to their original values before answering this question (600 cases at the farmers' market).

 Yes, adding all of these extra customers will increase his profit. 

 Yes, adding some of these extra customers will increase his profit. 

 No, he shouldn't sell produce to any of these customers. 

## Problem 3.4 - Sensitivity Analysis

Now suppose that Brett has purchased 5 additional acres of land, which allows him to produce 10 additional cases of one of his vegetables. Which vegetable should he plant on these 5 additional acres?

If you have changed any values in the constraints, change them back to their original values before answering this question (600 cases at the farmers' market, and 90 potential CSA customers). Assume for this problem that the production cost is the same for all types of produce. For your reference, here is a list of the number of cases of each type of produce that Brett currently produces: 406 cases of Large Tomatoes, 608 cases of Small Tomatoes, 167 cases of Watermelon, 76 cases of Okra, 72 cases of Basil, 251 cases of Cucumbers, 107 cases of Sweet Potatoes, and 133 cases of Winter Squash.

 Tomatoes (large) 

 Tomatoes (small) 

 Watermelon 

 Okra 

 Basil 

 Cucumber 

 Sweet Potatoes 

 Winter Squash 

Acknowledgements: This problem is based on the case study *Introducing Integer Modeling with Excel Solver* by Dessislava Pachamanova, INFORMS Transactions on Education 7:1(88-98). Publication year 2006.

{{% resource_link "3083aeae-6367-2e76-61a3-34ffc021896d" "Back: Video 8: Extensions and the Edge" %}}