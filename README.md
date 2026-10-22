# PharmaPulse-Pharmaceutical Sales Analytics

## Project Overview

PharmaPulse is a pharmaceutical sales analytics project developed in Databricks to explore historical sales patterns, identify changes in sales performance, and understand how recorded sales are distributed across medicine categories and hours of the day.

Using PySpark and Databricks, I performed data exploration, calculated key performance indicators (KPIs), analyzed year-over-year (YoY) changes, and built visualizations to communicate findings.

The project demonstrates practical skills in data preparation, aggregation, trend analysis, data quality awareness, and business intelligence reporting.

## Business Questions

- How did recorded pharmaceutical sales change over time?
- Which medicine categories contributed the most to total recorded sales?
- Which years experienced the largest increases or decreases?
- How did the sales mix across medicine categories change?
- At what hours were the highest recorded sales observed?
- What data limitations should be considered before making business decisions?

## Tools and Technologies

- **Databricks:** Data analysis environment and dashboard development
- **PySpark:** Data processing, aggregations, and calculations
- **Python:** Analytical workflow and data manipulation
- **Delta tables:** Storage of the prepared annual dashboard dataset
- **Databricks visualizations:** Trend analysis and KPI reporting

## Dataset

The project uses historical pharmaceutical sales data organized into daily, hourly, weekly, and monthly tables.

The hourly dataset contains **50,532 records** spanning **2,106 distinct dates**, with observations covering 2014 through October 2019.

The medicine category columns analyzed are:

- `M01AB`
- `M01AE`
- `N02BA`
- `N02BE`
- `N05B`
- `N05C`
- `R03`
- `R06`

A total recorded sales measure was calculated by summing the eight medicine category values for each record.

**Data limitation:** The available dataset does not establish a currency, so the figures are described as recorded sales rather than revenue or profit.

## Analysis and Methodology

### 1. Data Exploration and Quality Checks

- Examined the available tables and column structures.
- Checked the sales category fields used in the analysis.
- Investigated records with zero recorded sales.
- Reviewed the time coverage of the dataset.
- Identified the incomplete 2019 period as a limitation for annual comparisons.

### 2. KPI Analysis

Calculated key summary metrics from the hourly dataset:

| Metric | Result |
|---|---:|
| Total records | 50,532 |
| Total recorded sales | 127,595.50 |
| Average sales per record | 2.53 |
| Distinct dates | 2,106 |

The average includes records with zero recorded sales.

### 3. Time-Series Analysis

Analyzed monthly and annual sales patterns to identify changes over time. Calculated year-over-year growth and decline percentages and compared the performance of medicine categories across years.  <br/>
 <br/>
  <br/>
### The Monthly sales trend  <br/>
 <img width="921" height="382" alt="image" src="https://github.com/user-attachments/assets/f83b3e19-1394-41e6-8b2b-e709e12f1ed6" />  <br/>
 <br/>
  <br/>
### The year-over-year growth Trend  <br/>
 <img width="1067" height="524" alt="image" src="https://github.com/user-attachments/assets/98c5187f-30c3-4570-a177-bc73c2c05d41" />

### 4. Medicine Category Analysis

Calculated category totals and percentage contributions to understand the composition of recorded sales and identify categories with the largest contributions.

<img width="695" height="400" alt="image" src="https://github.com/user-attachments/assets/0ee861d3-31ff-4e7c-bb54-dd749fafb403" />

### 5. Hourly Sales Analysis

Aggregated recorded sales by hour to identify periods with higher and lower recorded activity.

### 6. Dashboard Development

Created a Databricks dashboard containing sales trends, annual comparisons, category contribution charts, and supporting tables.

## Key Findings

### 1. Sales Were Concentrated in Two Medicine Categories

`N02BE` contributed approximately **49.38%** of total recorded sales, while `N05B` contributed approximately **14.61%**. Together, these categories accounted for approximately **64%** of the recorded total.

### 2. Recorded Sales Declined Substantially in 2017

Total recorded sales decreased by approximately **23.12%** in 2017 compared with 2016.

This decline is a signal for further investigation; the dataset alone does not explain its cause.

### 3. Recorded Sales Recovered in 2018

Total recorded sales increased by approximately **17.97%** in 2018 compared with 2017. However, the 2018 total remained below the 2016 peak.

### 4. R03 Recorded Strong Growth in 2018

Recorded sales for `R03` increased by approximately **40.22%** in 2018 compared with 2017, making it an interesting category for further analysis.

### 5. Evening Hours Showed High Recorded Sales

Across the hourly dataset, **19:00 (7 PM)** had the highest aggregate recorded sales among the observed hours, at approximately **11,322**.

This describes the dataset's recorded pattern and does not establish why it occurred.

## Business Recommendations

- Investigate the 2017 decline using additional operational or market data before attributing a cause.
- Monitor the contribution of `N02BE` to understand the risks associated with a concentrated sales mix.
- Investigate the growth in `R03` and determine whether it continues in subsequent, complete periods.
- Validate data completeness before comparing annual performance.
- Combine sales data with relevant inventory, pricing, or promotional information if those datasets become available.

These are analytical recommendations, not conclusions about causes established by the current dataset.

## Data Limitations

- The 2019 data is incomplete. October contains only 188 observations, compared with approximately 720–744 observations in a typical full month in this dataset.
- The 2019 annual total should not be compared directly with complete years.
- The data does not establish currency, profit, market share, or the causes of sales changes.
- Zero recorded sales do not necessarily mean a pharmacy was closed or that no demand existed.
- The dataset does not contain direct marketing campaign fields, so campaign effectiveness was not measured.

## Project Deliverables

- Databricks analysis notebook
- Annual dashboard Delta table
- Sales trend and category contribution visualizations
- Databricks dashboard
- Project documentation

## Skills Demonstrated

Data analysis · PySpark · Python · Data aggregation · KPI development · Year-over-year analysis · Time-series exploration · Data quality checks · Data visualization · Dashboard development · Business insight communication


## Author

**Kanu Winner Ezinne**

**Focus:** Data Analytics and Business Intelligence

