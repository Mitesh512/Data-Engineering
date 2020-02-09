# AmExpert 2019 – Machine Learning Hackathon
# Problem Statement
XYZ Credit Card company regularly helps it’s merchants understand their data better and take key business decisions accurately by providing machine learning and analytics consulting. ABC is an established Brick & Mortar retailer that frequently conducts marketing campaigns for its diverse product range. As a merchant of XYZ, they have sought XYZ to assist them in their discount marketing process using the power of machine learning. Can you wear the AmExpert hat and help out ABC?
Discount marketing and coupon usage are very widely used promotional techniques to attract new customers and to retain & reinforce loyalty of existing customers. The measurement of a consumer’s propensity towards coupon usage and the prediction of the redemption behaviour are crucial parameters in assessing the effectiveness of a marketing campaign.

ABC’s promotions are shared across various channels including email, notifications, etc. A number of these campaigns include coupon discounts that are offered for a specific product/range of products. The retailer would like the ability to predict whether customers redeem the coupons received across channels, which will enable the retailer’s marketing team to accurately design coupon construct, and develop more precise and targeted marketing strategies.

The data available in this problem contains the following information, including the details of a sample of campaigns and coupons used in previous campaigns -

User Demographic Details

Campaign and coupon Details

Product details

Previous transactions

Based on previous transaction & performance data from the last 18 campaigns, predict the probability for the next 10 campaigns in the test set for each coupon and customer combination, whether the customer will redeem the coupon or not?


# Data-Engineering

Here we have 5 to 6 tables which will be used for feature Engineering:
We have customer data, item data, campaign data and table which maps coupons to items.

Now first focus is on Feature Engineering.
1. Campaign data has information about campaigns and date ranges
2. coupon item has maping coupons with respective items
3. Customer dempgraphic table has customer's personal information
4. Customer transaction table has information of customers id, what item id is purchased and what coupon and discounts are used. (Here lots of enginnering is performed to create data for total discounts, discount percentage, total purchase, min amount spend by customer and many more )
5. item table has information about item brand and in what category it lies.

Step By Step we will perfom feature Enginneing. 

# Modeling:
LGBM model.
Stratified K fold LGBM with Bayesian Optimizer

# Evaluation:
Submissions are evaluated on area under the ROC curve between the predicted probability and the observed target.
