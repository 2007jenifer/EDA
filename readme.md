# Rainfall Pattern Analysis

## 1. Project Description
This project performs Exploratory Data Analysis (EDA) on rainfall data from Salem, Erode, and Coimbatore. It analyses rainfall, temperature, and humidity to understand daily, monthly, and region-wise rainfall patterns.

## 2. Tools and Technologies
- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 3. Dataset Details
- Dataset Name: Rainfall Dataset
- File Name: `rainfall_data.csv`
- Total Records: 540
- Total Columns: 5
- Regions: Salem, Erode, Coimbatore

### Dataset Attributes

| Column | Description |
|---|---|
| Date | Date of weather record |
| Region | Region name |
| Rainfall_mm | Rainfall in millimetres |
| Temperature_C | Temperature in Celsius |
| Humidity_Percent | Humidity percentage |

## 4. Python Code and Implementation

### 4.1 Importing Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

**Purpose:** Imports the libraries required for data manipulation, numerical calculations, and visualisation.

### 4.2 Loading the Dataset

```python
data = pd.read_csv('/content/rainfall_data.csv')

print(data.head())

print(data.shape)
```

**Purpose:** Loads the rainfall dataset and displays the first five records and dataset dimensions.

**Output:** 540 rows and 5 columns.

### 4.3 Exploring the Dataset

```python
print(data.info())

print(data.describe())

print(data.isnull().sum())
```

**Purpose:** Displays dataset information, statistical summary, and missing values.

**Output:** No missing values were found in the dataset.

### 4.4 Data Cleaning

```python
data = data.drop_duplicates()

data = data.dropna()

data['Date'] = pd.to_datetime(data['Date'])

print(data.head())
```

**Purpose:** Removes duplicate and missing records and converts the date column into datetime format.

### 4.5 Extracting Month and Year

```python
data['Month'] = data['Date'].dt.month

data['Year'] = data['Date'].dt.year
```

**Purpose:** Extracts month and year information from the date column for time-based analysis.

### 4.6 Correlation Analysis

```python
print(data[['Rainfall_mm',
            'Temperature_C',
            'Humidity_Percent']].corr())
```

**Purpose:** Calculates the correlation between rainfall, temperature, and humidity.

### 4.7 Daily Rainfall Analysis

```python
daily_rainfall = data.groupby('Date')['Rainfall_mm'].mean()

print(daily_rainfall.head())
```

**Purpose:** Calculates the average rainfall for each date.

### 4.8 Monthly Rainfall Analysis

```python
monthly_rainfall = data.groupby('Month')['Rainfall_mm'].mean()

print(monthly_rainfall)
```

**Purpose:** Calculates the average rainfall for each month.

### 4.9 Region-wise Rainfall Analysis

```python
region_rainfall = data.groupby('Region')['Rainfall_mm'].mean()

print(region_rainfall)
```

**Purpose:** Calculates and compares average rainfall across Salem, Erode, and Coimbatore.

## 5. Data Visualisation

### 5.1 Rainfall vs Temperature

```python
sns.scatterplot(
    data=data,
    x='Temperature_C',
    y='Rainfall_mm'
)

plt.title('Rainfall vs Temperature')
plt.xlabel('Temperature (C)')
plt.ylabel('Rainfall (mm)')

plt.show()
```

**Purpose:** Analyses the relationship between temperature and rainfall.

### 5.2 Rainfall vs Humidity

```python
sns.scatterplot(
    data=data,
    x='Humidity_Percent',
    y='Rainfall_mm'
)

plt.title('Rainfall vs Humidity')
plt.xlabel('Humidity (%)')
plt.ylabel('Rainfall (mm)')

plt.show()
```

**Purpose:** Analyses the relationship between humidity and rainfall.

### 5.3 Correlation Heatmap

```python
sns.heatmap(
    data[['Rainfall_mm',
          'Temperature_C',
          'Humidity_Percent']].corr(),
    annot=True,
    cmap='coolwarm'
)

plt.title('Weather Variable Correlation Heatmap')

plt.show()
```

**Purpose:** Displays the correlation between weather variables using a heatmap.

### 5.4 Daily Rainfall Trend

```python
daily_rainfall.plot(kind='line')

plt.title('Daily Rainfall Trend')
plt.xlabel('Date')
plt.ylabel('Average Rainfall (mm)')

plt.show()
```

**Purpose:** Visualises daily average rainfall trends.

### 5.5 Monthly Rainfall Analysis

```python
monthly_rainfall.plot(kind='bar')

plt.title('Monthly Rainfall Analysis')
plt.xlabel('Month')
plt.ylabel('Average Rainfall (mm)')

plt.show()
```

**Purpose:** Compares average rainfall across different months.

### 5.6 Region-wise Rainfall Comparison

```python
region_rainfall.plot(kind='bar')

plt.title('Rainfall Comparison by Region')
plt.xlabel('Region')
plt.ylabel('Average Rainfall (mm)')

plt.show()
```

**Purpose:** Compares average rainfall across Salem, Erode, and Coimbatore.

## 6. Results and Observations

### 6.1 Correlation Results

| Variables | Correlation |
|---|---:|
| Rainfall and Temperature | -0.065582 |
| Rainfall and Humidity | 0.210762 |
| Temperature and Humidity | -0.062446 |

### 6.2 Monthly Average Rainfall

| Month | Average Rainfall (mm) |
|---|---:|
| January | 4.630108 |
| February | 6.482143 |
| March | 7.075269 |
| April | 5.971111 |
| May | 8.813978 |
| June | 9.694253 |

### 6.3 Region-wise Average Rainfall

| Region | Average Rainfall (mm) |
|---|---:|
| Coimbatore | 6.875556 |
| Erode | 7.496667 |
| Salem | 6.925556 |

### Observations
- June has the highest average rainfall among the months analysed.
- January has the lowest average rainfall.
- Erode has the highest average rainfall among the three regions.
- Rainfall has a weak positive correlation with humidity.
- Rainfall has a very weak negative correlation with temperature.

## 7. How to Run the Project

1. Open Google Colab.
2. Upload `Rainfall_Analysis.ipynb`.
3. Upload `rainfall_data.csv`.
4. Run the notebook cells in sequence.
5. View the analysis results and charts.

### Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

## 8. Platform Used
Google Colab

## 9. Conclusion
This project analyses rainfall patterns across Salem, Erode, and Coimbatore. It studies daily and monthly rainfall trends, compares rainfall across regions, and examines the relationship between rainfall, temperature, and humidity using Python-based data analysis and visualisation.
