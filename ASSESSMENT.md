## Instructions
Complete the two sections below. Submit the answers as a pull request or email a patch file.

## MySQL
Answer the following questions in the space provided.

#### Example Question:
Example. Select all data from the fruit table.
```sql
// select statement
SELECT * FROM fruit;
```

#### Question 1:
Which fruit sold more units, apples or oranges?
```sql
For Apples: select sum(quantity) from sales where fkfruit_id IN(1,2,3,4,5) order by quantity ASC;
For Oranges: select sum(quantity) from sales where fkfruit_id IN(6,7,8) order by quantity ASC;
```

#### Question 2:
Select the varieties of apples costing at least $2.00.
```sql
SELECT variety from fruit WHERE cost <= 2.00 and fruit_id in(1,2,3,4,5);

```

#### Question 3:
Make a sales report listing store ID, store name, and total money from sales. Order stores from most money to least.
```sql

```

#### Question 4:
Update the price of mandarin oranges from $1.99 to $2.25.
```sql
UPDATE fruit SET cost = 2.25 where fruit_id = 8;
```

#### Question 5:
Insert a new type of fruit: a cameo apple costing $1.75
```sql
INSERT INTO fruit ( type, variety, cost) VALUES ('apple', 'cameo', 1.74);
```

#### Question 6:
Identify the fruits that have sold less than 20 units.
```sql

```

#### Question 7:
Add a new decimal column to the sales table called *discount* that does not allow NULL values and set the default value to 0.00.
```sql
ALTER TABLE `sales` ADD `discount` DECIMAL NOT NULL DEFAULT '0.00' ;

```

#### Question 8:
Update the values for the *discount* field with random values between 0 and 1.
```sql
ALTER TABLE `sales` CHANGE `discount` `discount` DECIMAL(1,0) NOT NULL DEFAULT'0';
```

## PHP
Using the code supplied, solve the two problems below.

#### Problem 1:
The Store view page is displaying an error. Fix it.

#### Problem 2:
Update the site to support the new *discount* column rate.
You should be able to save a sale with a discount.
A discount is applied per item. To get the total sale, subtract the discount from the cost and multiply it by the quantity.
