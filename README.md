# Project 1 Revisited
## Linear Regression Coefficients Unscaled
![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/bfd913a5-4084-4bbe-b430-9dba5758a2c5)

Before dropping Item_Type:
- Intercept: Our model assumed a baseline score of -69,552.21
- Unscaled:
   - Positive:
   - Outlet_Type_Supermarket:
      - Type 3: This coefficient tells us that adding a Type 3 supermarket increases sales by 3,814.74 rupies.
      
      - Type 1: Adding a Type 1 supermarket increases sales by 1,511.49 rupies.
           
     - Type 2: Adding a Type 2 supermarket increases sales by 1,278.18 rupies.
 
![Linear_no_item_type](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/44b11a27-3fcc-4e31-a16b-6b72be4fbb6f)

After dropping Item_Type (Linear Regression):
- Intercept: Our model assumed a baseline score of 0
- Unscaled:
   - Positive:
   - Outlet_Type_Supermarket:
      - Type 3: This coefficient tells us that adding a Type 3 supermarket increases sales by 3,119.64 rupies.
      
      - Type 1: Adding a Type 1 supermarket increases sales by 1,888.05 rupies.
           
      - Type 2: Adding a Type 2 supermarket increases sales by 1,432.61 rupies.
    
## Linear Regression Permutation Importances

![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/e6a5ea40-70df-43f9-ad71-c3b3c6e7b7e0)

- In our Linear Regression model, it shows Item_MRP to be the most important to predicting sales prices, instead of Outlet_Type_Supermarket Type 3.
- Outlet_Type_Supermarket Type 3 has been traded to be the second most important, the more Type 3 supermarkets the better.
- Outlet_Type_Supermarket Type 1 is shown to be the third important. More of these types of supermarkets have a positive impact on predicting sales.

## Linear Regression SHAP

![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/cdbdd860-60aa-4d59-868b-9485435764a0)

- Item_MRP is also, shown as the most important in this graph. Interpretted as the higher the MRP SHAP the more likely the model will predict sales increasing, and the lower is most likely to decrease sales. Because red values are on the right (positive), we can see that the greater the Item_MRP, the more likely the model would predict the Item to sell.

     - Although the blue dots (fewer items with low MRP) are moderately to the left of the 0-line, indicating that the model is only moderately less likely to predict Item_MRP, compared to the big impact of having a large number of Item_MRP's.
 
 - Our model is heavily influenced to predict that the Outlet_Type_Supermarket Type 1 is less likely to increase sales, and the higher the type 1 supermarkets the less likely the model will predict higher sales.

 - The less type 3 supermarkets there are the model is slightly less likely to predict decrease in sales, the more type 3 supermarkets the model will predict heavily on the increase of sales.
      
## Random Regression Importances

![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/3c65d7d7-f1df-4d72-a94c-1b42924f407f)

- In our Random Regression model, it shows Item_MRP to be the most important to predicting sales prices at grocery store/supermarkets in India.
- Item_Visibility is shown the be the second most important, the more you're able to see it the better.
- Outlet_Type_Supermarket Type 3 is shown to be the third important. More of these types of supermarkets have a positive impact on predicting sales.
- These are shared importances with the linear regression model.

![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/283c1f10-bbdc-4627-baec-223241c25966)


- Our Feature and Permutation Importance model share Item_MRP at number 1 for being the most important coefficient. However other features have trade places. Instad of Item_Visibility being the second, as we see in Feature Importance, Outlet_Type_Supermarket Type 3 is now the second most important to the target.

![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/df507ac0-0c9b-4b76-add3-2f727ab72c23)

