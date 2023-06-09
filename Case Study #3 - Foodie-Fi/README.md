# 🍜 Case Study #3 - Foodie-Fi

- Case Study #3 Information: [Click Here!](https://8weeksqlchallenge.com/case-study-3/)

<img align="center" width="400" src="https://user-images.githubusercontent.com/94410139/160449485-68336255-3f3e-45af-94eb-388a3f9af974.png">

## 📚 Table of Contents
  * [Introduction](#introduction)
  * [Entity Relationship Diagram](#entity-relationship-diagram)
  * [Example Datasets](#example-datasets)
 
## Introduction 
Subscription based businesses are super popular and Danny realised that there was a large gap in the market - he wanted to create a new streaming service that only had food related content - something like Netflix but with only cooking shows!

Danny finds a few smart friends to launch his new startup Foodie-Fi in 2020 and started selling monthly and annual subscriptions, giving their customers unlimited on-demand access to exclusive food videos from around the world!

Danny created Foodie-Fi with a data driven mindset and wanted to ensure all future investment decisions and new features were decided using data. This case study focuses on using subscription style digital data to answer important business questions.

## Entity Relationship Diagram 

<img align="center" width="500" src="https://user-images.githubusercontent.com/94410139/160449786-4e908a9c-85ee-40de-9f46-c650abd1b351.png">

## Example Datasets
### Table 1: plans

Customers can choose which plans to join Foodie-Fi when they first sign up.

Basic plan customers have limited access and can only stream their videos and is only available monthly at $9.90

Pro plan customers have no watch time limits and are able to download videos for offline viewing. Pro plans start at $19.90 a month or $199 for an annual subscription.

Customers can sign up to an initial 7 day free trial will automatically continue with the pro monthly subscription plan unless they cancel, downgrade to basic or upgrade to an annual pro plan at any point during the trial.

When customers cancel their Foodie-Fi service - they will have a churn plan record with a null price but their plan will continue until the end of the billing period.

| plan_id | plan_name | price |    
|---------|-------------------|--------|
| 0       | trial        | 0|
| 1       | basic monthly        |  9.90|   
| 2       | pro monthly        |  19.90|   
| 3       | pro annual        |     199|
| 4       | churn        |     null|


### Table 2: subscriptions

Customer subscriptions show the exact date where their specific `plan_id` starts.

If customers downgrade from a pro plan or cancel their subscription - the higher plan will remain in place until the period is over - the `start_date` in the `subscriptions` table will reflect the date that the actual plan changes.

When customers upgrade their account from a basic plan to a pro or annual pro plan - the higher plan will take effect straightaway.

When customers churn - they will keep their access until the end of their current billing period but the `start_date` will be technically the day they decided to cancel their service.

| customer_id | plan_id | start_date  |
|-------------|---------|-------------|
| 1           | 0     | 2020-08-01  |
| 1           | 1     | 2020-08-08  |
| 2           | 0     | 2020-09-20  |
| 2           | 3     | 2020-09-27  |
| 11           | 0     | 2020-11-19  |
| ...         | ...     | ...         | 

