# Olist E-commerce Sales & Customer Analysis

### [View the Interactive Dashboards on Tableau Public](https://public.tableau.com/shared/Z43NPKFBH?:display_count=n&:origin=viz_share_link)

## Project Overview

This project performs a comprehensive analysis of the Brazilian e-commerce market using the Olist dataset. The goal is to uncover actionable business insights into sales performance, customer behavior, and geographic market distribution.

The workflow begins with data cleaning, feature engineering, and predictive modeling in a Python Jupyter Notebook. The final, enriched datasets are then used to build a suite of interactive dashboards in Tableau, designed to provide key stakeholders with a clear overview of the business.

---

## Technologies Used

* **Data Analysis & Modeling:** Python (Pandas, Scikit-learn)
* **Data Visualization & Dashboards:** Tableau
* **Code Environment:** Jupyter Notebook

---

## Data Analysis & Modeling (Jupyter Notebook)

The `Olist_Analysis.ipynb` notebook handles the data processing and machine learning pipeline for the project.

#### 1. **Data Loading and Cleaning**
* Loaded all nine raw CSV files from the Olist dataset into Pandas DataFrames.
* Merged the disparate datasets into a single, cohesive master table.
* Handled missing values and converted columns to their correct data types (e.g., `datetime`).

#### 2. **Feature Engineering**
* **RFM Analysis:** Calculated Recency, Frequency, and Monetary values for each customer and used them to create segments like "Champions," "At Risk/Lost," and "New Customers."
* **Geographic Analysis:** Aggregated revenue and market share data at the state level.
* **Churn Prediction:** Engineered features relevant to predicting customer churn, such as customer tenure and payment behavior.

#### 3. **Predictive Modeling: Customer Churn**
* Built and evaluated a machine learning model to predict the likelihood of a customer churning.
* The model's predictions (`churn_probability`) were added back to the main DataFrame to be used in the Tableau dashboard.

#### 4. **Data Export**
* Exported the final, enriched datasets into clean CSV files, which serve as the data sources for the interactive dashboards.

---

## Data Visualization (Tableau Dashboards)

The Tableau workbook connects to the processed CSV files to present the findings through three key dashboards:

#### 1. **Geographic Sales Dashboard**
* **Purpose:** To provide an overview of sales performance and market dominance across Brazil.
* **Visualizations:** An interactive map color-coded by market share and a bar chart ranking states by total revenue.

#### 2. **RFM Customer Segmentation Dashboard**
* **Purpose:** To analyze the customer base by segmenting it using the RFM model.
* **Visualizations:** A bar chart showing the total number of customers in each segment and KPI cards highlighting key metrics.

#### 3. **Customer Lifetime Value (CLV) & Churn Analysis**
* **Purpose:** To visualize the future value of customers and identify segments with a high probability of churning.
* **Visualizations:** A headline KPI for estimated CLV and a chart categorizing customers into churn risk levels.

---

## How to Run This Project

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/Olist-E-commerce-Analysis.git](https://github.com/your-username/Olist-E-commerce-Analysis.git)
    cd Olist-E-commerce-Analysis
    ```

2.  **Install Dependencies:**
    Install the required Python libraries using the `requirements.txt` file.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Notebook:**
    Open and run the `Olist_Analysis.ipynb` notebook in Jupyter to perform the data analysis and generate the clean CSV files.

4.  **View the Dashboards:**
    Open the `.twbx` workbook file with Tableau Desktop or visit the live version on [Tableau Public](https://your-tableau-public-link-here).
