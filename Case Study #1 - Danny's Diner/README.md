# 🍜 Case Study #1 - Danny's Diner

- Case Study #1 Information: [Click Here!](https://8weeksqlchallenge.com/case-study-1/)

<img align="center" width="400" src="https://user-images.githubusercontent.com/94410139/158028436-eba944af-bdcc-459f-9c2f-fbd868c6c0c1.png">

## 📚 Table of Contents
  * [Introduction](#introduction)
  * [Problem Statement](#problem-statement)
  * [Entity Relationship Diagram](#entity-relationship-diagram)
  * [Example Datasets](#example-datasets)
 
## Introduction 
Danny seriously loves Japanese food so in the beginning of 2021, he decides to embark upon a risky venture and opens up a cute little restaurant that sells his 3 favourite foods: sushi, curry and ramen.

Danny’s Diner is in need of your assistance to help the restaurant stay afloat - the restaurant has captured some very basic data from their few months of operation but have no idea how to use their data to help them run the business.

## Problem Statement 
Danny wants to use the data to answer a few simple questions about his customers, especially about their visiting patterns, how much money they’ve spent and also which menu items are their favourite. Having this deeper connection with his customers will help him deliver a better and more personalised experience for his loyal customers.

He plans on using these insights to help him decide whether he should expand the existing customer loyalty program - additionally he needs help to generate some basic datasets so his team can easily inspect the data without needing to use SQL.

Danny has shared with you 3 key datasets for this case study:

- sales
- menu
- members

## Entity Relationship Diagram 

<img align="center" width="500" src="https://user-images.githubusercontent.com/94410139/158030281-2ea04216-34dd-41a3-adb6-f6df1cfb4c1a.png">

## Example Datasets
**Table 1: sales**

The `sales` table captures all `customer_id` level purchases with an corresponding `order_date` and `product_id` information for when and what menu items were ordered.

| customer_id | order_date  | product_id |
|-------------|-------------|------------|
| A           | 2021-01-01  | 1          |
| A           | 2021-01-01  | 2          |
| A           | 2021-01-07  | 2          |
| A           | 2021-01-10  | 3          |
| A           | 2021-01-11  | 3          |
| ...         | ...         | ...          |

**Table 2: menu**

The `menu` table maps the `product_id` to the actual `product_name` and `price` of each menu item.

| product_id | product_name | price |
|------------|--------------|-------|
| 1          | sushi        | 10    |
| 2          | curry        | 15    |
| 3          | ramen          | 12    |

**Table 3: members**

The final `members` table captures the `join_date` when a `customer_id` joined the beta version of the Danny’s Diner loyalty program.

| customer_id | join_date  |
|-------------|------------|
| A           | 2021-01-07 |
| B           | 2021-01-09 |