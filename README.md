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
  
  The data was explored for missing, duplicated, and outlying data. We discovered there were no duplicates, but there were missing values in Item_Fat_Content and Outlet_Size. Item_Fat_Content was encoded into binary values for easier imputation and the missing in Outlet_Size were replaced with the most frequent data within the column. 
  Next, the catagorical columns were converted into numerical ones using one hot encoding. This allows the variables to be easily used by our machine learning model. 'Item_Identifier', 'Outlet_Identifier', 'Outlet_Establishment_Year' were dropped upon splitting data for our feature. The justification here was these 
  

# Visualization
## What type of items tend to generate the most sales?
![image](https://user-images.githubusercontent.com/93495868/225975313-d2fe4136-aebc-4dce-a977-129853006290.png)

## How did item MRP trend with item sales with item visibility?  
![image](https://user-images.githubusercontent.com/93495868/225976279-7f940ede-9226-4ace-bf74-345b1301f5ba.png)


# Results:


# Conclusion:


# Limitations of the model:
