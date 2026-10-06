# ✈️ Flight Price Prediction

A machine learning project that predicts **flight ticket prices** based on factors such as airline, source, destination, number of stops, journey duration, booking time, and seat class.

## 📌 Project Overview

Flight prices can change significantly depending on different travel and booking factors.

The goal of this project is simple:

> **Can we use machine learning to predict flight ticket prices from available flight information?**

The project focuses on preparing real-world flight data, creating useful features, and comparing regression models to build a better price prediction solution.

## 🔍 What I Did

* Explored the flight price dataset
* Checked data types and basic statistics
* Cleaned and prepared the data
* Performed feature engineering on:

  * Journey date
  * Arrival time
  * Departure time
  * Flight duration
  * Number of stops
* Converted categorical features using **One-Hot Encoding**
* Removed unnecessary columns
* Split the dataset into **80% training and 20% testing**
* Applied **StandardScaler** to numerical features
* Built and evaluated:

  * Linear Regression
  * Random Forest Regression
* Compared model performance using:

  * MAE
  * MSE
  * RMSE
  * R² Score
* Used **RandomizedSearchCV** to tune the Random Forest model

## 📊 Key Features

The dataset includes information such as:

* **Airline** – Airline company
* **Flight** – Flight code
* **Source** – Departure city
* **Destination** – Arrival city
* **Departure Time** – Departure hour and minutes
* **Arrival Time** – Arrival hour and minutes
* **Total Stops** – Number of stops
* **Class** – Business or Economy
* **Duration** – Total journey duration
* **Days Left** – Days between booking and journey
* **Price** – Target variable

## 🛠️ Feature Engineering

Several raw features were transformed into model-friendly variables.

For example:

```text
Date of Journey
       ↓
Day + Month + Year

Departure Time
       ↓
Departure Hour + Departure Minutes

Arrival Time
       ↓
Arrival Hour + Arrival Minutes

Duration
       ↓
Duration Hours + Duration Minutes
```

Categorical features such as **Airline, Source, and Destination** were converted into numerical values using **One-Hot Encoding**.

## 🤖 Machine Learning Models

### Linear Regression

Used as a baseline regression model to understand the relationship between flight features and ticket price.

### Random Forest Regression

A Random Forest model was trained to capture more complex relationships between flight characteristics and ticket prices.

### Hyperparameter Tuning

**RandomizedSearchCV** with 5-fold cross-validation was used to search for better Random Forest parameters.

## 📈 Model Evaluation

The models were evaluated using:

**MAE — Mean Absolute Error**
Measures the average difference between actual and predicted prices.

**MSE — Mean Squared Error**
Penalizes larger prediction errors more heavily.

**RMSE — Root Mean Squared Error**
Shows the typical prediction error in the same unit as ticket price.

**R² Score**
Measures how well the model explains variations in flight prices.

The notebook also uses actual-vs-predicted plots and residual distributions to visually evaluate model performance.

## 💡 Key Takeaway

This project demonstrates how **data cleaning, feature engineering, categorical encoding, scaling, regression modeling, and hyperparameter tuning** can be combined to build a practical flight price prediction system.

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## 🎯 What This Project Demonstrates

* Exploratory data analysis
* Data cleaning
* Feature engineering
* Categorical encoding
* Feature scaling
* Regression modeling
* Model evaluation
* Hyperparameter tuning
* Practical machine learning workflow
