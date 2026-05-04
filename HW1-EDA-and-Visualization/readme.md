حتماً. این README برای فولدر تمرین اول یعنی مثلاً `HW1-EDA-and-Visualization` مناسبه و بر اساس صورت تمرین PDF نوشته شده؛ یعنی سه بخش اصلی فروشگاه، نظرسنجی مشتریان و دیتاست پزشکی را پوشش می‌دهد. 

````markdown
# HW1 - Exploratory Data Analysis and Visualization

This folder contains the first homework assignment for the **Data Mining** course.  
The assignment focuses on basic exploratory data analysis, data visualization, and outlier detection using Python.

## Overview

In this homework, three different datasets are analyzed:

1. Sales data from stores
2. Customer satisfaction survey data
3. Medical patient data

The main goal of this assignment is to practice data analysis techniques such as:

- Grouping and summarizing data
- Creating visualizations
- Detecting outliers using the IQR method
- Comparing distributions between different groups
- Interpreting data patterns from plots

## Tools and Libraries

The following Python libraries are used in this homework:

```python
pandas
numpy
matplotlib
seaborn
````

## Project Structure

```text
HW1-EDA-and-Visualization/
│
├── HW1.ipynb
├── HW1-report.pdf
├── README.md
└── data/
    └── Optional dataset files
```

## Questions

## Question 1: Sales Data Analysis

### Dataset Description

The first dataset contains sales information from different stores during a year.

### Columns

```text
Date
StoreID
ProductCategory
SalesAmount
```

### Tasks

The required tasks for this question are:

1. Draw a box plot for each `ProductCategory` to show the distribution of `SalesAmount`.
2. Detect outliers in each `ProductCategory` using the `1.5 * IQR` rule.
3. Create a new DataFrame containing the following columns:

```text
StoreID
ProductCategory
SalesAmount
Outlier
```

The `Outlier` column contains Boolean values:

```text
True  -> The record is an outlier
False -> The record is not an outlier
```

### Method

For each product category, the following values are calculated:

```text
Q1  = First quartile
Q3  = Third quartile
IQR = Q3 - Q1
```

Then, the lower and upper bounds are calculated as:

```text
Lower Bound = Q1 - 1.5 * IQR
Upper Bound = Q3 + 1.5 * IQR
```

Any `SalesAmount` value outside this range is considered an outlier.

### Output

The output of this question includes:

* A box plot of `SalesAmount` by `ProductCategory`
* A DataFrame showing whether each sales record is an outlier
* A visualization highlighting the detected outliers

---

## Question 2: Customer Satisfaction Analysis

### Dataset Description

The second dataset contains customer survey information.

### Columns

```text
CustomerID
Region
SatisfactionScore
```

The `SatisfactionScore` values range from 1 to 5.

### Tasks

The required tasks for this question are:

1. Calculate the average `SatisfactionScore` for each `Region`.
2. Draw a bar plot where each bar represents a region.
3. Sort the bars in descending order based on the average satisfaction score.
4. Display the number of customers who completed the survey on each bar.

### Method

The data is grouped by `Region`, and two values are calculated for each region:

```text
MeanSatisfaction = Average SatisfactionScore
CustomerCount    = Number of customers in that region
```

The result is then sorted in descending order based on `MeanSatisfaction`.

### Output

The output of this question includes:

* A summary table containing the average satisfaction score and customer count for each region
* A sorted bar plot showing the average satisfaction score by region
* Customer counts displayed on top of each bar

---

## Question 3: Medical Data Analysis

### Dataset Description

The third dataset contains medical information about patients.

### Columns

```text
PatientID
Age
BloodPressure
Cholesterol
Diagnosis
```

The `Diagnosis` column contains two possible values:

```text
Healthy
Sick
```

### Tasks

The required tasks for this question are:

1. Draw a violin plot to compare the distribution of `BloodPressure` between `Healthy` and `Sick` patients.
2. Add real patient data points to the same plot using a scatter plot.
3. Use point colors to represent the `Cholesterol` value of each patient.
4. Analyze whether the blood pressure distribution pattern is different between healthy and sick patients.

### Method

A violin plot is used to compare the overall shape of the blood pressure distribution in each diagnosis group.

Then, a scatter plot is added on top of the violin plot to show individual patient records.
The color of each scatter point represents the patient's cholesterol value.

### Output

The output of this question includes:

* A violin plot comparing `BloodPressure` between `Healthy` and `Sick` patients
* A combined violin and scatter plot
* A color bar representing `Cholesterol`
* A written analysis of the blood pressure distribution patterns

### Analysis Summary

Based on the generated dataset, the `Healthy` group has a slightly higher central blood pressure value compared to the `Sick` group. However, the `Sick` group shows more variability in blood pressure values.

Since the dataset is artificially generated and the `Diagnosis` values are assigned randomly, the observed difference should not be interpreted as a real medical relationship. The difference is most likely due to randomness in the generated data.

---

## Learning Objectives

By completing this homework, the following concepts are practiced:

* Loading and working with tabular data
* Using `pandas` for grouping and aggregation
* Drawing box plots, bar plots, violin plots, and scatter plots
* Detecting outliers using the IQR method
* Interpreting visual patterns in data
* Writing basic analytical conclusions from plots and summary statistics

## How to Run

To run the notebook, open the following file in Jupyter Notebook or JupyterLab:

```text
HW1.ipynb
```

Then run the cells in order from top to bottom.

## Main Files

```text
HW1.ipynb        Main notebook containing code, plots, and analysis
HW1-report.pdf   PDF version of the completed homework
README.md        Description of the homework and project structure
```

## Course Information

```text
Course: Data Mining
Assignment: Homework 1
Topic: Exploratory Data Analysis and Visualization
```

```