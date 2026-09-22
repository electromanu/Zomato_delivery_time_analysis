# Zomato Delivery Time Analysis

## 📊 Project Overview

An interactive Power BI dashboard developed to analyze delivery times and identify operational factors associated with longer delivery durations.

The analysis focuses on factors such as **weather conditions, road traffic, vehicle condition, festivals, and multiple deliveries** to understand how they relate to delivery time.

---

## 🎯 Business Problem

The company has delivery data containing information about delivery personnel, locations, weather, traffic, vehicles, order types, festivals, and delivery time.

The objective of this project is to transform the raw data into meaningful business insights and identify the factors associated with slower deliveries.

### Main Business Question

**Which factors are associated with longer delivery times?**

### Supporting Questions

* How does road traffic affect delivery time under different weather conditions?
* Does vehicle condition have an impact on delivery time?
* How do festival days differ from non-festival days?
* Does the number of multiple deliveries assigned to a delivery person affect delivery time?
* How do delivery person age and rating relate to delivery time?

---

## 🗂️ Dataset

The dataset contains information about:

* Delivery person ID
* Delivery person age
* Delivery person rating
* Restaurant location
* Delivery location
* Order date
* Weather conditions
* Road traffic density
* Vehicle condition
* Type of order
* Type of vehicle
* Multiple deliveries
* Festival
* City
* Time taken for delivery

The target metric used in the analysis is **Time Taken (Minutes)**.

---

## 🧹 Data Cleaning

The raw dataset was prepared before analysis.

Main cleaning steps included:

* Removed records containing invalid location values such as zero or negative coordinates.
* Removed order time and pickup time fields because delivery time was already provided in the dataset.
* Removed records with missing city or weather information.
* Checked for duplicate records.
* Converted order dates into a proper date format.
* Checked delivery person age and rating for potential outliers.
* Validated the data types of the columns.

---

## 🔍 Analysis

The analysis was performed around several operational factors.

### Weather & Traffic

The combination of traffic and weather conditions was analyzed to identify situations associated with longer delivery times.

The highest average delivery times were observed under:

| Traffic | Weather | Average Delivery Time |
| ------- | ------- | --------------------: |
| Jam     | Fog     |             36.89 min |
| Jam     | Cloudy  |             36.71 min |

The overall analysis indicates that **heavy traffic combined with adverse weather conditions is associated with longer delivery times**.

### Vehicle Condition

Delivery time was compared across vehicle-condition categories.

| Vehicle Condition | Average Delivery Time |
| ----------------- | --------------------: |
| 0                 |             30.25 min |
| 1                 |             24.58 min |
| 2                 |             24.67 min |

Vehicles with condition score **0** showed a higher average delivery time than vehicles with scores 1 and 2.

### Festival Days

Delivery times were compared between festival and non-festival days.

| Period       | Average Delivery Time |
| ------------ | --------------------: |
| Festival     |             45.47 min |
| Non-Festival |             26.12 min |

The analysis shows a substantial difference in average delivery time between festival and non-festival periods.

### Multiple Deliveries

The relationship between the number of deliveries assigned and delivery time was also analyzed.

| Multiple Deliveries | Average Delivery Time |
| ------------------- | --------------------: |
| 0                   |             23.03 min |
| 1                   |             26.96 min |
| 2                   |             34.59 min |
| 3                   |             48.22 min |

The analysis shows that **delivery time increases as the number of multiple deliveries increases**.

---

## 💡 Key Insights

### 1. Traffic + Weather

Heavy traffic combined with certain weather conditions is associated with longer delivery times.

The highest average delivery times in the analyzed combinations were:

* Jam + Fog → **36.89 minutes**
* Jam + Cloudy → **36.71 minutes**

### 2. Vehicle Condition

Vehicle condition is associated with differences in delivery time.

Vehicles with condition score 0 had an average delivery time of **30.25 minutes**, compared with approximately **24.6 minutes** for conditions 1 and 2.

### 3. Festival Periods

Festival days had an average delivery time of **45.47 minutes**, compared with **26.12 minutes** on non-festival days.

This represents an approximately **74% higher average delivery time** during festival periods.

### 4. Multiple Deliveries

The largest difference observed in the analysis was associated with multiple deliveries.

Average delivery time increased from **23.03 minutes** with zero additional deliveries to **48.22 minutes** with three deliveries.

This is approximately a **109% increase** in average delivery time.

---

## 📊 Dashboard

The Power BI dashboard provides interactive analysis of delivery time across:

* Delivery person age
* Delivery person rating
* Vehicle condition
* Festival status
* Multiple deliveries
* Traffic density
* Weather conditions

### Dashboard Filters

* Vehicle type
* Vehicle condition
* Weather condition

<img width="1321" height="748" alt="image" src="https://github.com/user-attachments/assets/0e7ce26f-be35-4b89-aa79-41ed521f7cfd" />



---

## 🛠️ Tools Used

**Excel**

* Data cleaning
* Data preparation
* Initial validation

**Power BI**

* Data visualization
* KPI analysis
* Interactive dashboard
* Business insight generation

---

## 📌 Business Takeaways

The analysis identifies several operational areas that may require further investigation:

* Review delivery stacking rules when multiple deliveries are assigned to one driver.
* Prepare additional delivery capacity during festival periods.
* Investigate vehicles with poor condition scores.
* Consider traffic and weather conditions when planning delivery operations.

These findings represent associations observed in the dataset and would require further operational data and testing before making causal decisions.

---

## 📄 Documentation

For the complete project methodology, data-cleaning details, analysis process, and dashboard documentation, see:

`documentation/project_documentation.pdf`

---

## 📚 Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis
* Business Question Formulation
* KPI Analysis
* Data Visualization
* Power BI
* Excel
* Business Insight Generation
