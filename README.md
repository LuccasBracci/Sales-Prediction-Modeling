# Sales Predictions

## Creating a model for sales predictions 

### Problem: 
  
  How can we use machine learning models to acccurately forecast outlet sales based on 8 different variables?

### Data dictionary:

<table>
    <tbody>
        <tr>
            <td><strong>Variable Name</strong></td>
            <td><strong>Description</strong></td>
        </tr>
        <tr>
            <td>Item_Identifier</td>
            <td>Unique product ID</td>
        </tr>
        <tr>
            <td>Item_Weight</td>
            <td>Weight of product</td>
        </tr>
        <tr>
            <td>Item_Fat_Content</td>
            <td>Whether the product is low fat or regular</td>
        </tr>
        <tr>
            <td>Item_Visibility</td>
            <td>The percentage of total display area of all products in a store allocated to the particular product</td></tr>
        <tr>
            <td>Item_Type</td>
            <td>The category to which the product belongs</td>
        </tr>
        <tr>
            <td>Item_MRP</td>
            <td>Maximum Retail Price (list price) of the product</td>
        </tr>
        <tr>
            <td>Outlet_Identifier</td>
            <td>Unique store ID</td>
        </tr>
        <tr>
            <td>Outlet_Establishment_Year</td>
            <td>The year in which store was established</td>
        </tr>
        <tr>
            <td>Outlet_Size</td>
            <td>The size of the store in terms of ground area covered</td>
        </tr>
        <tr>
            <td>Outlet_Location_Type</td>
            <td>The type of area in which the store is located</td>
        </tr>
        <tr>
            <td>Outlet_Type</td>
            <td>Whether the outlet is a grocery store or some sort of supermarket</td>
        </tr>
        <tr>
            <td>Item_Outlet_Sales</td>
            <td>Sales of the product in the particular store. This is the target variable to be predicted.        
</td>
        </tr>
    </tbody>
            </table>
  
# Methodology

  ## Data Preparation:
  
  The data was explored for missing, duplicated, and outlying data. We discovered there were no duplicates, but there were missing values in Item_Fat_Content and Outlet_Size. Item_Fat_Content was encoded into binary values for easier imputation and the missing in Outlet_Size were replaced with the most frequent data within the column. Most Frequen imputation ensures the distribution of data in a column that is not altered in any significant way. Mean imputation does not diseminate bias among the dataset as it preserves the sample size and works well with normally distributed variables.
  Next, the catagorical columns were converted into numerical ones using one hot encoding. This allows the variables to be easily used by our machine learning model. 'Item_Identifier', 'Outlet_Identifier', 'Outlet_Establishment_Year' were dropped upon splitting data for our feature. The justification here was these columns were not relevant for analysis or modeling and do not pose a strong relationship with predicting outlet sales.
  

# Visualization
## What type of items tend to generate the most sales?
![image](https://user-images.githubusercontent.com/93495868/225975313-d2fe4136-aebc-4dce-a977-129853006290.png)

### We can extrapolate that starchy food products are a popular commodity for customers. 
Starchy foods being the highest generate more consistent sales and it can be infered thay it is always in high demand among consumers.

## How did item MRP trend with item sales with item visibility?  
![image](https://user-images.githubusercontent.com/93495868/225976279-7f940ede-9226-4ace-bf74-345b1301f5ba.png)

### This graph shows that items of a higher mrp tend to generate more sales, however the higher density of items are within $75 and $150. Visually this graph demonstrates that item visibility does not have a strong contribution to item sales and suggests that other factors have an impact on item sales than visibility.



# Results:

## The metrics of the Decision Tree Regression model:

| Metrics      | Score |
| ----------- | ----------- |
| MAE     |   738.32    |
| MSE| 1,118,185.97       |
| R2| 0.59        |
| RMSE| 1,057.44      |

### The MAE of 738.32 suggests that the model's predictions have an error of $738.32. This is the best possible range of this model and further refining of parameters may give better results.

## 

# Conclusion:

###  This model is intended to predict outlet sales within +/- $738.32.  


# Limitations of the model:

### Although the accuracy is not perfect with room for improvement, the R2 score suggests the model explains ~%59 variance in outlet sales data. %41 of variance is not being captured by the model and it is worth exploring additional ways or alternative machine learning algorithms to achieve higher accuracy.

	
