# Aviation Performance Analysis Dashboard

![Power BI](https://img.shields.io/badge/Power_BI-Desktop-gold?style=for-the-badge&logo=powerbi)
![Data Analysis](https://img.shields.io/badge/Data_Analytics-Business_Intelligence-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

## Executive Summary

This project presents a comprehensive Business Intelligence solution designed to analyze airline performance across three critical dimensions: flight operations, financial revenue, and customer experience. By integrating disparate datasets—including flight logs, passenger feedback, and revenue streams—this Power BI dashboard provides a 360-degree view of the airline's operational health.

The primary objective was to translate raw operational data into actionable strategic insights, addressing key business questions regarding flight punctuality, route profitability, and the impact of delays on customer satisfaction.

## Dashboard Visuals and Analytics

This section highlights the key reporting interfaces developed for this project.

### 1. Executive Command Center
The Home dashboard serves as a high-level strategic tool for C-suite executives. It aggregates critical Key Performance Indicators (KPIs) to monitor daily performance.
* **Visual Features:** Aggregate metrics for Total Revenue, On-Time Percentage (OTP), and Average Load Factor.
* **Strategic Value:** Allows stakeholders to identify seasonal trends affecting demand and delays.


### 2. Flight Operations and Punctuality Report
This report focuses on operational efficiency and reliability. It provides a granular analysis of flight delays, categorizing them by cause (e.g., Technical, Weather, Operational) to facilitate root-cause analysis.
* **Key Insight:** Identifies specific airports and routes that contribute most to flight delays.
* **Metric Focus:** Analysis of delay duration versus carrier performance.


### 3. Revenue and Route Profitability Analysis
This financial view correlates operational metrics with revenue generation. It evaluates the economic performance of individual routes, analyzing the relationship between seat occupancy (Load Factor) and pricing strategies.
* **Key Insight:** Highlights routes that are underperforming despite high demand.
* **Metric Focus:** Revenue per Available Seat Mile (RASM) and the impact of pricing on seat occupancy.


## Business Problem Statements

The dashboard was engineered to address specific business challenges outlined in the project requirements:

### 1. Flight Operations and Punctuality
**Objective:** Minimize operational disruptions and enhance schedule reliability.
* **On-Time Performance (OTP):** Calculated the percentage of flights that are on-time, delayed, or cancelled.
* **Delay Drivers:** Analyzed the top reasons for delays and cancellations to prioritize operational improvements.
* **Route Efficiency:** Identified which routes experience the highest average delay duration.

  <img width="1329" height="747" alt="Screenshot 2026-01-16 201905" src="https://github.com/user-attachments/assets/4cde4c50-d5af-414e-b9b4-7781e9e73ed9" />

### 2. Revenue and Route Performance
**Objective:** Maximize revenue generation and optimize asset utilization.
* **Route Profitability:** Evaluated which routes generate the highest and lowest revenue to inform network planning.
* **Load Factor Analysis:** Assessed how load factor varies across different routes and seasons.
* **Carrier Benchmarking:** Identified which airlines are the most profitable per route.

  <img width="1339" height="742" alt="Screenshot 2026-01-16 201928" src="https://github.com/user-attachments/assets/f3ad26ca-f408-4bf9-b261-e381cc711f30" />

### 3. Customer Experience Analytics
**Objective:** Correlate operational performance with passenger sentiment.
* **Satisfaction Impact:** Quantified how delay duration affects customer satisfaction scores.
* **Complaint Analysis:** Identified which airlines receive the most complaints.
* **Service Recovery:** Highlighted operational factors that drive poor customer experience.

  <img width="1315" height="739" alt="Screenshot 2026-01-16 201943" src="https://github.com/user-attachments/assets/12b9dfb6-6c59-4a33-b776-ad434befbce5" />

### 4. Cost and Efficiency Analysis
**Objective:** Rationalize costs without compromising service quality.
* **Operational Costs:** Calculated the operational cost per flight and per route to identify margin erosion.
* **Aircraft Utilization:** Analyzed how aircraft utilization impacts overall efficiency.

  <img width="1312" height="735" alt="Screenshot 2026-01-16 202001" src="https://github.com/user-attachments/assets/419ae62b-c7cf-4780-b5a9-d635da0a6aa2" />
  <img width="1310" height="733" alt="Screenshot 2026-01-16 202014" src="https://github.com/user-attachments/assets/a83ea24d-3456-4ea3-a31b-87f7d32f34e0" />

## Data Architecture

The solution utilizes a Star Schema data model to ensure query performance and accurate filtering. The model integrates four primary datasets:

| Dataset | Description | Role |
| :--- | :--- | :--- |
| **Airline_Flights.csv** | Comprehensive logs of flight schedules, departure/arrival times, and delay statuses. | Fact Table |
| **Airline_Revenue.csv** | Financial records detailing ticket sales and revenue per flight. | Fact Table |
| **Airline_Passengers.csv** | Passenger demographic data and post-flight satisfaction survey results. | Fact Table |
| **Airline_Airports.csv** | Reference data containing airport codes, names, and geospatial coordinates. | Dimension Table |

## Technical Implementation

* **ETL (Extract, Transform, Load):** Utilized Power Query to cleanse and normalize data. This included handling missing values, standardizing date formats, and merging queries to create a unified data model.
* **Data Modeling:** Established active relationships between dimension tables (Airports) and fact tables (Flights, Revenue) to enable cross-filtering.
* **DAX Calculations:** Developed complex measures for time-intelligence (Year-over-Year growth), dynamic ranking (Top N Routes), and conditional aggregation (Delay segmentation).
* **User Experience (UX):** Designed an intuitive navigation system using bookmarks and page drill-throughs to allow users to move from high-level summaries to detailed row-level data.

## Usage Instructions

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/BhanujaSharma/AVIATION-PERFORMANCE-ANALYTICS]
    ```
2.  **Launch the Dashboard:**
    Open the `.pbix` file in Microsoft Power BI Desktop.
3.  **Data Refresh:**
    Ensure the data source settings point to the local folder if refreshing the report with new CSV files.

---

**Author:** Bhanuja Sharma
**Role:** Data Analyst and Business Intelligence Developer
