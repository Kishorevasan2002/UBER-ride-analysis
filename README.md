# 🚗 Uber Ride Analysis

This project analyzes Uber ride data to uncover trip patterns, cancellation trends, and factors influencing ride completion. The analysis includes data cleaning, exploratory data analysis (EDA), and data transformation to derive actionable insights.

---

## 📁 Dataset

The dataset is sourced from a CSV file and includes the following columns:

- Request, pickup, and drop timestamps  
- Pickup and drop locations  
- Trip cost and extra tip  
- Driver ID  
- Trip status (e.g., Completed, Cancelled, No Cars Available)  
- Ride type and payment method  
- Weather conditions  

---

## 📊 Analysis Highlights

### 🔹 Data Loading & Cleaning

- Loaded the dataset from a CSV file  
- Standardized column names  
- Handled missing values in `trip_status`, `trip_cost`, `payment_method`, and `driver_id`  
- Converted timestamp columns to datetime format  

### 🔹 Outlier Handling

- Identified and capped outliers in `trip_cost` using the IQR (Interquartile Range) method  

### 🔹 Exploratory Data Analysis (EDA)

- Reviewed dataset shape and data types  
- Analyzed distribution of trip statuses  
- Visualized trip cost and duration distributions  
- Compared trip costs across different payment methods  

### 🔹 Data Transformation

- Calculated total trip cost (`trip_cost + extra_tip`)  
- Extracted `date`, `day_of_week`, `time`, and `hour` from timestamps  
- Computed ride delays (difference between drop and start times)  
- Inferred cancellation reasons based on trip status and driver assignment  

### 🔹 Incomplete Rides Analysis

- Filtered incomplete rides (`Cancelled` or `No Cars Available`)  
- Analyzed proportions of incomplete ride statuses  
- Identified peak cancellation hours and days  
- Explored the impact of weather conditions on ride cancellations  

---

## 🧠 Key Findings

- Most frequent trip status  
- Peak hours/days for ride requests and cancellations  
- Common reasons for trip cancellations  
- Influence of weather on trip availability  

---

## 🚀 How to Reproduce

Follow these steps to reproduce the analysis:

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/uber-ride-analysis.git
   cd uber-ride-analysis
