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
      
## Random Regression Importances

![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/3c65d7d7-f1df-4d72-a94c-1b42924f407f)

- In our Random Regression model, it shows Item_MRP to be the most important to predicting sales prices at grocery store/supermarkets in India.
- Item_Visibility is shown the be the second most important, the more you're able to see it the better.
- Outlet_Type_Supermarket Type 3 is shown to be the third important. More of these types of supermarkets have a positive impact on predicting sales.
- These are shared importances with the linear regression model.

![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/283c1f10-bbdc-4627-baec-223241c25966)


- Our Feature and Permutation Importance model share Item_MRP at number 1 for being the most important coefficient. However other features have trade places. Instad of Item_Visibility being the second, as we see in Feature Importance, Outlet_Type_Supermarket Type 3 is now the second most important to the target.



