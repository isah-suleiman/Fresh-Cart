# Ad Analysis

## Introduction

This Power BI project aims to analyze advertising data for the fictional company “Fresh Cart.” By deriving insights from the data, we aim to answer crucial questions and provide actionable recommendations to help the store make informed decisions.

**_Disclaimer_**: _The data used in this analysis is purely fictional and created for educational purposes. Any resemblance to real individuals, companies, or events is coincidental. The dataset does not represent any actual business or organization, and the insights derived from it should be treated as hypothetical._

## Problem Statement

**FreshCart's Advertising Challenges:**

1. **Inefficient Ad Spend:**
   - FreshCart suspects that not all their digital advertising dollars are generating the desired return on investment (ROI).
   - Some campaigns may be costing more than they contribute in revenue.

2. **Identifying Effective Channels:**
   - FreshCart faces difficulty in determining which advertising platforms (search engines, social media, etc.) yield the best ROI.
   - Choosing the right channels is crucial in a competitive online grocery market.

As FreshCart aims to optimize its digital ad spend, addressing these challenges becomes essential. 🚀

## Project Objective: Optimizing FreshCart's Digital Ad Spending

**Specific Objectives:**

1. **Evaluate Campaign Effectiveness:**
   - Analyze the performance of current advertising campaigns across different platforms.
   - Metrics to consider: click-through rates (CTR), impressions, and conversions.

2. **Identify Top-Performing Channels:**
   - Determine which advertising channels (e.g., search engines, social media) yield the highest return on investment (ROI).
   - Consider cost per acquisition (CPA) and overall engagement.

3. **Assess Demographic Engagement:**
   - Segment the audience based on demographics (age, gender, location).
   - Evaluate engagement levels (likes, shares, comments) for each demographic group.

4. **Recommend Budget Allocation Strategies:**
   - Based on insights, propose adjustments to the ad budget allocation:
     - Allocate resources to high-performing channels.
     - Optimize spending for maximum impact.

## Skills and Concepts Demonstrated

The following power BI features were incorporated
- Data integration,
- cleaning and modeling,
- Dax,
- page navigation,
- filters

## Modelling
![Alt text](assets/images/freshcartdash.jpg)
Certainly! The data model displayed in the screenshot combines two tables: "ad_campaign_data" and "DateTable." A relationship links these tables. The model helps analyze advertising metrics, track performance over time, and optimize ad spending for FreshCart. 

The “ad_campaign_data” table is the fact table and The “DateTable” is the dimension table.

## Dax Measures

### 1. Conversion Rate
- **Purpose:** Calculate the percentage of conversions relative to total clicks.
- **DAX Expression:**
  ```DAX
  Conversion Rate = DIVIDE(SUM(ad_campaign_data[Conversions]), SUM(ad_campaign_data[Clicks]), 0)
  ```
- **Explanation:** This measure divides the total conversions by total clicks, handling cases where there are no clicks (denominator is zero).

### 2. Cost Per Conversion
- **Purpose:** Determine the cost associated with each conversion.
- **DAX Expression:**
  ```DAX
  Cost Per Conversion = DIVIDE(SUM(ad_campaign_data[Cost]), SUM(ad_campaign_data[Conversions]), 0)
  ```
- **Explanation:** This measure calculates the average cost per conversion.

### 3. CTR (Click-Through Rate)
- **Purpose:** Measure the effectiveness of ads.
- **DAX Expression:**
  ```DAX
  CTR = DIVIDE(SUM(ad_campaign_data[Clicks]), SUM(ad_campaign_data[Impressions]), 0)
  ```
- **Explanation:** CTR calculates the ratio of clicks to impressions.

### 4. ROAS (Return on Ad Spend)
- **Purpose:** Evaluate revenue generated relative to advertising costs.
- **DAX Expression:**
  ```DAX
  ROAS = DIVIDE(SUM(ad_campaign_data[ConversionValue]), SUM(ad_campaign_data[Cost]), 0)
  ```
- **Explanation:** ROAS quantifies how efficiently ad spending translates into revenue.

---
## Visualization

The Report Contains 3 pages.
1. Home
2. Analysis
3. Campaign

![Alt text](assets/images/freshcartdash.jpg)
![Alt text](assets/images/freshcartcamp.jpg)
![Alt text](assets/images/frescartplatform.jpg)
