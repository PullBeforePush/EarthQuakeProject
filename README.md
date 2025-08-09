# Building an End-To-End Data engineering project using Microsoft Fabric

## **Welcome to my first Data Engineering project!**

In this project, we'll explore building a data pipeline using **Microsoft Fabric**, applying the **Medallion Architecture** to organize earthquake data—from raw to refined—for easier analysis.

We'll source data from the **USGS Earthquake Hazards Program API**, and by the end of the project, we will have created an **automated system** that retrieves earthquake data, processes it, and delivers updated insights daily via **Power BI** dashboards.

## **Business Case**

Earthquake data is invaluable for understanding seismic activity and mitigating associated risks.
Government agencies, research institutions, and insurance companies depend on timely, accurate information to plan emergency responses and assess potential hazards. This automated pipeline ensures that these stakeholders receive up-to-date data in a clear, accessible format—saving time, enhancing decision-making, and supporting more effective risk management.

## **Solution Overview**

We're going to use **Microsoft Fabric** to build an end-to-end earthquake data pipeline using the medallion architecture. This involves:
- **Bronze Layer**: Collect raw earthquake data.
- **Silver Layer**: Transform it into a clean, structured format.
- **Gold Layer**: Enrich it with calculated fields for analysis.
- **Power BI**: Visualise the data interactively.
- **Data Factory**: Automate the entire process, ensuring up-to-date information daily.

## **Project Architecture**
![Frame 1](https://github.com/PullBeforePush/EarthQuakeProject/blob/d4839f63aa7949945ed58cca8923085d37642d11/DataDesign.png)

## **Medallion Architecture in Action**
Let'e break down each layer:
1. **Bronze Layer (Raw Data Ingestion)**
- **What It Does**: This Layer is for storing raw data, exactly as we receive it form the API
   - **How We Do It**: Fetch earthquake data from an external API using a Python script and store it as JSON files in the Fabric Lakehouse.
   -**Why it's Important**: This keeps the original data safe for audit incase issues rise and we need to audit the data.
