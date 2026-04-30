---
title: Using the Contracts Dashboard
description: With Contracts Dashboard, you can make data-driven decisions by analyzing the trends and insights derived from the contract request data.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Platform Analytics Solutions for Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Using the Contracts Dashboard

With Contracts Dashboard, you can make data-driven decisions by analyzing the trends and insights derived from the contract request data.

On the dashboard, you can analyze the contract request trends, compare data, and drill down into each report to view key performance indicator \(KPI\) details.

For more information on working with KPI details, see [Examining indicators with KPI Details](https://www.servicenow.com/docs/access?context=kpi-details-components&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

![Contracts Dashboard displaying contract-related trends and reports.](../../../product/contract-mgmt-pro/image/cmpro-contracts-dashboard.png "Contracts Dashboard")

## Required ServiceNow AI Platform roles

-   Contract Report Publisher \[sn\_cm\_core.contract\_report\_publisher\]: Needed to edit and publish reports related to contract requests and signed contracts data.
-   Contract Report Viewer \[sn\_cm\_core.contract\_report\_viewer\]: Needed to view reports related to contract requests and signed contracts data.
-   Contract PA Admin \[sn\_cm\_pa.pa\_admin\]: Needed to activate and configure the Analytics Pack for Contract Management Pro.

## Access the Contracts Dashboard

To open the Contracts Dashboard, navigate to **All** &gt; **Contracts Core** &gt; **Contracts Dashboard**.

## Using data in Contracts Dashboard

General counsels can make data-driven decisions through insights into the contract requests data with the following metrics:

-   Number of contract requests created, and contracts signed so far this year along with a comparison to the data collected during the previous run of scheduled jobs.
-   Number of open contract requests by type of paper: own paper and third-party paper.
-   Monthly trend of opened and closed contract requests in the last 12 months.
-   Number of contract requests by age range.
-   Monthly trend of completion time for various contract types in the last 12 months.

## Indicators

-   **YTD Contract request**

    Number of contract requests that have been created so far this year.

-   **YTD Signed Contracts**

    Number of contracts that have been signed so far this year.

-   **Average contract request completion time per contract type**

    Monthly trend of the average completion time of contract requests by various contract types.

-   **Contract Request Age**

    Number of contract requests that have been open for the following periods: 0-30 days, 31-60 days, and 61+ days.


## Breakdowns

-   Contract Type
-   Contract type of paper
-   Contract Request Age

## Reports

<table id="table_wjk_drv_w1c"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total contract requests \(YTD\)

</td><td>

Score![Score icon.](../../reporting/image/icon-single-score-report-p.png)

</td><td>

Contract Request \[sn\_cm\_core\_contract\_request\]

</td><td>

The number of contract requests created so far this year and the trend for contract request data.

 This report compares the latest data with the data collected during the previous run of scheduled jobs. It displays the following information:

-   Increase or decrease in the number of contract requests
-   Percentage of the increase or decrease
-   Date when the data was last collected

</td></tr><tr><td>

Total signed contracts \(YTD\)

</td><td>

Score![Score icon.](../../reporting/image/icon-single-score-report-p.png)

</td><td>

Contract Request Repository \[sn\_cm\_core\_contract\_request\_m2m\_contract\_repository\]

</td><td>

Number of signed contracts so far this year and the trend for signed contracts.

 This report compares the latest data with the data collected during the previous run of scheduled jobs. It displays the following information:

-   Increase or decrease in signed contract requests
-   Percentage of increase or decrease
-   Date when the data was last collected

</td></tr><tr><td>

Open contract requests by type of paper

</td><td>

Donut![Donut icon.](../../reporting/image/icon-donut-report-p.png)

</td><td>

Contract Request \[sn\_cm\_core\_contract\_request\]

</td><td>

Real-time count of open contract requests by the type of paper: own paper and third-party paper.

</td></tr><tr><td>

Contract requests trend

</td><td>

Line![Line icon.](../../reporting/image/icon-line-report-p.png)

</td><td>

Contract Request \[sn\_cm\_core\_contract\_request\]

</td><td>

Real-time monthly trend of contract requests that were opened and closed in the last 12 months.Hovering on a line displays the number of contract requests opened and closed in the month.

</td></tr><tr><td>

Open contract requests by age

</td><td>

Bar![Bar icon.](../../performance-analytics/image/column-icon.png)

</td><td>

Contract Request \[sn\_cm\_core\_contract\_request\]

</td><td>

Real-time count of contract requests by age ranges.The age of a contract request is calculated by the request creation date and the date when you are viewing the report.

</td></tr><tr><td>

Contract request completion time

</td><td>

Line![Line icon.](../../reporting/image/icon-line-report-p.png)

</td><td>

Contract Request \[sn\_cm\_core\_contract\_request\]

</td><td>

Real-time trend of the average completion time for different types of contract requests in the last 12 months. The completion time is calculated from the time the request is created to the time it is closed.Line graph in which hovering on a line displays the completion time for the related contract request type.

To hide a contract request type in the graph, select its name in the legend below the graph.

</td></tr></tbody>
</table>## Filters

<table id="table_yjk_drv_w1c"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract type

</td><td>

Multi-select

</td><td>

Select one or multiple values to view relevant contract type data in the Contracts Dashboard.

</td></tr><tr><td>

Type of paper

</td><td>

Choice

</td><td>

Displays own paper and third-party paper in the list. You can select the desired option to view the relevant data in the Contracts Dashboard.

</td></tr></tbody>
</table>