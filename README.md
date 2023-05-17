# Bigmart-sales-prediction

# ****Problem Statement -****

> **The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined. The aim is to build a predictive model and find out the sales of each product at a particular store.**
> 
> 
> **Using this model, Big Mart will try to understand the properties of products and stores which play a key role in increasing sales.**
> 

---

## ****Stakeholder - Sales Manager****

# ****Get the Data****

Item_Identifier - Unique product ID
Item_Weight - Weight of the product
Item_Fat_Content - Whether the product is low fat or not
Item_Visibility - The percentage of total display area of all products in a store allocated to the particular product
Item_Type - The category to which the product belongs
Item_MRP - Maximum Retail Price (list price) of the product
Outlet_Identifier - Unique store ID
Outlet_Establishment_Year - The year in which the store was established
Outlet_Size - The size of the store in terms of ground area covered
Outlet_Location_Type - The type of city in which the store is located
Outlet_Type - Whether the outlet is just a grocery store or some sort of supermarket
Item_Outlet_Sales - Sales of the product in the particular store. This is the outcome variable to be predicted.
source - A data point from either the train or test data.

---

# Steps -

- **Import libraries**
- **Load the data**
- **Data preparation**
- **Plot and predict the model by using polynomial features with degree 6**
- **Fitting Polynomial Regression to the dataset**
- **Visualizing the Linear Regression results**
- **Visualizing the Polynomial Regression results**
- **Predicting a new result with Linear Regression**
- **Predicting a new result with Polynomial Regression**
- **Create a baseline regression model and observe the error measured.**
- **Use all features for prediction and implement a linear regression model[¶](http://localhost:8888/notebooks/DSGS/Regression%20Notebooks/Big%20Mart%20Sales%2C%20implementing%20polynomial%20features%20and%20Lasso%20.ipynb#What-will-happen-to-R-Square-score-if---the-no.-of-predictors-is-increased-in-the-model.Use-all-features-for-prediction-and-implement-a-linear-regression-model)**
- **Implementing adjusted r square**
- **Comparing r square and adjusted r square across three models**
- **checking for Heteroskedastic**
- **Look at the model coefficients of our model**
- **Dealing with non-linearity in the model**
- **Implementing Lasso regression and understanding the differences**

---

# **Important Insights -**

**We saw that addition of `Item_Visibility` variable has caused the mse to further reduced value. There is an increase in the R-square value, does it mean that the addition of `Item_Visibility` is useful for out model.**

**The only drawback of R2 is that if new predictors (X) are added to our model, R2 only increases or remains constant but it never decreases. We can not judge that by increasing complexity of our model, are we making it more accurate?**

**That is why, we use “Adjusted R-Square”.**

`**Model 2` and `Model 3` shows that there is an increment in adjusted R square while removing the features which means that those features were irrelevant to the model and were not helping to that extent to explain the variance in data.**

**We can see a funnel like shape in the plot. This shape indicates Heteroskedasticity. The presence of non-constant variance in the error terms results in heteroskedasticity. This indicates signs of non linearity in the data which has not been captured by the model.**

**We can see that as we increased the value of alpha, coefficients were approaching towards zero, but if you see in case of lasso, even at smaller alpha’s, our coefficients are reducing to absolute zeroes. Therefore, lasso selects the only some feature while reduces the coefficients of others to zero. This property is known as feature selection and which is absent in case of ridge.**
