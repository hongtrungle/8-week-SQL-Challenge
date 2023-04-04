# 🍜 Case Study #4 - Data Bank

- Case Study #4 Information: [Click Here!](https://8weeksqlchallenge.com/case-study-4/)

<img align="center" width="400" src="https://user-images.githubusercontent.com/81607668/130343294-a8dcceb7-b6c3-4006-8ad2-fab2f6905258.png">

## 📚 Table of Contents
  * [Introduction](#introduction)
  * [Problem Statement](#problem-statement)
  * [Entity Relationship Diagram](#entity-relationship-diagram)
  * [Example Datasets](#example-datasets)
 
## Introduction 
Data Bank runs just like any other digital bank - but it isn’t only for banking activities, they also have the world’s most secure distributed data storage platform!

Customers are allocated cloud data storage limits which are directly linked to how much money they have in their accounts. There are a few interesting caveats that go with this business model, and this is where the Data Bank team need your help!

The management team at Data Bank want to increase their total customer base - but also need some help tracking just how much data storage their customers will need.

## Entity Relationship Diagram 

<img align="center" width="500" src="https://user-images.githubusercontent.com/81607668/130343339-8c9ff915-c88c-4942-9175-9999da78542c.png">

## Example Datasets
### Table 1: Regions

This `regions` table contains the `region_id` and their respective `region_name` values

| region_id | region_name |
|-----------|-------------|
| 1         | Africa      |
| 2         | America     |
| 3         | Asia        |
| 4         | Europe      |
| 5         | Oceania     |



### Table 2: Customer Nodes

Customers are randomly distributed across the nodes according to their region - this also specifies exactly which node contains both their cash and data.

This random distribution changes frequently to reduce the risk of hackers getting into Data Bank’s system and stealing customer’s money and data!

| customer_id | region_id   | node_id | start_date | end_date |
|-------------|------------|---------|----------|---------|
| 1           | 3 | 4       | 2020-01-02 | 2020-01-03|
| 2           | 3 | 5       | 2020-01-03 | 2020-01-17|
| 3           | 5 | 4       | 2020-01-27|	2020-02-18|
| 4           | 5 | 4       |	2020-01-07|2020-01-19|
| 5           | 3 | 3       |2020-01-15| 2020-01-23|
| ...         | ...        | ...     | ... | ...|

### Table 3: Customer Transactions

This table stores all customer deposits, withdrawals and purchases made using their Data Bank debit card.

| customer_id | txn_date    | txn_type | txn_amount |
|-------------|-------------|----------|------------|
| 429         | 2020-01-21  | deposit  | 82         | 
| 155         | 2020-01-10  | deposit  | 712        |
| 398         | 20210-01-01 | deposit  | 196        |
| 255         | 2020-01-14  | deposit  | 563        |
| 185         | 2020-01-29  | deposit  | 626        |
| ...         | ...         | ...      | ...        |