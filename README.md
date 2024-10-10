# Data Analyst - Customer Segmentation Project

## Goal of the Project:
The aim of this project is to perform a **Customer Segmentation Analysis** for an automobile bike company using the **RFM (Recency, Frequency, Monetary)** model. RFM analysis is a behavior-based approach that groups customers based on their purchasing patterns. In this analysis, the customer base is segmented into 11 distinct groups, allowing the company to better understand customer behavior and prioritize segments for targeted marketing.

## Key Components:

### 1. Data Quality Assessment and Analysis (DQA):
The data assessment and cleaning process is carried out using Python to ensure the accuracy and consistency of customer transaction data. This includes preparing customer demographics, transaction histories, and other relevant datasets for analysis.

### 2. RFM Model for Customer Segmentation:
- **Recency**: How recently a customer made a purchase.
- **Frequency**: How often a customer makes purchases.
- **Monetary Value**: How much a customer spends.

Based on these factors, customers are segmented into 11 groups to understand their purchasing behavior and potential value to the company.

### 3. Sales Dashboard for Customer Segmentation (using Python):
A comprehensive sales dashboard is developed entirely in Python to visualize the customer segments, their distribution, and their revenue impact. This dashboard allows stakeholders to easily interpret the data and make informed decisions about which customer segments to focus on to maximize sales revenue.

### Jupyter Notebooks:
If you're unable to load the Jupyter Notebooks on GitHub, you can view them on nbviewer by clicking the respective links:
- [RFM Analysis.ipynb](https://github.com/SUGANGOLD/Data-Analyst-Customer-Segmentation/blob/main/RFM%20Analysis.ipynb)
- [Data Cleaning CustomerDemographic.ipynb](https://github.com/SUGANGOLD/Data-Analyst-Customer-Segmentation/blob/main/Data%20Cleaning%20CustomerDemographic.ipynb)
- [Data Cleaning NewCustomerList.ipynb](https://github.com/SUGANGOLD/Data-Analyst-Customer-Segmentation/blob/main/Data%20Cleaning%20NewCustomerList.ipynb)
- [DQA and Data Cleaning Transactions.ipynb](https://github.com/SUGANGOLD/Data-Analyst-Customer-Segmentation/blob/main/Data%20Cleaning%20Transactions.ipynb)
- [Data Cleaning Customer Address.ipynb](https://github.com/SUGANGOLD/Data-Analyst-Customer-Segmentation/blob/main/Data%20Cleaning%20Customer%20Address.ipynb)

## Analysis Approach:

### 1. Data Quality Assessment and Data Cleaning:
The first step was data preparation, quality assessment, and cleaning. After cleaning, exploratory data analysis (EDA) on customer purchasing behavior was performed to generate insights.

#### Datasets and Observations:
- **CustomerDemographics.xlsx**:
  - One irrelevant column was dropped.
  - Missing values were handled by dropping records or imputing values where appropriate.
  - The gender column was standardized to remove inconsistencies.
  - A new column 'Age' was created from the Date of Birth.
  - Outliers in age distribution were removed.
  
- **NewCustomerList.xlsx**:
  - Five irrelevant columns were dropped.
  - Missing values were handled, and the 'Age' column was derived.
  - No inconsistencies or duplicates were found.

- **Transaction_data.xlsx**:
  - 'Product_first_sold_date' was converted to datetime.
  - Seven columns had missing values, handled appropriately.
  - A new 'Profit' column was created (difference between list price and standard price).

- **CustomerAddress.xlsx**:
  - The 'State' column was standardized.
  - Some customer IDs were dropped due to inconsistencies in the address data.

### 2. Exploratory Data Analysis on Customer Segments:
After cleaning, the following insights were obtained:

- **New vs Old Customers Age Distribution**:
  - Most new and old customers fall within the 40-49 age range.
  - The company is popular among new customers in the 20-29 and 40-49 age groups.
  
  <table>
    <tr>
      <td><b>Old Customers Age Distribution</b></td>
      <td><b>New Customers Age Distribution</b></td>
    </tr>
    <tr>
      <td><img src="/data visualization/Old Customer - Age Distribution.png" height="400" alt="Old Customers Age Distribution"></td>
      <td><img src="/data visualization/New Customers - Age Distribution.png" height="400" alt="New Customers Age Distribution"></td>
    </tr>
  </table>

- **Bike Purchases by Gender**:
  - Approximately 51% of bike purchases over the last 3 years were made by females.
  <img src="/data visualization/Female vs Male past 3 years Bike Purchases.png" height="400" alt="Bike Purchases by Gender">

- **New vs Old Customers Job Industry**:
  - Most customers are from the manufacturing and financial services sectors.
  <table>
    <tr>
      <td><b>Old Customers Job Industry</b></td>
      <td><b>New Customers Job Industry</b></td>
    </tr>
    <tr>
      <td><img src="/data visualization/Old Customers - Job Industry Customer Distribution.png" height="400" alt="Old Customers Job Industry"></td>
      <td><img src="/data visualization/New Customers - Job Industry Customer Distribution.png" height="400" alt="New Customers Job Industry"></td>
    </tr>
  </table>

- **Wealth Segmentation by Age Category**:
  - The 'Mass Customer' segment dominates across all age groups.
  <table>
    <tr>
      <td><b>Old Customers Wealth by Age Group</b></td>
      <td><b>New Customers Wealth by Age Group</b></td>
    </tr>
    <tr>
      <td><img src="/data visualization/Old Customers - Wealth Segmentation by Age Group.png" height="400" alt="Old Customers Wealth Segment"></td>
      <td><img src="/data visualization/New Customers - Wealth Segmentation by Age Group.png" height="400" alt="New Customers Wealth Segment"></td>
    </tr>
  </table>

- **Cars Owned by State**:
  - New South Wales has the largest number of non-car owners.
  <img src="/data visualization/Number of Customers who own a car.png" height="400" alt="Car Owners by State">

### 3. RFM Analysis and Customer Segmentation:
The RFM (Recency, Frequency, Monetary) model grouped customers into 11 segments:
- Platinum Customers
- Very Loyal Customers
- Recent Customers
- Potential Customers
- Lost Customers
- Losing Customers
- Late Bloomers
- High-Risk Customers
- Evasive Customers
- Becoming Loyal
- Almost Lost Customers

The current distribution of customer segments:
<img src="/data visualization/Number of Customers by Customer Segment.png" height="400" alt="Customer Segment Distribution">

### 4. RFM Analysis: Scatter Plots:
#### Recency vs Monetary:
Recent customers tend to generate more revenue.
<img src="/data visualization/Recency vs Monetary.png" height="400" alt="Recency vs Monetary">

#### Frequency vs Monetary:
Loyal customers show a higher purchase frequency and monetary value.
<img src="/data visualization/Frequency vs Monetary.png" height="400" alt="Frequency vs Monetary">

## Datasets Used:
The datasets used include:
- **Raw_data.xlsx** (with the following sheets):
  - **Transactions_data.xlsx**: Transactions data across states in Australia.
  - **NewCustomerList.xlsx**: Recent customers visiting the automobile company.
  - **CustomerDemographic.xlsx**: Customer demographic details.
  - **CustomerAddress.xlsx**: Customer addresses.

## Tools and Technologies Used:
- **Python**: Used for Data Quality Assessment, Data Cleaning, and Exploratory Data Analysis with libraries like `pandas`, `matplotlib`, and `seaborn`.

## Built With:
- Python 3.12.6

## Author:
- **Sugan** - [GitHub Profile](https://github.com/SUGANGOLD)
