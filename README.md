# Coffee Shop Sales Dashboard

This was based on a project by Maven analytics. I adjusted the data to make it suitable to the British context.

The workflow was as follows:

1. Changed the data to make it more British sounding
	- used find and replace to replace US sounding items with British ones.
	- used SUM() and MROUND() to change the prices to British prices that always ended in £0.05

2. Calculate the revenue for each transaction
    - =SUM([@[transaction_qty]]*[@[unit_price]])

3. Create columns for months and days of the week
    - =MONTH([@[transaction_date]])
    - =TEXT([@[transaction_date]],"mmm")

    - =WEEKDAY([@[transaction_date]],2)
    - =TEXT([@Weekday],"ddd")

4. Create pivot tables for the following:
    - Revenue by month
    - Revenue by Day of week
    - Reveue by hour of day
    - Revenue by product category
    - Top ten selling product types

5. Create visualisations to show data and patterns 
