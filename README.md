# Customer Segmentation using RFM Analysis

This project provides a comprehensive implementation of customer segmentation using **Recency, Frequency, and Monetary (RFM) analysis**. It utilizes a real-world retail dataset to categorize customers into distinct segments based on their purchasing behavior (how recently they purchased, how often they purchase, and how much they spend).

The goal of this analysis is to provide actionable insights for businesses to tailor marketing, improve customer retention, and enhance customer relationship strategies based on individualized segments.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Methodology](#methodology)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

---

## Project Overview

This repository contains the code for a detailed study on RFM-based customer segmentation. The approach combines statistical analysis, data visualization, and machine learning. The code walks through the entire process, from cleaning raw data to defining interpretable customer segments and, finally, explores the use of ML models to automate the segmentation.

## Methodology

The analysis follows a structured workflow:

1.  **Data Preparation:** The raw dataset is loaded, explored, and cleaned to ensure data integrity. This includes addressing issues like negative quantities and handling missing customer identifiers.
2.  **RFM Metric Calculation:** The three core metrics are computed for each customer:
    * **Recency:** Days since the customer's last purchase.
    * **Frequency:** Total number of transactions made by the customer.
    * **Monetary:** Total monetary value of the customer's purchases.
3.  **Quantile-Based Scoring:** Customers are scored on a 1-4 scale for each RFM metric based on quantiles. This allows for a granular and relative ranking.
4.  **Segmentation:** A combined RFM score is created, and rule-based logic is applied to define distinct, interpretable customer segments.
5.  **Visualization:** The distributions of the RFM metrics and the final customer segments are visualized using violin plots, histograms, and pie charts for clear interpretation.
6.  **Predictive Modeling (Experimental):** The project includes a (commented-out) framework for using machine learning models (`XGBClassifier`, `CatBoostClassifier`) to predict customer segments based on their RFM metrics.

## Key Features

* **Data Cleaning:** Robust preprocessing to handle common issues in retail data.
* **RFM Calculation:** Clear and accurate computation of Recency, Frequency, and Monetary metrics.
* **Quantile Segmentation:** A statistical method for segmenting customers into four distinct groups for each RFM metric.
* **Interpretable Segments:** Defines clear, rule-based segments such as:
    * Best Customer
    * Loyal Customer
    * Big Spender
    * Dead Beats
    * Lost Customer
* **Rich Visualization:** Uses `matplotlib` and `seaborn` to provide intuitive visualizations of customer behavior and segment distribution.
* **Machine Learning Integration:** Provides a foundation for automating segmentation and predictive analytics (XGBoost, CatBoost).

## Technology Stack

* **Python 3.x**
* **Pandas:** For data manipulation and analysis.
* **NumPy:** For numerical operations.
* **Matplotlib & Seaborn:** For data visualization.
* **Scikit-learn (sklearn):** For preprocessing and ML utilities.
* **XGBoost:** For the `XGBClassifier` model (experimental).
* **CatBoost:** For the `CatBoostClassifier` model (experimental).
* **Jupyter Notebook:** As the environment for the analysis.

---

## Installation

1.  Clone the repository to your local machine:
    ```sh
    git clone [https://github.com/your-username/Customer-Segmentation-using-RFM-Analysis.git](https://github.com/your-username/Customer-Segmentation-using-RFM-Analysis.git)
    cd Customer-Segmentation-using-RFM-Analysis
    ```

2.  Install the required Python libraries. It is highly recommended to use a virtual environment.
    ```sh
    pip install -r requirements.txt
    ```
    *(Note: You can create a `requirements.txt` file by running `pip freeze > requirements.txt` in your project's environment.)*

## Usage

1.  Place your dataset (e.g., `retail_data.csv`) in the root directory of the project.
2.  Open and run the Jupyter Notebook (`RFM_Analysis.ipynb`).
3.  Follow the steps in the notebook to see the complete process, from data loading and cleaning to the final visualization of customer segments.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
