# A/B Testing Project

This project aims to conduct an A/B test using the "Online Retail Dataset" from the UCI Machine Learning Repository. The objective is to analyze the impact of a treatment (e.g., a new website design) on customer spending.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Setup](#setup)
- [Data Preprocessing](#data-preprocessing)
- [A/B Test Design](#ab-test-design)
- [Analysis](#analysis)
- [Conclusion](#conclusion)
- [Results](#results)
- [License](#license)

## Introduction
A/B testing is a statistical method used to compare two groups to determine if there is a significant difference between them. In this project, we perform an A/B test to evaluate the effect of a treatment on the total amount spent by customers.

## Dataset
The dataset used in this project is the "Online Retail Dataset" from the UCI Machine Learning Repository. It contains transactional data from a UK-based online retail store.

- [Online Retail Dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/00352/Online%20Retail.xlsx)

## Setup
To run this project, follow these steps:

1. Clone this repository:

2. Install the required libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn scipy
    ```

3. Open the Jupyter Notebook or Google Colab to execute the code.

## Data Preprocessing
The data preprocessing steps include:
- Removing rows with missing `CustomerID`
- Filtering transactions for UK customers
- Converting `InvoiceDate` to datetime format
- Adding a `TotalAmount` column (Quantity * UnitPrice)

## A/B Test Design
The A/B test involves:
- Randomly assigning customers to either the control group (A) or treatment group (B)
- Calculating the total amount spent by each customer
- Comparing the mean and standard deviation of total spending between the two groups

## Analysis
We use an independent t-test to determine if there is a statistically significant difference between the control and treatment groups.

## Conclusion
Based on the analysis, we interpret the results to determine if the treatment had a significant impact on customer spending.

## Results
### Descriptive Statistics
- **Mean Total Amount (Control):** 901.44
- **Std Total Amount (Control):** 4660.87
- **Mean Total Amount (Treatment):** 837.53
- **Std Total Amount (Treatment):** 4254.27

### Inferential Statistics
- **T-statistic:** 0.6318
- **P-value:** 0.5276

### Interpretation
The difference in mean spending between the control and treatment groups is not statistically significant (p-value > 0.05). Therefore, the treatment did not have a significant impact on customer spending.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
