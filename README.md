

# HVAC Sensor Data Analysis

**SUPRAKASH MAITY**
**2nd Year, Department of Mechanical Engineering**
**ARM College of Engineering & Technology**
**Course: Data Analysis in Mechanical Engineering**

---

## Introduction

This project focuses on analyzing data collected from HVAC (Heating, Ventilation, and Air Conditioning) systems. By studying environmental and operational parameters like temperature, humidity, air flow, CO₂ concentration, occupancy, and energy usage, we aim to gain meaningful insights into how these systems behave in real-world settings.

The goal is to find patterns that can help improve energy efficiency and support decisions in building management and automation.

---

## Why This Project Matters

Understanding HVAC data is important because it allows us to:

* Detect trends in energy usage and environmental conditions
* Identify periods or conditions that cause high energy consumption
* Support smart building systems by providing data-driven insights
* Improve comfort and air quality while reducing operational costs

---

## About the Dataset

The dataset contains time-stamped sensor readings recorded from an HVAC system. Here's a brief description of each feature:

| **Feature**               | **What it Represents**                  |
| ------------------------- | --------------------------------------- |
| Date\_Logged              | Date and time the data was recorded     |
| Temperature (C)           | Indoor temperature in Celsius           |
| Humidity (%)              | Indoor humidity percentage              |
| Air\_Flow (CFM)           | Air flow rate in cubic feet per minute  |
| CO2\_Level (ppm)          | CO₂ concentration inside the room (ppm) |
| Occupancy                 | Number of people present at that time   |
| Energy\_Consumption (kWh) | Energy used by the HVAC system (in kWh) |

---

## How the Data Was Processed

1. **Data Loading and Initial Check**
   The dataset was loaded using pandas, and basic inspection was done to understand column types and data shape.

2. **Date Formatting**
   The `Date_Logged` column was converted to a datetime format for easier time-based analysis.

3. **Handling Missing Values**
   Missing entries in columns like `CO2_Level` and `Air_Flow` were filled using their respective mean values.

4. **Feature Creation**
   New features were extracted from the timestamp:

   * `Hour` to identify usage patterns throughout the day
   * `DayOfWeek` to detect weekday vs weekend differences

---

## What the Exploratory Data Analysis Revealed

### Time-Based Trends

* Energy consumption shows a consistent pattern, peaking during typical working hours (9 AM to 6 PM).
* CO₂ levels and temperature also change based on occupancy.

### Relationships Between Features

* `CO2_Level` increases with the number of people in the room.
* Higher occupancy also leads to increased air flow, possibly due to automatic system adjustments.
* Energy usage is moderately influenced by temperature and airflow.

### Data Distribution

* Some features like energy consumption and air flow showed signs of skewness.
* Boxplots helped identify potential outliers that could affect model performance in later steps.

---

## Main Takeaways

* **Occupancy strongly affects CO₂ concentration**: More people leads to higher CO₂ levels, as expected.
* **Air Flow adjusts automatically** based on how many people are present.
* **Energy use follows a daily cycle**, peaking during office hours on weekdays.
* **Temperature and humidity remain mostly stable**, showing that the system works effectively under normal conditions.

---

## What’s Next?

This project could be taken further by:

* Applying outlier detection techniques to clean up any abnormal readings
* Building machine learning models to predict energy consumption
* Detecting anomalies that may signal inefficiencies or system faults

---

## Tools and Technologies Used

* **Python** with **Pandas** and **NumPy** for data manipulation
* **Matplotlib** and **Plotly** for data visualization
* **Jupyter Notebook** as the development environment
