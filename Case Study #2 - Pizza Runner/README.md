# 🍜 Case Study #2 - Pizza Runner

- Case Study #2 Information: [Click Here!](https://8weeksqlchallenge.com/case-study-2/)

<img align="center" width="400" src="https://user-images.githubusercontent.com/94410139/158215978-83465a74-7ccf-457a-8770-f1bdaa0b5343.png">

## 📚 Table of Contents
  * [Introduction](#introduction)
  * [Entity Relationship Diagram](#entity-relationship-diagram)
  * [Example Datasets](#example-datasets)
 
## Introduction 
Danny was scrolling through his Instagram feed when something really caught his eye - “80s Retro Styling and Pizza Is The Future!”

Danny was sold on the idea, but he knew that pizza alone was not going to help him get seed funding to expand his new Pizza Empire - so he had one more genius idea to combine with it - he was going to Uberize it - and so Pizza Runner was launched!

Danny started by recruiting “runners” to deliver fresh pizza from Pizza Runner Headquarters (otherwise known as Danny’s house) and also maxed out his credit card to pay freelance developers to build a mobile app to accept orders from customers.

## Entity Relationship Diagram 

<img align="center" width="500" src="https://user-images.githubusercontent.com/94410139/158216376-6b51187b-95ec-48f0-9c58-e912d9f1b035.png">

## Example Datasets
### Table 1: runners

The `runners` table shows the `registration_date` for each new runner

| runner_id | registration_date |    
|-----------|-------------------|
| 1         | 2021-01-01        |
| 2         | 2021-01-03        |     
| 3         | 2021-01-08        |     
| 4         | 2021-01-15        |     


### Table 2: customer_orders

Customer pizza orders are captured in the `customer_orders` table with 1 row for each individual pizza that is part of the order.

The `pizza_id` relates to the type of pizza which was ordered whilst the `exclusions` are the `ingredient_id` values which should be removed from the pizza and the `extras` are the `ingredient_id` values which need to be added to the pizza.

Note that customers can order multiple pizzas in a single order with varying `exclusions` and `extras` values even if the pizza is the same type!

The `exclusions` and `extras` columns will need to be cleaned up before using them in your queries.

| order_id | customer_id | pizza_id |exclusions | extras | order_time             |
|----------|-------------|----------|----------|--------|------------------------|
| 1        | 101         | 1        |          |        | 2021-01-01 18:05:02    |
| 2        | 101         | 1        |           |        | 2021-01-01 19:00:52    |
| 3        | 102         | 1        |           |        | 2021-01-02 23:51:23    |
| 3        | 102         | 2        |           | NaN    | 2021-01-02 23:51:23    |
| 4        | 103         | 1        | 4         |        | 2021-01-04 13:23:46    |
| ...      | ...         | ...      | ... | ... | ...                    |

### Table 3: runner_orders

After each orders are received through the system - they are assigned to a runner - however not all orders are fully completed and can be cancelled by the restaurant or the customer.

The pickup_time is the timestamp at which the runner arrives at the Pizza Runner headquarters to pick up the freshly cooked pizzas. The distance and duration fields are related to how far and long the runner had to travel to deliver the order to the respective customer.

| order_id | runner_id | pickup_time | distance | duration   | cancellation |
|----------|-----------|------------------|----------|------------|--------------|
| 1        | 1       | 2021-01-01 18:15:34   | 20km     | 32 minutes |              |
| 2        | 1       | 2021-01-01 19:10:54   | 20km     | 27 minutes |              |
| 3        | 1       | 2021-01-03 00:12:37   | 13.4km   | 20 mín     | NaN          |
| 4        | 2       | 2021-01-04 13:53:03   | 23.4     | 40         | NaN          |
| 5        | 3       | 2021-01-08 21:10:57   | 10       | 15         | NaN          |
| ...      | ...       | ... | ...      | ...        | ...          |


### Table 4: pizza_name

At the moment - Pizza Runner only has 2 pizzas available the Meat Lovers or Vegetarian!

|pizza_id|pizza_name|
|--------|-----------|
| 1     | Meat Lovers |
| 2     | Vegetarian |

### Table 5: pizza_recipes

Each `pizza_id` has a standard set of `toppings` which are used as part of the pizza recipe.

|pizza_id| toppings                  |
|--------|---------------------------|
| 1     | 1, 2, 3, 4, 5, 6, 8, 10   |
| 2     | 4, 6, 7, 9, 11, 12        |

### Table 6: pizza_toppings

This table contains all of the `topping_name` values with their corresponding `topping_id`value

| topping_id | topping_name |
|------------|--------------|
| 1          | Bacon        |
| 2          | BBQ Sauce    |
| 3          | Beef         |
| 4          | Cheese       |
| 5          | Chicken      |
| ...        | ...          |

