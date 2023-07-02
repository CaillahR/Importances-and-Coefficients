# Project 1 Revisited
 
![Linear_Unscaled](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/78fa8571-88a1-457f-8955-31653cc9b818)

- Intercept: Our model assumed a baseline score of -69,552.21
 - Unscaled:
  - Positive:
  - Outlet_Type_Supermarket:
    - Type 3: This coefficient tells us that adding a Type 3 supermarket increases sales by $3,814.74.

    - Type 1: Adding a Type 1 supermarket increases sales by $1,511.49.

    - Type 2: Adding a Type 2 supermarket increases sales by $1,278.18.
      
![Linear_Scaled](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/f713fcbb-ca1c-4ed5-a156-3d61777a2041)

- For the scaled data the most important are still Outlet_Type_Supermarket 3, 1, & 2. This model is putting most of its' weight on these three deciding factors, for predicting the target. 

- The new baseline of the intercept is 1,367.59.

![Regression, Unscaled](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/c8b2db2b-905d-4027-9ae6-d66bd7e8dddc)

- This model shows that Item_MRP has the highest relationship with the target. The 2nd, 3rd, 4th, and 5th are Outlet_Type_Grocery Store, Item_Visibility, Outlet_Typer_Supermarket Type3, and Item_Weight.
  
![Regression, Scaled](https://github.com/CaillahR/Importances-and-Coefficients/assets/121994185/672d4e9c-42f0-4e90-98a7-8ad7edf706cf)

- Scaled, the 5 most important features stayed the same with Item_MRP still having the highest importance. But, the order of the other features have changed.
