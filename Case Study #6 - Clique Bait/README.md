# 🍜 Case Study #6 - Clique Bait

- Case Study #6 Information: [Click Here!](https://8weeksqlchallenge.com/case-study-6/)

<img align="center" width="400" src="https://8weeksqlchallenge.com/images/case-study-designs/6.png">

## 📚 Table of Contents
  * [Introduction](#introduction)
  * [Entity Relationship Diagram](#entity-relationship-diagram)
  * [Example Datasets](#example-datasets)
 
## Introduction 
Clique Bait is not like your regular online seafood store - the founder and CEO Danny, was also a part of a digital data analytics team and wanted to expand his knowledge into the seafood industry!

In this case study - you are required to support Danny’s vision and analyse his dataset and come up with creative solutions to calculate funnel fallout rates for the Clique Bait online store.

## Entity Relationship Diagram 
This entity relationship diagram is created through dbdiagram.io

<img align="center" width="500" src="https://user-images.githubusercontent.com/95112831/229834315-fe7110b3-cd06-465c-9df9-9ca91bc3317c.png">

## Example Datasets
### Table 1: Users 

Customers who visit the Clique Bait website are tagged via their `cookie_id`.

| user_id | cookie_id   | start_date | 
|---------|-------------|-----------|
| 397     | 3759ff      | 2020-03-30 00:00:00 |
| 215     | 863329      | 2020-01-26 00:00:00 |
| 191     | eefca9      | 2020-03-15 00:00:00 |
| 89     | 764796      | 2020-01-07 00:00:00 |
| 127     | 17ccc5      | 2020-01-22 00:00:00 |
|...| ...         |...|

### Table 2: Events

Customer visits are logged in this events table at a `cookie_id` level and the `event_type` and `page_id` values can be used to join onto relevant satellite tables to obtain further information about each event.

The `sequence_number` is used to order the events within each visit.

| visit_id | cookie_id | page_id | event_type | sequence_number | event_time |
|----------|-----------|---------|--------|---------|---------|
|719fd3|	3d83d3|	5|	1|	4|	2020-03-02 00:29:09.975502 |
|fb1eb1|	c5ff25|	5|	2|	8|	2020-01-22 07:59:16.761931 |
|23fe81|	1e8c2d|	10|	1|	9|	2020-03-21 13:14:11.745667 |
|ad91aa|	648115|	6|	1|	3|	2020-04-27 16:28:09.824606 |
|5576d7|	ac418c|	6|	1|	4|	2020-01-18 04:55:10.149236 |
| ...      | ...       | ...     | ... | ...|

### Table 3: Event Identifier

The `event_identifier` table shows the types of events which are captured by Clique Bait’s digital data systems.

| event_type | event_name      | 
|----------|-----------------|
| 1        | Page View       | 
| 2        | Add to Cart     |
| 3        | Purchase        |
| 4        | Ad Impression   |
| 5        | Ad Click        |

### Table 4: Campaign Identifier

This table shows information for the 3 campaigns that Clique Bait has ran on their website so far in 2020.

| campaign_id | products          | campaign_name | start_date | end_date |
|--------|-------------|---------|------------|---------|
|1|	1-3|	BOGOF - Fishing For Compliments|	2020-01-01 00:00:00|	2020-01-14 00:00:00|
|2|	4-5|	25% Off - Living The Lux Life|	2020-01-15 00:00:00|	2020-01-28 00:00:00|
|3|	6-8|	Half Off - Treat Your Shellf(ish)|	2020-02-01 00:00:00|	2020-03-31 00:00:00|

### Table 5: Page Hierarchy

This table lists all of the pages on the Clique Bait website which are tagged and have data passing through from user interaction events.

| page_id | page_name      | product_category | product_id |
|-------|----------------|----------|------------|
| 1     | Home Page      | null  | null |      
| 2     | All Products   | null  | null |         
| 3     | Salmon         | Fish  | 1        |
| 4     | Kingfish       | Fish  | 2        |
| 5     | Tuna           | Fish  | 3        |
| ...   | ...            | ...      | ...        |