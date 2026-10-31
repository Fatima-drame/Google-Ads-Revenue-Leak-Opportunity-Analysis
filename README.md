
# Google Ads Revenue Leak & Opportunity Analysis

**Project Period:** October 2025 – September 2026

---

## Table of Contents

- [Project Overview](#project-overview)
- [Executive Summary](#executive-summary)
- [Business Questions](#business-questions)
- [Tools](#tools)
- [Skills Demonstrated](#skills-demonstrated)
- [Dataset Overview](#dataset-overview)
- [Methodology and Workflow](#methodology-and-workflow)
  - [Data Quality Assessment](#data-quality-assessment)
  - [Data Cleaning & Preparation](#data-cleaning--preparation)
  - [Data Forecasting](#data-forecasting)
  - [Data Modelling in Power BI](#data-modelling-in-power-bi)
  - [Dashboard Design](#dashboard-design)
- [Key Findings and Business Implications](#key-findings-and-business-implications)
- [Recommendations](#recommendations)
- [Expected Business Impact](#expected-business-impact)
- [Limitations and Considerations](#limitations-and-considerations)
- [Potential Future Improvement](#potential-future-improvement)

---

## Project Overview

Northstar Growth is a fictional UK digital marketing agency with reporting data held across advertising, organic search and website analytics tables. This project brings these sources together to examine campaign efficiency and website conversion performance, then translates the findings into practical optimisation recommendations.

## Executive Summary

I prepared the five source tables in Power Query, built the relationships in Power BI and developed a three-page dashboard covering Google Ads performance and efficiency, campaign and audience segmentation, and a monthly conversion forecast.

The dashboard reported £620,926.93 spend, £683,214.45 conversion value, 10,166 conversions and 1.10x ROAS.

The analysis highlighted:

- Ad Group 01 as the weakest performing ad group.
- "boiler installation quote" as the highest-volume search term.
- Tablet is the least performing device.
- Budget and landing-page optimisation actions.

## Business Questions

- How efficiently is advertising spend generating recorded conversions and conversion value?
- Which campaign types and ad groups show stronger or weaker recorded efficiency?
- Which search terms generate meaningful conversion volume relative to spend?
- Which landing pages and devices show differences in reported conversion performance?
- How reliable is a forecast based on the available monthly conversion history?

## Tools

- Excel
- Excel Forecast Sheet
- Power Query
- Power BI
- DAX

## Skills Demonstrated

- Data Cleaning
- Data Transformation
- Data Modeling
- Data Forecasting
- Exploratory Data Analysis
- Dashboard Design
- Data Visualization
- Critical Thinking
- Business Recommendation

## Dataset Overview

The source workbook contained five analytical tables with different purposes and levels of detail. I reviewed their columns before deciding how to prepare and relate the data.

| Source table | Rows | Contents |
|---|---:|---|
| Campaign_Performance | 1,800 | Campaign, ad group, reporting month, impressions, clicks, cost, conversions and conversion value. |
| Search_Terms | 2,500 | Search terms linked to campaigns and months, with impressions, clicks, cost and conversions. |
| Search_Console | 1,500 | Organic queries, landing pages, impressions, clicks, CTR and average position. |
| Landing_Device | 1,200 | Landing page, device, sessions, engaged sessions, key events and related rates. |
| GA4_Events | 1,000 | Recorded events, event date/time, session ID, source/medium, campaign ID, page and device. |

## Methodology and Workflow

### Data Quality Assessment

I imported all five source tables into Power Query to prepare the data in a repeatable workflow. I reviewed the tables and inspected the columns individually before applying transformations.
Found that the dataset contained missing values, wrong data types, outliers, inconsistent spelling, formatting issues.

<img width="252" height="271" alt="image" src="https://github.com/user-attachments/assets/84cb9fd0-26e2-4614-ab03-68096aba664f" />



### Data Cleaning & Preparation

- Trimmed text and standardised capitalisation in each table.
- Changed CTR values from decimal format to percentage format.
- Created custom YearMonth columns for date-related tables.
- Created date and campaign dimension tables.
- Standardised the inconsistent date format before converting the field to a date type.

<img width="315" height="320" alt="image" src="https://github.com/user-attachments/assets/874d7aa9-b21b-44b2-a7fa-e78aba2d289c" />


### Data Forecasting

I duplicated the campaign table for the forecast, retained the conversion and date columns, removed the other columns, and aggregated conversions by date. Loaded the resulting table into Excel and used the Forecast Sheet tool to generate a four-month forecast with lower and upper confidence bounds.

<img width="1090" height="341" alt="image" src="https://github.com/user-attachments/assets/8b73107a-5686-4da7-919d-b0f2fa44dbba" />


### Data Modelling in Power BI

After preparing the tables in Excel, I loaded the workbook into Power BI and created relationships between the tables.

<img width="1338" height="740" alt="image" src="https://github.com/user-attachments/assets/6994edeb-3d17-4a24-a8d2-70aaa08bb349" />

### Dashboard Design

Before creating visuals, I translated the business question into analytical requirements and identified the KPIs, comparisons and charts needed to assess campaign performance, conversion efficiency and optimisation opportunities.

I built three dashboard pages:


#### **Google Ads Performance & Efficiency**

<img width="1212" height="688" alt="image" src="https://github.com/user-attachments/assets/523cbb4b-353a-4bcd-84f8-d6c201b0114a" />



#### **Campaign & Audience Segmentation**

<img width="1301" height="732" alt="image" src="https://github.com/user-attachments/assets/443f5bb7-038c-4535-a5b7-dd6e59669fbb" />



#### **Monthly Conversion Forecast**

<img width="1293" height="732" alt="image" src="https://github.com/user-attachments/assets/fc0787c0-4b46-4714-8be5-c3057702f90b" />

## Key Findings and Business Implications

The total Recorded conversion value is only 10.03% above spend.

Ad Group 01 recorded £3,228.26 spend and 18 conversions, with 0.35x ROAS and comparatively the highest CPA. Making it a candidate for budget review because its recorded return and acquisition cost are weaker.

"Boiler installation quote" recorded approximately £45,000 spend and 788 conversions. This is a high-volume, quote-focused search opportunity that could be supported by a closely aligned landing page.

The drain-unblocking page had a reported conversion rate of 7.0%, compared with 0.1% for the emergency-plumbing page. The difference requires a review of the emergency-plumbing page's message, contact options and enquiry journey.

Reported device conversion rates were 36% for mobile, 25% for desktop and 2% for tablets. Tablet usability and tracking needs to be investigated, before making budget decisions.

## Recommendations

1. Review Ad Group 01's budget because of its 0.35x ROAS and comparatively high CPA. Reallocate budget towards Ad Group 05, which the analysis identified as having the lowest CPA, while monitoring whether the additional spend maintains its efficiency.

2. Create a landing page aligned with the "boiler installation quote" search intent. Make the service information, request-a-quote message and primary call to action prominent.

3. Optimise the emergency-plumbing landing page by making emergency availability and click-to-call prominent, shortening the enquiry process and placing contact details near the top of the page.

4. Improve the mobile conversion journey and investigate tablet landing-page usability and tracking before changing device-level budgets.

5. Keep Performance Max budget changes limited until further evidence establishes whether the CPA difference is meaningful and whether conversion quality supports a change.

6. Use observed campaign and monthly performance to guide current budget decisions. Collect more consistent historical data before relying on forecasts for planning.

## Expected Business Impact

If validated and implemented, the recommendations are intended to improve budget allocation, align landing pages more closely with search intent and reduce friction in the enquiry journey.

## Limitations and Considerations

- The project uses synthetic data and does not demonstrate actual client losses, revenue or guaranteed improvements.
- Recorded conversion value is not necessarily revenue or profit.
- GA4_Events contains recorded event-level data which cannot be treated as unique leads.
- The available history covers approximately one year, limiting the reliability of the four-month conversion forecast.

## Potential Future Improvement

During data preparation, I identified an opportunity to reduce repetitive cleaning as new data is added by connecting GA4 to BigQuery and use SQL to clean and standardise the data into reusable views, which get connected to Looker Studio.
