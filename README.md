# **Dominos Predictive Purchase Order System**

## **Overview**
The Dominos Predictive Purchase Order System leverages historical sales data and machine learning models to forecast weekly pizza sales. Based on these predictions, the system calculates the required quantities of ingredients for the upcoming week and generates a detailed purchase order to streamline inventory management and procurement processes.

---

## **Features**

- **Sales Prediction**: 
  - Predict weekly pizza sales using LSTM (Long Short-Term Memory) models.
  - Supports predictions for individual pizza types.

- **Ingredient Calculation**:
  - Calculate required quantities of ingredients based on sales predictions.
  - Support for dynamic ingredient mapping via the `Pizza_ingredients.csv` dataset.

- **Purchase Order Generation**:
  - Generate a detailed purchase order for all required ingredients.
  - Provide totals and summaries for streamlined procurement.

---

## **Tech Stack**

- **Programming Language**: Python
- **Libraries**:
  - Data Processing: `numpy`, `pandas`
  - Machine Learning: `keras`, `sklearn`
  - Visualization: `matplotlib`

---

## **Data Files**

1. **Pizza_Sales.csv**:
   - Contains historical pizza sales data.
   - Key columns:
     - `order_date`: Date of the order.
     - `pizza_name_id`: Unique identifier for each pizza type.
     - `quantity`: Quantity of pizzas sold.

2. **Pizza_ingredients.csv**:
   - Contains ingredient details for each pizza type.
   - Key columns:
     - `pizza_name_id`: Unique identifier for each pizza type.
     - `pizza_ingredients`: Name of the ingredient.
     - `Items_Qty_In_Grams`: Quantity of the ingredient required per pizza.

---

## **Workflow**

1. **Data Preprocessing**:
   - Aggregate weekly sales data from `Pizza_Sales.csv`.
   - Normalize sales data for model input.

2. **Model Training and Prediction**:
   - Train an LSTM model for each pizza type using historical sales data.
   - Predict sales for the upcoming week for each pizza type.

3. **Ingredient Calculation**:
   - Multiply predicted pizza sales by ingredient requirements from `Pizza_ingredients.csv`.
   - Summarize ingredient requirements for all pizzas.

4. **Purchase Order Generation**:
   - Generate a detailed purchase order with the required quantities of each ingredient.

---
