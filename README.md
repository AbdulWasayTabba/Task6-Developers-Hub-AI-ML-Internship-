# Task6-Developers-Hub-AI-ML-Internship-
# House Price Prediction - Feature Selection and Outlier Handling

## 📌 Project Overview
This project focuses on predicting house prices using a subset of highly influential features from the standard Housing Prices dataset. Developed as part of my journey through the "100 Days of ML" challenge (inspired by CampusX), this notebook (`task6.ipynb`) demonstrates practical implementations of essential data science steps, including data loading, exploratory data analysis (EDA), feature selection, data clipping (outlier handling), and model performance visualization.

## 📊 Dataset
The dataset used in this project is the classic **House Prices dataset** (`train.csv`). It contains various attributes of houses and their corresponding sale prices. 

* **Original Shape:** 1460 rows and 81 columns.
* **Target Variable:** `SalePrice`

## 🔑 Key Features Selected
To simplify the model and focus on the most impactful metrics, the following 10 columns were isolated from the original dataset:
* `OverallQual` - Overall material and finish quality
* `GrLivArea` - Above grade (ground) living area square feet
* `GarageCars` - Size of garage in car capacity
* `GarageArea` - Size of garage in square feet
* `TotalBsmtSF` - Total square feet of basement area
* `FullBath` - Full bathrooms above grade
* `YearBuilt` - Original construction date
* `1stFlrSF` - First Floor square feet
* `TotRmsAbvGrd` - Total rooms above grade (does not include bathrooms)
* `SalePrice` - The property's sale price in dollars (Target)

## 🧹 Data Preprocessing & Outlier Handling
To make the model more robust and prevent extreme values from skewing the regression, data clipping was applied to cap outliers:
* **GrLivArea:** Clipped at a maximum of `3700` sq. ft.
* **GarageCars:** Capped at `3` cars.
* **GarageArea:** Clipped to fall within the range of `100` to `1200` sq. ft.
* **TotalBsmtSF:** Capped at `3000` sq. ft.
* **1stFlrSF:** Capped at `3000` sq. ft.
* **TotRmsAbvGrd:** Capped at `12` rooms.

## 📈 Visualization
The notebook concludes by visualizing the model's accuracy. A scatter plot is generated using `matplotlib` to compare the **Actual SalePrice** (Blue) against the **Predicted SalePrice** (Green), helping to visually assess the regression model's performance and variance.

## 💻 Dependencies
To run this notebook successfully, you will need the following Python libraries installed:
* `pandas`
* `matplotlib`
* `scikit-learn`

You can install the dependencies using pip:
```bash
pip install pandas matplotlib scikit-learn
