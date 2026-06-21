---
title: Financial Management Level 3 Costing – Business Capabilities dashboard
description: The Level 3 Costing – Business Capabilities dashboard provides an executive view into the total spend drilled down to the business units or business capabilities for a quarter and year-to-date. The dashboard provides visibility on the cost of supporting a business capability and helps communicate value in terms of the business functions aligned to the business capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-business-management/financial-management/financial-mgmt-level3-costing-business-capabilities.html
release: xanadu
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Financial Management Platform Analytics Solutions, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Financial Management Level 3 Costing – Business Capabilities dashboard

The Level 3 Costing – Business Capabilities dashboard provides an executive view into the total spend drilled down to the business units or business capabilities for a quarter and year-to-date. The dashboard provides visibility on the cost of supporting a business capability and helps communicate value in terms of the business functions aligned to the business capabilities.

**Important:**

This feature is available only when you own an ITBM Analyst license.

The dashboard is based on Level 3 Costing – Business Capabilities cost model. The model aligns the actual capability that is associated with a business application with the high-level business capability.

\[Omitted image "Level3CostingBusinessCapabilitiesDashboard.png"\] Alt text: Screenshot showing Level 3 Costing – Business Capabilities dashboard

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Financial Modeling Analyst: To track the total spend of business applications. Administrator: To track the amount spent on a business capability aligned to each business unit.|cost\_transparency\_admin|
|Financial Modeling Analyst: To track the total spend of business applications. Analyst: To predict the future total cost of business capability based on its past trend. Requires to constantly realign the business capability with the changing business trends and requirements.|cost\_transparency\_analyst|

## Indicators

-   **Total Expenses Fiscal Quarterly – Business Capability Cost Model**

    The indicator collects fiscal quarterly total cost data for the Business Capability and Business Unit of the Level 3 Costing – Business Capabilities cost model.

-   **Total Expenses Fiscal Quarterly Breakdowns – Business Capability Cost Model**

    The indicator collects fiscal quarterly cost allocation aggregated data that is rolled up from the Business Capability to the Business Unit of the level 3 cost model.

-   **Average Cost Per User**

    Formula used to calculate the average cost of business capabilities per user.


## Breakdowns

-   Business unit.
-   Business capability.

## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Business Capabilities with Drivers|Bar\[Omitted image "bar-stacked.svg"\] Alt text: Bar stacked report|Displays the total amount spent on business capabilities stacked by buckets \(cost pools\) from which the amount is allocated.|
|Average Enterprise Cost per CPU|Spline\[Omitted image "spline.svg"\] Alt text: Spline chart|Displays the trend of average unit cost per CPU.|
|Business Units – Business Capabilities|Pivot\[Omitted image "pivot.svg"\] Alt text: Pivot report|Gives a tabular view of the amount spent on the business capabilities by the business units for the last four quarters.|

**Parent Topic:**[Financial Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-business-management/financial-management/financial-content-pack.md)

