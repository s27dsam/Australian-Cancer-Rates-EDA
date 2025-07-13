# Exploratory Data Analysis of Australian Cancer Rates

This repository contains a Jupyter Notebook detailing an exploratory data analysis (EDA) on a simulated dataset of Australian cancer rates. The primary goal of this project is to uncover initial insights, identify patterns, and check for data quality issues before any predictive modeling.

## 🚀 Project Overview

The analysis explores the relationships between various patient attributes and cancer-related outcomes. It is divided into several key sections:

-   **Data Loading and Inspection**: Initial loading of the dataset with PySpark and a first look at the schema and data structure.
-   **Descriptive Statistics**: Summary statistics for both numerical and categorical features to understand their distributions.
-   **Data Quality Check**: An analysis of missing or null values to identify potential data cleaning needs.
-   **Visualizations**: A comprehensive suite of plots to visualize distributions, relationships, and trends within the data, including:
    -   Histograms and box plots for numerical features like `Age` and `BMI`.
    -   Bar charts showing survival rates by `Cancer_Type`.
    -   A correlation heatmap to identify relationships between numerical variables.
    -   Violin plots to compare distributions across different categories (e.g., `Tumor_Size_cm` by `Stage`).
    -   Geographic and lifestyle factor analysis.
-   **Statistical Analysis**: A t-test to check for statistically significant differences between groups (e.g., smokers vs. non-smokers).
-   **Time-Based Analysis**: A look at trends over the `Diagnosis_Year`.

## 🛠️ Technologies & Libraries Used

-   **Language**: Python
-   **Core Libraries**:
    -   `PySpark`: For handling and processing the data in a distributed manner.
    -   `Pandas`: For data manipulation on the sampled data for visualization.
    -   `Matplotlib` & `Seaborn`: For generating a wide range of static visualizations.
    -   `SciPy`: For statistical testing.

## 📋 How to Use

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/your-username/Australian-Cancer-Rates-EDA.git](https://github.com/your-username/Australian-Cancer-Rates-EDA.git)
    ```
2.  **Ensure you have the required environment**: A local Spark installation or a cloud-based environment (like Databricks or Google Colab) configured for PySpark is required.
3.  **Install dependencies**:
    ```bash
    pip install pyspark pandas matplotlib seaborn scipy
    ```
4.  **Launch Jupyter Notebook**:
    ```bash
    jupyter notebook Aus_Cancer_EDA.ipynb
    ```
5.  **Run the cells** in the notebook sequentially to reproduce the analysis. Make sure the `cancer_rates_australia.csv` dataset is in the same directory.

## 🔍 Key Findings from the EDA

-   The dataset is well-balanced across different states and genders, with no missing values.
-   The initial analysis of `Tumor_Size_cm` identified a potential data quality issue with a minimum value of -1.55, which would need to be addressed before modeling.
-   Survival rates vary significantly across different cancer types.
-   There is no strong linear correlation between the primary numerical features (`Age`, `Tumor_Size_cm`, `BMI`, `Survival_Years`).
-   The t-test indicates that the difference in BMI between smokers and non-smokers in this dataset is not statistically significant.
