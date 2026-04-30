---
title: Intelligent Servicing for Fraud dashboard
description: Intelligent Servicing for Fraud contains a preconfigured dashboard with actionable data visualizations that can help your organization improve your business processes and quantify the value of self-service.
locale: en-US
release: yokohama
product: Intelligent Servicing for Fraud
classification: intelligent-servicing-for-fraud
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Intelligent Servicing for Fraud, Using banking applications, Financial Services Operations \(FSO\)]
---

# Intelligent Servicing for Fraud dashboard

Intelligent Servicing for Fraud contains a preconfigured dashboard with actionable data visualizations that can help your organization improve your business processes and quantify the value of self-service.

The Intelligent Servicing for Fraud dashboard enables you to monitor the status of fraud cases, see trends, and drill down into details from a single view. For any given duration, you can view the details for closed cases that breached SLA and open cases that need immediate attention.

![Intelligent Servicing for Fraud dashboard showing metrics such as closed cases and time to close. For descriptions of indicators, breakdowns, and filters included on this dashboard, see the following sections.](../../../product/fso-banking-fraud/image/fso-fraud-dashboard.png "Intelligent Servicing for Fraud dashboard")

## Required ServiceNow AI Platform roles

-   sn\_bom\_fraud.manager, needed to see the dashboard widgets and data.
-   sn\_bom\_fraud.admin, needed to edit the dashboard.

## Access the Intelligent Servicing for Fraud dashboard

To open the dashboard, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**, then select the **Fraud Management** tile.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_lqm_w3z_ypb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Fraud manager

</td><td>

Needs to gain visibility into the status of fraud cases and do the following:-   Monitor open fraud cases that have breached an SLA \(Service Level Agreement\) or are about to breach an SLA and hence need attention
-   Monitor the volume of fraud cases for each fraud category and their trend
-   Review the average closing time of cases for each category
-   Drill down into details in a fraud category

</td></tr><tr><td>

Fraud admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **Number of closed cases breached SLA**

    Count of closed fraud cases in a day that have breached SLA.

-   **Number of closed cases with SLA**

    Count of fraud cases closed that day within SLA. This indicator is used to compare the number of cases closed that met SLA vs. cases that breached SLA.

-   **Number of closed cases**

    Count of closed fraud cases in selected time period where breakdowns are Fraud Source, Service and Risk classification.

-   **Fraud Cases with writeoff**

    For selected time period, this holds the total writeoff amount of closed fraud cases that underwent write-off process where breakdown is Service.

-   **Fraud Cases with recovery option**

    For selected time period, this holds the total recovery amount of closed fraud cases that underwent recovery process where breakdown is Service.

-   **Open Cases**

    Count of cases open as of today. The indicator is used to compare and see the trend of the number of cases created vs. cases closed vs. open cases.

-   **Number of cases created**

    Count of new fraud cases created today. The indicator is used to compare and see the trend of the number of cases created vs. cases closed vs. open cases.

-   **Average time to close case**

    Breakdown of average number of hours to close fraud cases. The score is calculated as: \[FSO Fraud.Summed duration of closed cases\]/\[ FSO Fraud.Number of closed cases\]


## Breakdowns

-   Fraud service
-   Fraud source
-   Fraud risk classification

## Filters

|Name|Type|Description|
|----|----|-----------|
|Fraud service|Choice|Shows all active services defined for the Fraud case \[sn\_bom\_fraud\_case\] table.|
|Fraud risk classification|Choice|Shows all active risk classifications for the Fraud case \[sn\_bom\_fraud\_case\] table.|
|Fraud source|Choice|Shows all active source types for the Fraud case \[sn\_bom\_fraud\_case\] table.|

