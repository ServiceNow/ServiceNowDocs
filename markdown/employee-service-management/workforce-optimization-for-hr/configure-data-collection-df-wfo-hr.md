---
title: Configure data collection for Demand Forecast
description: Define the data you want to collect for cases, interactions, or any table to forecast the number of agents that you require for your staffing needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workforce-optimization-for-hr/configure-data-collection-df-wfo-hr.html
release: australia
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure demand forecast, Configure, Workforce Optimization overview, HR Service Delivery, Employee Service Management]
---

# Configure data collection for Demand Forecast

Define the data you want to collect for cases, interactions, or any table to forecast the number of agents that you require for your staffing needs.

## Before you begin

You must have the MetricBase plugin \[com.snc.clotho\] enabled to use Demand Forecast in Workforce Optimization for HR. For more information, see Requesting the MetricBase product.

Role required: sn\_hr\_wfo.admin

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for HR** &gt; **Demand Forecast**.

2.  Define the data you want to collect for forecasting agents to resolve cases.

    1.  Click **Data Collection Definitions**.

        See the [Components installed with Workforce Optimization for HR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workforce-optimization-for-hr/wfo-hr-reference.md) for the list of configurations that are available by default.

    2.  Click **New**.
    3.  On the form, fill in the fields:

        |Field|Description|
        |-----|-----------|
        |Name|Name for the collection forecast configuration.|
        |Table|Table that is used for collecting data.|
        |Type|Data Collection Definition type is set to **Collection** by default and collects data using a scheduled job.|
        |Date Field|Data that you can add to forecast for the future.|
        |Conditions|Conditions that you can set so that you can capture the data that you need.|

    4.  Click **Submit**.
    5.  Create an index for the table you have created using the date field and the conditions you have added to the table. For information on creating a table index, see Create a table index.

-   **[Add parameters to be defined in the formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workforce-optimization-for-hr/add-formula-parameters-wfo-hr.md)**  
Add parameters to be defined in the formula to calculate agent count per hour in a day.
-   **[Configure resource conversion formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workforce-optimization-for-hr/configure-reverse-conversion-wfo-hr.md)**  
Configure the resource conversion formula.
-   **[Group forecast configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workforce-optimization-for-hr/group-forecase-configuration-wfo-hr.md)**  
Associate an assignment group with a Resource Conversion Formula. You can assign a forecast configuration to multiple assignment groups, but an assignment group can have only one forecast configuration.

**Parent Topic:**[Setting up Demand Forecast in Workforce Optimization for HR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workforce-optimization-for-hr/setup-demand-forecast-wfo-hr.md)

