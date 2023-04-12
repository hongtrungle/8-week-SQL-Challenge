# 🍜 Case Study #7 - Balanced Tree Clothing Co.

- Case Study #7 Information: [Click Here!](https://8weeksqlchallenge.com/case-study-7/)

<img align="center" width="400" src="https://8weeksqlchallenge.com/images/case-study-designs/7.png">

## 📚 Table of Contents
  * [Introduction](#introduction)
  * [Example Datasets](#example-datasets)
 
## Introduction 
Balanced Tree Clothing Company prides themselves on providing an optimised range of clothing and lifestyle wear for the modern adventurer!

Danny, the CEO of this trendy fashion company has asked you to assist the team’s merchandising teams analyse their sales performance and generate a basic financial report to share with the wider business.

## Example Datasets
### Table 1: Product Details

`balanced_tree.product_details` includes all information about the entire range that Balanced Clothing sells in their store.

| product_id  | price   | product_name  | category_id   | segment_id | style_id | category_name | segment_name | style_name |
|--------|---------|-----|---------------|---------|---------|---------|--------|--------|
|c4a632|	13|	Navy Oversized Jeans - Womens| 	1            |	3|	7|	Womens|	Jeans|	Navy Oversized|
|e83aa3|    32|	Black Straight Jeans - Womens| 	1            |	3|	8|	Womens|	Jeans|	Black Straight|
|e31d39|	10|	Cream Relaxed Jeans - Womens| 	1            |	3|	9|	Womens|	Jeans|	Cream Relaxed|
|d5e9a6|	23|	Khaki Suit Jacket - Womens| 	1            |	4|	10|	Womens|	Jacket|	Khaki Suit|
|72f5d4|	19|	Indigo Rain Jacket - Womens| 	1            |	4|11|	Womens|	Jacket|	Indigo Rain|
| ...    | ...     | ... | ...           | ...| ...| ...| ...| ...|

### Table 2: Product Sales 

`balanced_tree.sales` contains product level information for all the transactions made for Balanced Tree including quantity, price, percentage discount, member status, a transaction ID and also the transaction timestamp.

| prod_id|	qty|	price|	discount|	member|	txn_id|	start_txn_time|
|----------|-----------|---------|--------|---------|---------|---------|
|c4a632|	4|	13|	17|	t|	54f307|	2021-02-13 01:59:43.296|
|5d267b|	4|	40|	17|	t|	54f307|	2021-02-13 01:59:43.296|
|b9a74d|	4|	17|	17|	t|	54f307|	2021-02-13 01:59:43.296|
|2feb6b|	2|	29|	17|	t|	54f307|	2021-02-13 01:59:43.296|
|c4a632|	5|	13|	21|	t|	26cc98|	2021-01-19 01:39:00.3456|
| ...      | ...       | ...     | ... | ...| ...| ...|

### Table: Product Hierarchy & Product Price

These tables are used only for the bonus question where we will use them to recreate the `balanced_tree.product_details` table.

`balanced_tree.product_hierarchy`

| id | parent | level_text | level_name | 
|-------|--------|------------|------------|
| 1     |        | Womens     | Category   |      
| 2     |        | Mens       | Category   |         
| 3     | 1      | Jeans      | Segment    |
| 4     | 1      | Jacket     | Segment    |
| 5     | 2      | Shirt        | Segment         |
| ...   | ...    | ...        | ...        |

`balanced_tree.product_prices`

| id             | product_id | price | 
|----------------|------------|-------|
| 7| 	c4a632    | 	13   |
| 8| 	e83aa3    | 	32   |
| 9| 	e31d39    | 	10   |
| 10| 	d5e9a6    | 	23   |
| 11| 	72f5d4    | 	19   |
| ...| ...| 	...  |
