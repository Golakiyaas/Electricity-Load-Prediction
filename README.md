# ⚡ **Electricity-Load-Prediction** ⚡

## 🚀 Introduction

Welcome to the **Electricity-Load-Prediction** project! This project aims to provide data-driven policy recommendations for the efficient use of renewable energy sources and the optimization of energy infrastructure in **Valencia, Spain**. By analyzing and forecasting energy consumption patterns through multiple datasets, this project helps uncover valuable insights into energy load trends and provides the tools necessary for effective decision-making.

### 🎯 **Main Goal**:
- Predict electricity consumption to improve energy management.
- Provide visualizations of energy data trends.
- Offer insights into peak energy demand for policy recommendations.

---

## 🔧 Features

- **Data Preprocessing**: Clean, format, and prepare raw energy data for analysis.
- **Exploratory Data Analysis**: Investigate distributions and characteristics of energy consumption.
- **Visualization**: Generate insightful plots to visualize energy consumption over time.
- **Analysis**: Perform in-depth analysis of energy data, including peak load detection and timestamp-based analysis.
- **Forecasting**: Predict future energy consumption with state-of-the-art forecasting models.
- **Reports**: Generate comprehensive and clear reports based on the analysis.

---

## 📥 Installation

To get started, follow these simple steps:

1. **Clone the repository**:

    ```bash
    git clone https://github.com/Golakiyaas/Electricity-Load-Prediction.git
    ```

2. **Navigate to the project directory**:

    ```bash
    cd Electricity-Load-Prediction
    ```

3. **Install required dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

---

## 📝 Usage

Once you have the project set up, open the `main.ipynb` notebook and execute the cells to run the analysis. Make sure all datasets are in the correct directory.

Each section of the notebook comes with detailed comments, explaining the steps and providing visualizations for better understanding.

---

## 📊 Datasets

### 1. **energy_dataset.csv**
This dataset contains detailed information on energy consumption, including timestamps, energy loads, and other relevant features. 

### 2. **df_combined.csv**
A combination of multiple datasets, offering a comprehensive overview of energy data over a specified period.

### 3. **Maximum_Load_Per_Day_with_Timestamps.csv**
Tracks the maximum energy load for each day with corresponding timestamps, helping identify peak consumption periods.

---

## 🔍 Exploratory Analysis & Data Cleaning

### 🧹 **Handling Missing & Duplicate Values**

- **Duplicate Values**: There were no duplicate values found in the dataset, but some missing values (`NaN`) were present.
- **Missing Values**: The 'total load actual' column contained the majority of missing values. Since this is time-series data, instead of removing rows with missing values, we used **linear interpolation** to fill in the gaps.

### 📈 **Visualizations & Distribution**

We used **violin plots** to analyze data distributions and understand the energy consumption patterns. The `.info()` method was also employed to investigate the type of values and the count of null/non-null values.

---

## 🧠 Modelling Process

We tried several machine learning models including **ARIMA**, **Auto-ARIMA**, **SARIMAX**, **Prophet**, **XGBoost**, and **Random Forest Regressor (RFR)**. Based on evaluation metrics such as R², we proceeded with **XGBoost** and **RFR** for forecasting energy consumption.

Additionally, we filtered out the maximum energy load per day from the 'total load actual' column for further analysis and prediction.

---

## 📊 Examples

Here are some examples of the visualizations and analyses you can generate using this project:

### 📈 Energy Load Over Time

```python
import matplotlib.pyplot as plt
import pandas as pd

# Load data
df = pd.read_csv('energy_dataset.csv')

# Plot energy load over time
df.plot(x='timestamp', y='load', title='Energy Load Over Time')
plt.show()
```

### 📊 Maximum Load Per Day

```python
df_max_load = pd.read_csv('Maximum_Load_Per_Day_with_Timestamps.csv')

# Plot maximum load per day
df_max_load.plot(x='date', y='max_load', kind='bar', title='Maximum Load Per Day')
plt.show()
```

---

## 🖤 **Thank You!** 🖤

Thank you for checking out the **Electricity-Load-Prediction** project!  
If you found it useful, please ⭐ star the repository on GitHub.

💬 **Feel free to**:
- Fork the project.
- Contribute improvements.
- Open issues or suggest new features.
- Stay tuned for future updates and improvements! 🔥

---

## 🤝 **Contributing**

We welcome contributions from the community! If you'd like to contribute, please fork the repository and submit a pull request.
---
---
