# Cambridge Crime Data Cleaning and Exploratory Data Analysis

## Project Overview

This project focuses on cleaning, processing, and analyzing crime reports from Cambridge, Massachusetts. The objective is to transform raw crime data into meaningful insights through data cleaning and Exploratory Data Analysis (EDA).

Using Python and data analysis libraries, the dataset was cleaned, missing values were handled, datetime issues were resolved, and visualizations were created to identify crime patterns, trends, and high-crime areas.

---

## Problem Statement

Crime datasets often contain missing values, inconsistent formats, and large amounts of raw information that can be difficult to interpret.

The goal of this project is to:

* Clean and preprocess the Cambridge Crime Reports dataset.
* Handle missing and inconsistent data.
* Perform Exploratory Data Analysis (EDA).
* Identify crime trends and patterns.
* Generate meaningful insights using visualizations.

---

## Dataset Information

### Dataset Name

Cambridge Crime Reports Dataset

### Source

Cambridge Police Department Crime Reports

### Dataset Size

* Records: Approximately 95,923
* Columns: 7

### Features

| Column          | Description                                 |
| --------------- | ------------------------------------------- |
| File Number     | Unique identifier for each report           |
| Date of Report  | Date when the incident was reported         |
| Crime Date Time | Time period during which the crime occurred |
| Crime           | Type of crime reported                      |
| Reporting Area  | Police reporting area                       |
| Neighborhood    | Neighborhood where the crime occurred       |
| Location        | Location of the incident                    |

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Data Cleaning Process

### 1. Data Loading

The dataset was loaded into a Pandas DataFrame using:

```python
pd.read_csv()
```

### 2. Missing Value Analysis

Missing values were identified using:

```python
df.isnull().sum()
```

### 3. Handling Missing Values

Rows containing missing information were removed to improve data quality.

```python
df.dropna(inplace=True)
```

### 4. Duplicate Detection

Duplicate records were checked and removed when necessary.

```python
df.duplicated().sum()
```

### 5. Datetime Processing

The Crime Date Time column contained date ranges instead of single timestamps.

Example:

```text
02/21/2009 09:20 - 09:30
02/20/2009 22:30 - 02/21/2009 10:00
```

To enable time-based analysis:

* The starting timestamp was extracted.
* The extracted value was converted to datetime format.
* New Year, Month, and Day columns were created.

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:

### Top Crime Types

A bar chart was created to identify the most frequently reported crimes.

### Crime by Neighborhood

Neighborhood-level analysis was conducted to identify areas with higher crime activity.

### Crime Trend Over Years

Yearly crime patterns were analyzed using the extracted datetime information.

### Crime by Month

Monthly crime counts were analyzed to identify seasonal patterns.

### Crime by Day of Week

Crime frequency was examined across weekdays to understand weekly trends.

---

## Key Findings

* Certain crime categories occur significantly more often than others.
* Crime incidents are concentrated in specific neighborhoods.
* Reported crimes generally increased over time and reached higher levels around 2019–2020.
* Crime activity varies across months, suggesting seasonal patterns.
* Weekly trends indicate that some days experience higher crime frequencies than others.
* Data cleaning greatly improved the usability and quality of the dataset.

---

## Challenges Faced

### Datetime Conversion

The Crime Date Time column contained date ranges rather than single timestamps, requiring additional preprocessing before analysis.

### Missing Values

Several columns contained missing values that needed to be addressed before performing EDA.

### Feature Engineering

New variables such as Year, Month, and Day of Week were created to support time-based analysis.

---

## Repository Structure

```text
Cambridge-Crime-EDA/
│
├── README.md
├── Crime_Reports_20240701.csv
│
├── notebooks/
│   └── crime_eda.ipynb
│
└── docs/
    └── report.md
```

---

## How to Run the Project

### Clone the Repository

```bash
git clone <repository-url>
```

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

### Run the Notebook

Open:

```text
notebooks/crime_eda.ipynb
```

and execute all cells sequentially.

---

## Future Improvements

* Crime hotspot mapping using geographical coordinates.
* Predictive crime trend analysis using machine learning.
* Interactive dashboards using Power BI or Tableau.
* Crime forecasting based on historical trends.

---

## Conclusion

The Cambridge Crime Reports dataset was successfully cleaned and analyzed using Python. Missing values and datetime formatting issues were resolved, and multiple visualizations were created to identify crime patterns and trends. The project demonstrates how raw data can be transformed into meaningful insights through data cleaning and exploratory data analysis, providing valuable information that can support public safety decision-making.
