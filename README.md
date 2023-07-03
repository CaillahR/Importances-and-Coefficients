# Project 1 Revisited
## Linear Regression
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
      
## Random Regression

![image](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/f7ad4b00-2ac5-4960-8bc9-45dd13bb1069)

- In our Random Regression model, it shows Item_MRP to be the most important to predicting sales in India.
- Item_Visibility is shown the be the second most important, the more you're able to see it the better.
- Outlet_Type_Supermarket Type 3 is shown to be the third important. More of these types of supermarkets have a positive impact on predicting sales.
