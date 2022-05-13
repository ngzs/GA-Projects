# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Capstone Project: Instacart Recommender: Recommendation for groceries


### Description

As part of a team of data analysts at Instacart, a grocery delivery and pick-up service in the US and Canada, we would like to recommend which products will be in a user’s next order, based on their prior orders.

6 datasets
Aisles.csv: Type of food (fresh pasta, prepared soups etc.)
Department.csv: Broad categories they are in (frozen food, bakes etc.)
Product.csv: Contains all the products, with names and associated aisle and department
Prior.csv: All prior orders, on individual item level
Train.csv: Most recent order, on individual item level
Orders.csv: All orders, but on order level (have to match to prior or train)

Due to high number of re-ordered products, we will explore recommending all the items that users previously bought back to them to set a baseline.

The improved model will include only recommending the top 50% of their bought items.

Finally, we will use collaborative filtering, user-based, to find the next closest user. Ideally, we will find the difference between their list and recommend them in case it affects our F1-score, which is used to assess our space-delimited list against Kaggles. However due to technical difficulties that was not acheived.



---

### Analysis

a) Base model performance: 0.12631

b) 50% top purchases performance: 0.11949

c) Collaborative filtering performance: 0.12834

F1 score is a combination of not just hitting the right predictions, but also not recommending excessively (false positives). This resulted in model b performing well too.

Narrowing down recommendations, even if there might be fewer true positives, can still produce a good F1 score
There is evidence that the target might purchase related items – can fine-tune user-based collaborative filtering more.


---

## Conclusions / Next Steps:

- More can be done to utilise more EDA features
e.g. Add organic products or bananas to every list (low-hanging fruits) as initial models
- Use average of the number of items they ordered previously as a way to decide how many to include 
- Use weightage to diminish value of products for those further in time 
- Items that are placed in the cart first to have higher weightage 
- Create our own train-test split to do error analysis 
- Figure out how whether any other packages can work well (e.g. Turicreate)
- Using products that were bought > 50% of the time, rather than the top 50% frequency 
Difference is that this user might have been buying items once for 90% of the time and recurring only for staples such as eggs- using the top half of a value_count list might recommend him items that he has stopped buying already






---
