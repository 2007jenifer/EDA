Food Delivery Analysis

1. Project Description
This project performs Exploratory Data Analysis (EDA) on food delivery data using Python. It analyses food categories, food items, order amounts, delivery times, and order status to understand customer ordering patterns.

2. Tools and Technologies
- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

3. Dataset Details
- Dataset Name: Food Delivery Dataset
- File Name: `food_delivery_data.csv`
- Total Records: 100
- Total Columns: 9

Dataset Attributes

| Column | Description |
|---|---|
| Order_ID | Unique order identifier |
| Customer_ID | Customer identifier |
| Food_Category | Category of food |
| Food_Item | Name of food item |
| Order_Date | Date of order |
| Order_Time | Time of order |
| Order_Amount | Order amount |
| Delivery_Time_Minutes | Delivery duration |
| Order_Status | Delivered or Cancelled |

4. Python Code and Implementation

4.1 Importing Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

**Purpose:** Imports the libraries required for data manipulation, numerical calculations, and visualisation.

4.2 Loading the Dataset

```python
data = pd.read_csv('/content/food_delivery_data.csv')

print(data.head())
print(data.shape)
```

**Purpose:** Loads the CSV dataset and displays the first five records and dataset dimensions.

**Output:** 100 rows and 9 columns.

4.3 Exploring the Dataset

```python
print(data.info())
print(data.describe())
print(data.isnull().sum())
```

**Purpose:** Displays dataset information, statistical summary, and missing values.

**Output:** No missing values were found in the dataset.

4.4 Data Cleaning

```python
data = data.drop_duplicates()

data = data.dropna()

data.columns = data.columns.str.strip()

data['Order_Date'] = pd.to_datetime(data['Order_Date'])

print(data.head())
```

**Purpose:** Removes duplicate and missing records, cleans column names, and converts the order date into datetime format.

4.5 Food Category Analysis

```python
print(data['Food_Category'].value_counts())
```

**Purpose:** Counts the number of orders in each food category.

4.6 Food Item Analysis

```python
print(data['Food_Item'].value_counts())
```

**Purpose:** Finds the number of orders for each individual food item.

4.7 Average Order Amount

```python
print(data['Order_Amount'].mean())
```

**Output:** 386.81

**Purpose:** Calculates the average order amount.

4.8 Average Delivery Time

```python
print(data['Delivery_Time_Minutes'].mean())
```

**Output:** 41.07 minutes

**Purpose:** Calculates the average delivery time.

4.9 Order Status Analysis

```python
print(data['Order_Status'].value_counts())
```

**Output:**
- Delivered: 76
- Cancelled: 24

**Purpose:** Counts delivered and cancelled orders.

 5. Data Visualisation

5.1 Food Category Bar Chart

```python
data['Food_Category'].value_counts().plot(kind='bar')

plt.title('Food Category Ordering Analysis')
plt.xlabel('Food Category')
plt.ylabel('Number of Orders')

plt.show()
```

**Purpose:** Compares the number of orders in each food category.

5.2 Food Category Pie Chart

```python
data['Food_Category'].value_counts().plot(
    kind='pie',
    autopct='%1.1f%%'
)

plt.title('Food Category Distribution')
plt.ylabel('')

plt.show()
```

**Purpose:** Displays the percentage distribution of food categories.

5.3 Delivery Time Histogram

```python
plt.hist(data['Delivery_Time_Minutes'], bins=10)

plt.title('Food Delivery Time Distribution')
plt.xlabel('Delivery Time in Minutes')
plt.ylabel('Number of Orders')

plt.show()
```

**Purpose:** Shows the distribution of food delivery times.

5.4 Order Amount Box Plot

```python
sns.boxplot(x=data['Order_Amount'])

plt.title('Food Order Amount Box Plot')
plt.xlabel('Order Amount (Rs)')

plt.show()
```

**Purpose:** Displays the distribution and spread of order amounts.

6. Results and Observations

Summary of Results

| Analysis | Result |
|---|---:|
| Total Orders | 100 |
| Average Order Amount | ₹386.81 |
| Average Delivery Time | 41.07 minutes |
| Delivered Orders | 76 |
| Cancelled Orders | 24 |

Food Category Results

| Food Category | Number of Orders |
|---|---:|
| Burger | 24 |
| Desserts | 18 |
| Biryani | 17 |
| Chinese | 15 |
| Pizza | 14 |
| South Indian | 12 |

Observations
- Burger is the most frequently ordered food category.
- South Indian has the lowest number of orders.
- Average order amount is ₹386.81.
- Average delivery time is 41.07 minutes.
- 76 orders were delivered and 24 orders were cancelled.

7. How to Run the Project

1. Open Google Colab.
2. Upload `Food_delivery_analysis.ipynb`.
3. Upload `food_delivery_data.csv`.
4. Run the notebook cells in sequence.
5. View the analysis results and charts.

Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

8. Platform Used
Google Colab

9. Conclusion
This project analyses food delivery data to understand customer ordering patterns, popular food categories, average order amounts, delivery times, and order status using Python and data visualisation.
