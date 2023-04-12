# 🍜 Case Study #5 - Data Mart

- Case Study #5 Information: [Click Here!](https://8weeksqlchallenge.com/case-study-5/)

<img align="center" width="400" src="https://8weeksqlchallenge.com/images/case-study-designs/5.png">

## 📚 Table of Contents
  * [Introduction](#introduction)
  * [Entity Relationship Diagram](#entity-relationship-diagram)
  * [Column Dictionary](#column-dictionary)
  * [Example Rows](#example-rows)

 
## Introduction 
In June 2020 - large scale supply changes were made at Data Mart. All Data Mart products now use sustainable packaging methods in every single step from the farm all the way to the customer.

Danny needs your help to quantify the impact of this change on the sales performance for Data Mart and it’s separate business areas.

The key business question he wants you to help him answer are the following:

- What was the quantifiable impact of the changes introduced in June 2020?
- Which platform, region, segment and customer types were the most impacted by this change?
- What can we do about future introduction of similar sustainability updates to the business to minimise impact on sales?

## Entity Relationship Diagram 

<img align="center" width="500" src="https://8weeksqlchallenge.com/images/case-study-5-erd.png">

## Column Dictionary 

1. Data Mart has international operations using a multi-`region` strategy
2. Data Mart has both, a retail and online `platform` in the form of a Shopify store front to serve their customers
3. Customer `segment` and `customer_type` data relates to personal age and demographics information that is shared with Data Mart
4. `transactions` is the count of unique purchases made through Data Mart and `sales` is the actual dollar amount of purchases

Each record in the dataset is related to a specific aggregated slice of the underlying sales data rolled up into a `week_date` value which represents the start of the sales week.

## Example Rows

10 random rows are shown in the table output below from `data_mart.weekly_sales`:

| week_date | region   | platform  | segment | customer_type | transactions | sales |
|------|----------|-----------|----------|---------|------|-------|
| 9/9/20    | OCEANIA | Shopify   | C3 | New| 610 | 110033.89|
| 29/7/20    | AFRICA | Retail    | C1 | New | 110692 | 3053771.19|
| 22/7/20    | EUROPE | Shopify   | C4 | Existing	| 24 | 8101.54|
| 13/5/20    | AFRICA | Shopify   | null | Guest	| 5287 | 1003301.37|
| 24/7/19    | ASIA | Retail    | C1 | New | 127342 | 3151780.41|
| ...  | ...      | ...       | ... | ...| ...| ...|
