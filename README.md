# Exploratory Data Analysis on Google Play Store Dataset 📊

This repository contains a detailed Exploratory Data Analysis (EDA) and feature engineering project on the Google Play Store dataset. The goal is to clean a messy real-world dataset and derive meaningful insights through data visualization.

## 📋 Dataset

The dataset used is the popular "Google Play Store Apps" dataset, sourced from Kaggle. It contains details for over 10,000 apps with 13 distinct features, including:

* App Name & Category
* Rating & Number of Reviews
* Size & Number of Installs
* Type (Free/Paid) & Price
* Content Rating & Genres

## ⚙️ Key Steps & Analysis

The project follows a structured approach to analyze the data:

### 1. Data Cleaning & Preprocessing 🧹
* **Corrected Data Types:** Columns like `Reviews`, `Size`, `Installs`, and `Price` were loaded as text objects and were converted to appropriate numerical types (`int`, `float`).
* **Handled Special Characters:** Removed characters like `+`, `,`, `$`, `M`, and `k` from numerical columns to allow for proper computation.
* **Addressed Inconsistent Data:** Replaced the "Varies with device" value in the `Size` column with NaN to be handled later.
* **Removed Erroneous Rows:** Identified and dropped a row where data was shifted across columns, causing data type errors.
* **Duplicate Handling:** Removed duplicate entries based on the 'App' name, keeping the first occurrence.

### 2. Feature Engineering 🛠️
* **Date Extraction:** The `Last Updated` column was converted to a datetime object.
* **New Time-Based Features:** New columns `Day`, `Month`, and `Year` were created from the `Last Updated` column to enable time-based analysis.

### 3. Exploratory Data Analysis (EDA) 📈
* **Category Distribution:** Visualized the distribution of apps across different categories, revealing that **Family** and **Game** categories have the highest number of apps.
* **Most Installed Categories:** Analyzed the total number of installs per category, finding that **Game** and **Communication** apps are the most popular by a large margin.
* **Top Installed Apps:** Identified the top 5 most installed apps within the most popular categories (GAME, COMMUNICATION, PRODUCTIVITY, SOCIAL).
* **App Type & Content Rating:** Analyzed the distribution of Free vs. Paid apps and the target audience through Content Rating visualizations.

## 💡 Key Insights

* **Most Crowded Categories:** The **Family** (18.2%) and **Game** (9.6%) categories are the most saturated with apps.
* **Highest User Reach:** The **Game** and **Communication** categories dominate installations, indicating the highest user engagement.
* **Top Performers:** Apps like **Subway Surfers**, **Instagram**, and **Google Drive** are the most installed apps in their respective categories.
* **Market Dynamics:** Over **92%** of the apps on the Play Store are **Free**.
* **Target Audience:** A vast majority of apps (~80%) are rated for **"Everyone"**, highlighting a focus on a broad user base.

## 🚀 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

## 🚀 How to Run

1.  Clone this repository:
    ```bash
    git clone [https://github.com/your-username/Google-Playstore-Data-EDA.git](https://github.com/your-username/Google-Playstore-Data-EDA.git)
    ```
2.  Install the required libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
3.  Open and run the `Google_Plystore_Data_EDA.ipynb` file in Jupyter Notebook or Jupyter Lab.
