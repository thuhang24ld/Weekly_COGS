# 📊 F&B Strategic COGS & Inventory Control Dashboard

[![Google Sheets API](https://img.shields.io/badge/Google%20Sheets%20API-v4-green.svg)](https://developers.google.com/sheets/api)
[![Looker Studio](https://img.shields.io/badge/Looker%20Studio-Visualization-orange.svg)](https://lookerstudio.google.com/)

## 📝 Project Overview
This project delivers a comprehensive **Cost of Goods Sold (COGS)** analysis system customized for buffet and à la carte restaurant chains. The system tracks revenue structures, ingredient costs, and operational efficiency over time, giving management full visibility into inventory consumption and waste.

## 🎯 Business Challenge & Objective
In the F&B sector—particularly within the **all-you-can-eat (Buffet)** model—calculating the exact cost of ingredients consumed per guest is a major operational challenge. 

This system addresses that problem by:
* **Breaking Down Costs:** Segregating COGS by service types (e.g., *Vé ăn xanh* (Food buffet)], *Vé uống lành* (Drink buffet), and *Hàng bán thẳng* (Direct retail/À la carte)).
* **Controlling Wastage:** Quantifying the exact financial impact of expired or discarded goods (*Xuất hủy*).
* **Optimizing Portions:** Measuring the average consumption per guest (Cost per Pax) to help chefs and management fine-tune menu engineering and supply chain orders.

  
## 💡 Methodology: Periodic Inventory System
To accurately capture consumption without relying solely on theoretical recipe assumptions, this system implements the **Periodic Inventory Method**:

$$\text{Actual Consumption} = \text{Beginning Inventory} + \text{Purchases During Period} - \text{Ending Inventory}$$

From this foundation, the system computes core financial and operational metrics:
1. **Cost per Pax (Cost per Guest):** $$\text{Cost per Pax} = \frac{\text{Total Cost of Ingredients Consumed}}{\text{Total Number of Guests (Pax) served}}$$
2. **COGS Percentage (% COGS):** Calculated against Net Revenue to evaluate the gross profit margin for each item/ticket type.
3. **Wastage Rate:** Evaluates physical and financial shrinkage by comparing discarded goods (*Giá trị xuất hủy*) against the total warehouse issues (*Giá trị xuất kho*).


## 🛠 Tech Stack
* Visualization: Looker Studio.
* Data Pipeline: Google Sheets automated data cleaning and inventory logic processing.
* Data Sources: Sales records, Physical Stocktake logs

## 📊 Report Modules & Key Metrics Included

As outlined in **"Báo_cáo_COGS.pdf"**, the analysis is divided into four key operational dashboards[cite: 1]:

### 1. Executive Summary & Revenue Structure
* **Revenue Breakdown:** Visualizes revenue share by product type (Buffet tickets vs. À la carte)[cite: 1].
* **COGS Trend Over Time:** Tracks weekly fluctuations in food costs to flag operational anomalies (e.g., supplier price spikes, kitchen portion control issues)[cite: 1].

### 2. Buffet Gaskets Analysis (Food & Drink Tickets)
* **Detailed Group Breakdown:** Itemized consumption and costs for specific ticket types like *Vé ăn xanh* and *Vé uống lành*[cite: 1].
* **Average Consumption per Guest:** Calculates the exact average quantity of each ingredient group consumed by a single customer[cite: 1].

### 3. Direct Sales (À la carte / Hàng bán thẳng)
* Separate tracking for revenue, cost, and net margins of items sold directly outside the standard buffet packages[cite: 1].

### 4. Inventory Discharges & Warehouse Issues (Xuất hủy & Xuất kho)
* **Wastage Log:** Granular tracking of the value of items discarded during the period[cite: 1].
* **Warehouse Outflow:** Measures total quantities and financial value issued from the central store/kitchen to cross-check with actual consumption[cite: 1].

