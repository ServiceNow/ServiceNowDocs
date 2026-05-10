---
title: Configure workplace data sources
description: Configure multiple data sources to generate insights.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Insight cards on the Workplace Central dashboard, Workplace Advisor Overview, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Configure workplace data sources

Configure multiple data sources to generate insights.

## Before you begin

Role required: admin

## About this task

Each data source is mapped to a prompt configuration, ensuring that relevant data is processed and transformed into actionable insights.

## Procedure

1.  Navigate to **All** &gt; **Workplace Insights** &gt; **Data Source**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ex4_5dr_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name used to identify the data source.

</td></tr><tr><td>

Application

</td><td>

By default, the application is set to AI Agents for Workplace Service Delivery.

</td></tr><tr><td>

Domain

</td><td>

By default, the domain is set to global.

</td></tr><tr><td>

Source

</td><td>

Option to specify the source from which this record is created. The following options are available:-   Table
-   Indicator


</td></tr><tr><td>

Table

</td><td>

A source table from which the data is retrieved. The **Table** field appears when **Table** is selected from the Source list. Select the required table from the list. For example, Reservation \[sn\_wsd\_core\_reservation\].

</td></tr><tr><td>

Filter condition

</td><td>

Set the filters in the Filter Condition field and define the criteria.Add more conditions by selecting  AND  or  OR.

-   If  AND  is selected, all conditions must be matched.
-   If  OR  is selected, either condition can be matched.
This field appears when you select **Table** from the **Source** field.

</td></tr><tr><td>

Field selector

</td><td>

A list of fields available for selection. This field appears when you select **Table** as the value in the **Source** field.

</td></tr><tr><td>

Indicator

</td><td>

The **Indicator** field appears when **Indicator** is selected from the Source list. Select the lookup icon![](../../workplace-lease-administration/images/look-up-icon.png) and select the indicator for the data source.Specify the details for the following fields that appear when you select **Indicator** in the **Source** field.

-   **Time Period**
-   **Step**
-   **Breakdown**
-   **Aggregator**
For more information about the fields, see [Performance Analytics indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_Indicators.md).

**Note:** The PA admin role \(pa\_admin\) must be explicitly assigned to users for them to run historic indicator jobs and edit indicators.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Insight cards on the Workplace Central dashboard](../concept/insight-cards-on-the-workplace-central-dashboard.md)

