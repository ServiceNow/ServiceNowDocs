---
title: Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for Data Foundations
description: The CMDB success advisor for Data Foundations dashboard enables CMDB administrators to identify and address data quality issues specific to principal classes in the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-dashboard.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 4
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for Data Foundations

The CMDB success advisor for Data Foundations dashboard enables CMDB administrators to identify and address data quality issues specific to principal classes in the Configuration Management Database \(CMDB\).

**Important:** When you select a segment or count on a chart from a CMDB success advisor dashboard, the KPI Details page opens. On the page, you can analyze how a specific metric trends over time. Additionally, the Remediation actions panel appears when remediation actions are available for that card. Use the panel to improve the quality of CMDB. To learn more, see [KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/kpi-details.md) and [Improving CMDB data quality for Data Foundations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-remediation.md).

\[Omitted image "cmdb-sa-df-dashboard.png"\] Alt text: CMDB success advisor for Data Foundations dashboard overview.

**Note:** If the Performance Analytics data collector exceeds its row limit during data processing, a notification banner appears on the dashboard indicating that some metrics could not be loaded. For more information, see [Data collector Performance Analytics properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/performance-analytics/pa-dc-props.md).

## Access the dashboard

To open the dashboard, select **View insights** for Data Foundations on the CMDB success advisor landing page. See [Access CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-access.md).

**Note:** The CMDB success advisor for Data Foundations dashboard is available only after the setup process is complete. For more information, see [CMDB success advisor for Data Foundations setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-config-settings.md).

## Required roles

|Role|Description|
|----|-----------|
|sn\_cmdb\_admin|Required to access the Data Foundations dashboard.|

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_lnc_zz1_2gc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

CMDB administrator

</td><td>

-   Monitor CI attribute completeness across principal classes
-   Identify classes at risk with low data quality scores
-   Detect stale and duplicate CI records affecting CMDB data accuracy
-   Evaluate integration coverage to ensure the right sources are populating the CMDB
-   Prioritize remediation efforts based on incident, change, and problem impact
-   Track progress toward CSDM alignment

</td></tr></tbody>
</table>## Dashboard features

The dashboard provides clear, consolidated insights into principal CI class data quality and completeness. Use the dashboard to identify and resolve data quality issues within the CMDB through dedicated sections, filters, indicators, and visual reports. Gain valuable insights into CMDB performance related to Data Foundations. Targeted CMDB metrics focus remediation efforts. Regularly monitor these metrics and follow suggested remediation actions to systematically improve CMDB data quality over time.

**Important:** The dashboard data is filtered based on the Selected principal classes and Date range filters. See [Filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-dashboard.md).

|Feature|Description|
|-------|-----------|
|CIs by principal class|Displays the breakdown of operational CIs by principal CI class to highlight CI distribution in the CMDB.|
|CIs by data integration source|Displays the breakdown of operational CIs by data integration source to highlight their contribution to CMDB population.|
|[CIs missing key attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-dashboard.md)|Displays completeness metrics per principal CI class, identifying classes below the defined threshold.|
|[CI data quality issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-dashboard.md)|Displays key metrics related to CIs that have not been updated or may have duplicate records, leading to outdated information and inconsistencies in the CMDB.|

## Filters

Enables narrowing the data shown in graphs and metrics based on principal class, date range, or stale CI threshold.

|Name|Type|Description|
|----|----|-----------|
|Principal classes|List|Filters CIs based on the selected principal classes.|
|Date range|Date|Filters the dashboard data based on the selected date range.|
|Stale CI|List|Filters stale CIs based on the number of days since their last update. Available values: `7`, `14`, `30`, `60`, and `90` days.|

## CIs missing key attributes

Key metrics for the completeness of CI attributes across principal classes, identifying gaps that affect data quality.

|Card|Description|Indicators|
|----|-----------|----------|
|CIs missing name|Total number of CI records from principal classes missing a name, measured daily, where the CI does not have a name specified.|[DF CIs missing name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)|
|CIs missing managed by group|Total number of CI records from principal classes missing a managed by group, measured daily, where the CI does not have a managed by group assigned.|[DF CIs missing managed by group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)|
|CIs missing location|Total number of CI records from principal classes missing a location, measured daily, where the CI does not have a location assigned.|[DF CIs missing location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)|

## CI data quality issues

Key metrics for CIs that have not been updated or may have duplicate records, leading to outdated information and inconsistencies in the CMDB.

<table><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Stale CIs

</td><td>

Principal class CIs not updated within the expected maintenance window, causing data gaps and inaccuracies that affect incident and change impact analysis. Additionally filtered by the [Stale CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-dashboard.md) filter.When you select a segment on the Stale CIs chart, the KPI Details page title reflects the Stale CI filter value selected at the time \(for example, "CIs not updated in last 30 days"\).

</td><td>

[DF CIs not updated in last 7 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)[DF CIs not updated in last 14 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)

[DF CIs not updated in last 30 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)

[DF CIs not updated in last 60 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)

[DF CIs not updated in last 90 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)

**Note:** The CIs not updated card data is additionally filtered based on the Stale CI filter. See [Filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-dashboard.md).

</td></tr><tr><td>

Duplicate CIs

</td><td>

Operational CIs identified as duplicates within principal classes, causing ambiguous CI selection in processes and data redundancy.

</td><td>

[DF duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-indicators.md)

</td></tr></tbody>
</table>