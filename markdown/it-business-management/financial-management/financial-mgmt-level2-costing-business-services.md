---
title: Financial Management Level 2 Costing – Business Services dashboard
description: The Level 2 Costing – Business Services dashboard provides an executive view into the cost of enabling a business service and aligning it to the business capabilities of an enterprise. The dashboard provides visibility on the cost of supporting a business service and helps understand the cost of the business services driven by the business units.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-business-management/financial-management/financial-mgmt-level2-costing-business-services.html
release: xanadu
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Financial Management Platform Analytics Solutions, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Financial Management Level 2 Costing – Business Services dashboard

The Level 2 Costing – Business Services dashboard provides an executive view into the cost of enabling a business service and aligning it to the business capabilities of an enterprise. The dashboard provides visibility on the cost of supporting a business service and helps understand the cost of the business services driven by the business units.

**Important:**

This feature is available only when you own an ITBM Analyst license.

The dashboard is based on Level 2 Costing – Business Services cost model that aligns business services to business units. Therefore, you can track the service cost for each business unit.

\[Omitted image "Level2CostingBusinessServiceDashboard.png"\] Alt text: Screenshot showing the Level 2 Costing – Business Services dashboard.

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Financial Modeling Analyst: To track the total spend of business applications. Administrator: To track the amount spent on a business service aligned to each business unit.|cost\_transparency\_admin|
|Financial Modeling Analyst: To track the total spend of business applications. Analyst: To predict the future total cost of business service based on its past trend. Requires to constantly realign the business service with the customer needs and the organizational goals.|cost\_transparency\_analyst|

## Indicators

-   **Total Expenses Fiscal Quarterly – Business Service Cost Model**

    The indicator collects fiscal quarterly total cost data for the Business Services and Business Unit of the Level 2 Costing – Business Services cost model.

-   **Total Expenses Fiscal Quarterly Breakdowns – Business Service Cost Model**

    The indicator collects fiscal quarterly cost allocation aggregated data that is rolled up from the Business Service to the Business Unit of the level 2 cost model.


## Breakdowns

-   Business unit.
-   Business service.

## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Business Services with Drivers|Bar\[Omitted image "bar-stacked.svg"\] Alt text: Bar stacked report|Displays the total amount spent on business services stacked by buckets from which the amount is allocated.|
|Average Enterprise Cost per Workstation|Spline\[Omitted image "spline.svg"\] Alt text: Spline chart|Displays the trend of average unit cost per workstation for the last four quarters.|
|Average Enterprise Cost per CPU|Spline\[Omitted image "spline.svg"\] Alt text: Spline chart|Displays the trend of average unit cost per CPU.|
|Business Unit – Business Service|Pivot\[Omitted image "pivot.svg"\] Alt text: Pivot report|Gives a tabular view of the amount breakup spent by the business units on the business services for the last four quarters.|

**Parent Topic:**[Financial Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-business-management/financial-management/financial-content-pack.md)