- Item_MRP is also, shown as the most important in this graph. Interpretted as the higher the MRP SHAP the more likely the model will predict sales increasing, and the lower is most likely to decrease sales.

     - The blue dots (fewer items with low MRP) are somewhat severely to the left of the 0-line, indicating that the model is only somewhat severely less likely to predict Item_MRP.
 
 - Our model is most likely to predict that the Outlet_Type_Supermarket Type 1 is moderately unlikely to increase sales, and the higher the type 1 supermarkets the less likely the model will predict higher sales.

 - The less type 3 supermarkets there are the model is slightly less likely to predict decrease in sales, the more type 3 supermarkets the model will predict heavily on the increase of sales.


# LIME Tubular explanation

## Random Regression

![random_reg_LIME1](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/fa5f27ae-5b10-4eb3-9187-b1675e7ff5bd)

- This store from our low-MRP group had a very high probability of high sales.
- While this store has an even number of features that were associated with positive sale predictions:
    - Item_MRP = >190.69 rupies
    - Outlet_Type_Supermarket Type 1 = 1 (yes)
    - Item_Visibility = <= 0.03

- Three of the top 5 most impactful features were associated with negative sales predictions:
    - Outlet_Type_Supermarket 3 = 0 (no)
    - Outlet_Size_Medium = 0 (no)
    - Outlet_Type_Supermarket Type 2 = 0 (no)
    
- Becasue this store is not a Type 2 or 3, and not a size medium store this will affect the sales negatively.
- Predicted sales: 5217.01 rupies

![random_reg_LIME2](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/22ce28d2-d34c-46b9-a9f5-cfc64d95ab6c)

- This store from our low-MRP group had a very high probability of low sales.
- While this store has an even number of features that were associated with positive sale predictions:
    - Outlet_Type_Supermarket 1 = 1 (yes)
    - Outlet_Size_Small = 1 (yes), also >0
    - Item_Fat_Content_Regular = 1 (yes), also >0
    - Outlet_Size_MISSING = 0 (no), known size
    - Outlet_Location_Type_Tier 2 = 1 (yes)

- Four of the top 5 most impactful features were associated with negative sales predictions:
    - Outlet_Type_Supermarket 3 = 0 (no)
    - Item_MRP = 32.06 rupies
    - Outlet_Type_Supermarket 2 = 0 (no)
    - Outlet_Size_Medium = 0 (no)
    
- Becasue this store is in a Tier 3 location, not a medium size location, no Type 2 and 3 supermarket, and a low Item_MRP this will affect the sales negatively.
- Predicted sales: 788.11 rupies

![Linear_reg_LIME1 (1)](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/61dd6934-7346-40bf-bd55-042e2e3781fc)

- This store from our high-MRP group had a high probability of sales.
- While this store has a few number of features that were associated with positive sale predictions:
    - Outlet_Type_Supermarket Type 1 = 1 (yes)
    - Item_MRP = >190.69
    - Outlet_Location_Type_Tier 2 = 1 (yes)

- Two of the top 5 most impactful features were associated with negative sales predictions:
    - Outlet_Type_Supermarket Type 3 = 0 (no)
    - Outlet_Type_Supermarket Type 2 = 0 (no)
    
- Because this store is not a Type 3 or Type 2 supermarket  this will affect the sales negatively.
- Predicted sales: 4227.53 rupies

![Linear_reg_LIME2](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/06d5027f-fc58-459c-9202-b2064d8e2a5f)

- This store from our high-MRP group had a high probability of very low sales.
- While this store has a few number of features that were associated with positive sale predictions:
    - Outlet_Type_Supermarket Type 1 = 1 (yes)
    - Outlet_Location_Type_Tier 2 = 1 (yes)
    - Item_Fat_Content_Regular = 1 (yes)
    - Outlet_Size_MISSING = 0 (no)
    
- Three of the top 5 most impactful features were associated with negative sales predictions:
    - Outlet_Type_Supermarket Type 3 = 0 (no)
    - Item_MRP = <= 98.21
    - Outlet_Type_Supermarket Type 2 = 0 (no)
    
- Because this store is not a Type 3 or Type 2 supermarket and has a low Item_MRP of 32.06 this will affect the sales negatively.
- Predicted sales: 680.65 rupies

