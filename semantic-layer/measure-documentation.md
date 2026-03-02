# Semantic Layer Measure Documentation

This document describes the core measures used in the Power BI model for PlantControllerSim.

Purpose
Provide clear measure intent, business definition, and calculation approach so the report is understandable without opening the PBIX.

## Scope and assumptions

- Dataset is simulated and contains no real company data
- Month filtering uses MonthKey
- Measures are written to support reconciliation and controller style analysis

## Measure groups

### Revenue and margin

#### Revenue
Definition  
Total invoiced sales for the selected month.

Source  
Close view for sales revenue.

Notes  
Ties to AR movement and GL revenue for the month.

#### Standard COGS
Definition  
Standard cost of shipped finished goods for the selected month.

Source  
Close view for standard COGS.

Notes  
Used to compute standard gross margin before variances.

#### Standard Gross Margin
Definition  
Revenue minus Standard COGS.

Notes  
Baseline margin before manufacturing variances.

### Manufacturing variances

#### Material Price Variance
Definition  
Difference between actual purchase price and standard price for purchased material, multiplied by purchase quantity.

Notes  
Favorable when positive, unfavorable when negative if you keep your current sign convention.

#### Material Usage Variance
Definition  
Difference between actual material consumption quantity and standard quantity allowed for output, multiplied by standard price.

Notes  
Highlights process yield and scrap.

#### Labor Rate Variance
Definition  
Difference between actual labor rate and standard rate, multiplied by actual hours.

#### Labor Efficiency Variance
Definition  
Difference between actual hours and standard hours allowed for output, multiplied by standard rate.

#### Overhead Spending Variance
Definition  
Difference between actual overhead spending and budgeted overhead spending for the achieved activity base.

#### Overhead Volume Variance
Definition  
Difference caused by absorbing overhead based on production volume versus the budget base.

Notes  
Often the largest driver in absorption costing when production volume differs from budget base.

#### Total Manufacturing Variance
Definition  
Sum of all manufacturing variance components.

Notes  
Should tie to the variance bridge and close view totals.

### Close level profit

#### EBIT
Definition  
Earnings before interest and taxes after including standard gross margin and all variance and period close adjustments such as depreciation and warranty.

Notes  
Should tie to the management P and L close output.

### Working capital and balance sheet hooks

#### AR Ending
Definition  
Ending accounts receivable balance for the selected month.

Notes  
Should reconcile to sales and collections.

#### AP Ending
Definition  
Ending accounts payable balance for the selected month.

#### Inventory Ending
Definition  
Ending inventory value for the selected month.

Notes  
Should reconcile via inventory bridge.

#### Net Working Capital
Definition  
AR plus Inventory minus AP.

Notes  
This is the high level working capital exposure indicator.

## Reconciliation checks

- Variance totals tie to GL variance postings
- EBIT ties to Excel close output
- Inventory bridge ties opening plus movements to ending
- Working capital ties AR, AP, inventory ending to NWC

## Measure list checklist

- Revenue
- Standard COGS
- Standard Gross Margin
- Material Price Variance
- Material Usage Variance
- Labor Rate Variance
- Labor Efficiency Variance
- Overhead Spending Variance
- Overhead Volume Variance
- Total Manufacturing Variance
- Depreciation
- Warranty
- EBIT
- AR Ending
- AP Ending
- Inventory Ending
- Net Working Capital