Food Delivery Analysis

Project Description
This project performs Exploratory Data Analysis (EDA) on food delivery data using Python. It analyses food categories, food items, order amounts, delivery times, and order status to understand customer ordering patterns.

Dataset Details
- **Dataset:** Food Delivery Dataset
- **File:** `food_delivery_data.csv`
- **Total Records:** 100
- **Total Columns:** 9

Dataset Attributes

| Column | Description |
|---|---|
| Order_ID | Unique order ID |
| Customer_ID | Customer ID |
| Food_Category | Category of food |
| Food_Item | Name of food item |
| Order_Date | Date of order |
| Order_Time | Time of order |
| Order_Amount | Amount of order |
| Delivery_Time_Minutes | Delivery duration |
| Order_Status | Delivered or Cancelled |

Libraries Used
- Pandas – Data manipulation
- NumPy – Numerical operations
- Matplotlib – Data visualisation
- Seaborn – Statistical visualisation

Code and Analysis

1. Data Loading
Loads the CSV dataset and displays the first five records and dataset dimensions.

2. Data Exploration
Uses `info()`, `describe()`, and `isnull().sum()` to understand the dataset structure, statistics, and missing values.

3. Data Cleaning
Removes duplicate and missing records, cleans column names, and converts the order date into datetime format.

4. Food Category Analysis
Uses `value_counts()` to identify the number of orders in each food category.

5. Food Item Analysis
Analyses the number of orders for individual food items.

6. Average Order Amount
Calculates the average amount spent on orders.

7. Delivery Time Analysis
Calculates the average delivery time in minutes.

8. Order Status Analysis
Counts delivered and cancelled orders.

Visualisations

1. **Bar Chart:** Compares the number of orders across food categories.
2. **Pie Chart:** Displays food category distribution.
3. **Histogram:** Shows the distribution of delivery times.
4. **Box Plot:** Displays the distribution of order amounts.

Results

| Analysis | Result |
|---|---:|
| Total Orders | 100 |
| Average Order Amount | ₹386.81 |
| Average Delivery Time | 41.07 minutes |
| Delivered Orders | 76 |
| Cancelled Orders | 24 |

Food Category Results

| Category | Orders |
|---|---:|
| Burger | 24 |
| Desserts | 18 |
| Biryani | 17 |
| Chinese | 15 |
| Pizza | 14 |
| South Indian | 12 |

Observations
- Burger is the most ordered food category.
- South Indian has the lowest number of orders.
- Average order amount is ₹386.81.
- Average delivery time is 41.07 minutes.
- 76 orders were delivered and 24 were cancelled.

How to Run
1. Open Google Colab.
2. Upload `Food_delivery_analysis.ipynb`.
3. Upload `food_delivery_data.csv`.
4. Run the notebook cells in sequence.
5. View the outputs and visualisations.

Installation

```bash
pip install pandas numpy matplotlib seaborn
```
Platform Used
Google Colab

Conclusion
This project helps understand food delivery patterns by analysing food categories, order amounts, delivery times, and order status through Python-based data analysis and visualisation.
