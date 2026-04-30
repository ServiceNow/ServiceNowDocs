---
title: Financial Management Business Application Costing dashboard
description: The Business Application Costing dashboard provides an executive view into the total expenses on business applications consolidated for a quarter and year-to-date. The dashboard provides visibility on the application cost to an extent that you can drill the data on top spenders down to the buckets that contribute to the application cost, and business units that use the applications.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Financial Management Platform Analytics Solutions, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Financial Management Business Application Costing dashboard

The Business Application Costing dashboard provides an executive view into the total expenses on business applications consolidated for a quarter and year-to-date. The dashboard provides visibility on the application cost to an extent that you can drill the data on top spenders down to the buckets that contribute to the application cost, and business units that use the applications.

The dashboard is based on the Business Applications Costing cost model. This cost model aligns business applications to business units and hence enables you to know the cost of applications that support each business unit.

![Screenshot showing Business Application Costing dashboard.](../image/Level2CostingBusinessApplicationsDashboard.png "Business Application Costing dashboard")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Financial Modeling Analyst: To track the total spend of business applications. Administrator: To track the amount spent on a business application.|cost\_transparency\_admin|
|Financial Modeling Analyst: To track the total spend of business applications. Analyst: To predict the future cost of application based on its past trend, and determine whether to continue with the application or not.|cost\_transparency\_analyst|

## Indicators

-   **Total Expenses Fiscal Quarterly – Application Cost Model**

    The indicator collects fiscal quarterly total cost data for the Business Applications and Business Unit of the Business Applications Costing cost model.

-   **Total Expenses Fiscal Quarterly Breakdowns – Application Cost Model**

    The indicator collects fiscal quarterly cost allocation aggregated data, rolled up from the Business Application to the Business Unit of the level 2 cost model.

-   **Average Cost Per User – Application**

    Average cost of applications consumed by a user.


## Breakdowns

-   Business unit.
-   Business applications.
-   Buckets – Application Cost.

## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Business Applications Cost with Drivers|Bar![Bar stacked report](../../../reuse/reporting/image/bar-stacked.svg)|Displays the amount that each account in the Business Application consumes from different buckets \(cost pools\).|
|Average Enterprise Cost per CPU|Spline![Spline report](../../../reuse/reporting/image/spline.svg)|Displays the trend of average unit cost per CPU.|
|Business Unit – Business Application|Pivot![Pivot report](../../../reuse/reporting/image/pivot.svg)|Gives a tabular view of the amount breakup spent by the business units on the applications for the last four quarters.|

**Parent Topic:**[Financial Management Platform Analytics Solutions](financial-content-pack.md)

