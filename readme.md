Rainfall Pattern Analysis

Project Description
This project performs Exploratory Data Analysis (EDA) on rainfall data from Salem, Erode, and Coimbatore. It analyses rainfall, temperature, and humidity to understand daily, monthly, and region-wise rainfall patterns.

 Dataset Details
- **Dataset:** Rainfall Dataset
- **File:** `rainfall_data.csv`
- **Total Records:** 540
- **Total Columns:** 5
- **Regions:** Salem, Erode, Coimbatore

Dataset Attributes

| Column | Description |
|---|---|
| Date | Date of weather record |
| Region | Region name |
| Rainfall_mm | Rainfall in millimetres |
| Temperature_C | Temperature in Celsius |
| Humidity_Percent | Humidity percentage |

Libraries Used
- Pandas – Data manipulation
- NumPy – Numerical operations
- Matplotlib – Data visualisation
- Seaborn – Statistical visualisation

Code and Analysis

1. Data Loading
Loads the rainfall CSV dataset and displays the first five records and dataset dimensions.

2. Data Exploration
Uses `info()`, `describe()`, and `isnull().sum()` to examine dataset structure, statistics, and missing values.

3. Data Cleaning
Removes duplicate and missing records and converts the date column into datetime format.

4. Month and Year Extraction
Extracts month and year from the date column for time-based analysis.

5. Correlation Analysis
Calculates the correlation between rainfall, temperature, and humidity.

6. Daily Rainfall Analysis
Groups rainfall data by date and calculates the average daily rainfall.

7. Monthly Rainfall Analysis
Groups rainfall data by month and calculates monthly average rainfall.

8. Region-wise Rainfall Analysis
Compares average rainfall across Salem, Erode, and Coimbatore.

Visualisations

1. **Scatter Plot – Rainfall vs Temperature:** Analyses the relationship between rainfall and temperature.
2. **Scatter Plot – Rainfall vs Humidity:** Analyses the relationship between rainfall and humidity.
3. **Correlation Heatmap:** Displays correlations between weather variables.
4. **Line Chart:** Shows daily rainfall trends.
5. **Bar Chart – Monthly Rainfall:** Compares monthly average rainfall.
6. **Bar Chart – Region-wise Rainfall:** Compares rainfall across the three regions.

Results

Correlation Analysis

| Variables | Correlation |
|---|---:|
| Rainfall and Temperature | -0.065582 |
| Rainfall and Humidity | 0.210762 |
| Temperature and Humidity | -0.062446 |

Monthly Average Rainfall

| Month | Average Rainfall (mm) |
|---|---:|
| January | 4.630108 |
| February | 6.482143 |
| March | 7.075269 |
| April | 5.971111 |
| May | 8.813978 |
| June | 9.694253 |

Region-wise Average Rainfall

| Region | Average Rainfall (mm) |
|---|---:|
| Coimbatore | 6.875556 |
| Erode | 7.496667 |
| Salem | 6.925556 |

Observations
- June has the highest average rainfall among the months analysed.
- January has the lowest average rainfall.
- Erode has the highest average rainfall among the three regions.
- Rainfall has a weak positive correlation with humidity.
- Rainfall has a very weak negative correlation with temperature.

How to Run
1. Open Google Colab.
2. Upload `Rainfall_Analysis.ipynb`.
3. Upload `rainfall_data.csv`.
4. Run the notebook cells in sequence.
5. View the analysis results and visualisations.

Installation

```bash
pip install pandas numpy matplotlib seaborn
```
Platform Used
Google Colab

Conclusion
This project analyses rainfall patterns across Salem, Erode, and Coimbatore using Python. It examines daily and monthly rainfall trends, compares rainfall across regions, and studies the relationship between rainfall, temperature, and humidity through data analysis and visualisation.
