# Customer Segmentation Analysis

## Project Overview

Customer Segmentation Analysis is an e-commerce analytics project that identifies different groups of customers based on their purchasing behaviour.

The project uses **RFM Analysis (Recency, Frequency, Monetary)** and **K-Means Clustering** to divide customers into meaningful segments. These segments can help businesses understand customer behaviour and develop targeted marketing strategies.

## Objective

The main objectives of this project are:

* Clean and preprocess the e-commerce transaction dataset.
* Analyze customer purchasing behaviour.
* Calculate Recency, Frequency, and Monetary values.
* Apply feature standardization using `StandardScaler`.
* Determine the appropriate number of clusters using the Elbow Method.
* Apply K-Means clustering to segment customers.
* Profile and visualize the resulting customer segments.
* Develop marketing strategies for each customer segment.

## Dataset

The project uses the **Online Retail Dataset**.

### Dataset Columns

| Column      | Description                        |
| ----------- | ---------------------------------- |
| InvoiceNo   | Invoice number for the transaction |
| StockCode   | Product/item code                  |
| Description | Product description                |
| Quantity    | Number of items purchased          |
| InvoiceDate | Date and time of the transaction   |
| UnitPrice   | Price per item                     |
| CustomerID  | Unique customer identifier         |
| Country     | Customer's country                 |

## Data Preprocessing

The following preprocessing operations were performed:

* Loaded the CSV dataset using Pandas.
* Handled missing Customer IDs.
* Converted `InvoiceDate` into datetime format.
* Removed transactions with negative quantities.
* Removed transactions with zero or negative unit prices.
* Created a new `TotalAmount` column.

The transaction value was calculated as:

`TotalAmount = Quantity × UnitPrice`

## Exploratory Customer Analysis

The analysis calculated the following overall customer metrics:

| Metric                 |         Result |
| ---------------------- | -------------: |
| Total Customers        |          4,338 |
| Average Recency        |     92.06 days |
| Average Frequency      | 4.27 purchases |
| Average Monetary Value |       2,054.27 |

These metrics provide an overall understanding of customer purchasing behaviour.

## RFM Analysis

RFM analysis was used to create three behavioural features:

### Recency

Number of days since the customer's most recent purchase.

### Frequency

Number of unique invoices/purchases made by the customer.

### Monetary

Total amount spent by the customer.

A reference date of **10 December 2011** was used for calculating customer recency.

## Feature Standardization

The RFM features were standardized using:

* `StandardScaler`
* Python scikit-learn library

Standardization ensures that the three RFM variables can be compared effectively during clustering.

## K-Means Clustering

The **K-Means clustering algorithm** was used to segment customers.

The Elbow Method was applied to evaluate different values of K. Based on the analysis, **4 clusters** were selected.

The four customer segments are:

1. VIP Customers
2. Loyal Customers
3. Regular Customers
4. At-Risk Customers

## Customer Segment Profile

| Customer Segment  | Recency | Frequency |   Monetary | Customer Type                     |
| ----------------- | ------: | --------: | ---------: | --------------------------------- |
| VIP Customers     |    6.62 |     82.54 | 127,338.31 | Highest-value customers           |
| Loyal Customers   |   14.96 |     22.33 |  12,709.09 | Frequent and high-value customers |
| Regular Customers |   43.43 |      3.68 |   1,358.17 | Moderate-value customers          |
| At-Risk Customers |  248.17 |      1.55 |     478.19 | Low activity customers            |

## Customer Segment Insights

### VIP Customers

VIP customers have the highest purchase frequency and monetary value. They have also purchased very recently.

**Marketing Action:**
Provide exclusive rewards, premium offers, loyalty benefits, and personalized experiences.

### Loyal Customers

Loyal customers purchase frequently and generate high monetary value. Their recent purchasing activity indicates strong engagement.

**Marketing Action:**
Use personalized promotions, loyalty programs, and repeat-purchase incentives.

### Regular Customers

Regular customers show moderate purchasing frequency and spending.

**Marketing Action:**
Use targeted discounts, product recommendations, and promotional campaigns to increase purchase frequency.

### At-Risk Customers

At-risk customers have a long period since their last purchase, low purchase frequency, and low monetary value.

**Marketing Action:**
Use re-engagement emails, special discounts, reminders, and win-back campaigns.

## Visualizations

The project includes the following visualizations:

* Elbow Method for determining the optimal number of clusters
* Recency vs Monetary customer segmentation scatter plot
* Frequency vs Monetary customer segmentation scatter plot
* Customer count by segment
* Customer segment percentage distribution

## Key Insights

* Customers can be effectively grouped according to their purchasing behaviour.
* VIP customers contribute significantly higher monetary value than other segments.
* Loyal customers demonstrate strong repeat purchasing behaviour.
* Regular customers represent an opportunity for increasing purchase frequency.
* At-risk customers require re-engagement strategies to encourage them to return.
* Customer segmentation allows businesses to use different marketing strategies for different customer groups.

## Business Recommendations

Businesses can use these segments to create targeted marketing campaigns:

| Segment           | Recommended Strategy                               |
| ----------------- | -------------------------------------------------- |
| VIP Customers     | Exclusive rewards and premium loyalty benefits     |
| Loyal Customers   | Personalized offers and repeat-purchase incentives |
| Regular Customers | Targeted promotions and cross-selling              |
| At-Risk Customers | Win-back campaigns and re-engagement offers        |

## Technologies Used

* **Python**
* **Pandas**
* **Scikit-learn**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

## Project Files

* `Customer_Segmentation_Analysis.ipynb` — Complete Python analysis and visualizations
* `OnlineRetail.csv` — Dataset used for analysis
* `Customer_Segmentation_Results.csv` — Final customer segmentation results
* `README.md` — Project documentation

## Conclusion

This project demonstrates how customer purchasing behaviour can be analyzed using RFM analysis and K-Means clustering.

The analysis identified four meaningful customer groups: **VIP, Loyal, Regular, and At-Risk customers**. Each segment has different purchasing characteristics and therefore requires a different marketing approach.

Customer segmentation can help businesses improve customer engagement, personalize marketing campaigns, strengthen customer loyalty, and identify opportunities for customer retention.

## Author

**Monika**

Customer Segmentation Analysis — Data Analytics Project
