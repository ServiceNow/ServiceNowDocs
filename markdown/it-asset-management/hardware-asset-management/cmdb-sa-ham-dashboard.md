---
title: Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for HAM
description: The CMDB success advisor for HAM dashboard enables CMDB administrators to identify and address data quality issues specific to HAM in the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 6
breadcrumb: [Use HAM advisor, Asset and CI management, Explore, Hardware Asset Management, IT Asset Management]
---

# Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for HAM

The CMDB success advisor for HAM dashboard enables CMDB administrators to identify and address data quality issues specific to HAM in the Configuration Management Database \(CMDB\).

**Important:** When you select a segment or count on a chart from a CMDB success advisor dashboard, the KPI Details page opens. On the page, you can analyze how a specific metric trends over time. Additionally, the Remediation actions panel appears when remediation actions are available for that card. Use the panel to improve the quality of CMDB. To learn more, see  and [Improving CMDB data quality for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-remediation.md).

\[Omitted image "cmdb-sa-ham-dashboard.png"\] Alt text: CMDB success advisor for HAM dashboard overview.

**Note:** If the Performance Analytics data collector exceeds its row limit during data processing, a notification banner appears on the dashboard indicating that some metrics could not be loaded. For more information, see .

## Access the dashboard

To open the dashboard, select **View insights** for HAM on the CMDB success advisor landing page. See .

**Note:** The CMDB success advisor for HAM dashboard is available only after the setup process is complete. For more information, see [Set up CMDB success advisor for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-config-settings.md).

## Required roles

|Role|Description|
|----|-----------|
|sn\_cmdb\_admin|Required to access the dashboard.|

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_lnc_zz1_2gc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

CMDB administrator

</td><td>

-   Gain real-time visibility into hardware asset data quality and completeness
-   Identify missing or incorrect CI attributes quickly
-   Detect duplicate CIs and unlinked assets
-   Monitor asset life cycle status \(installed, retired, inactive\)
-   Prioritize and track data cleanup and remediation tasks
-   Verify that the CMDB stays accurate to support HAM

</td></tr></tbody>
</table>## Dashboard features

The dashboard provides clear, consolidated insights into hardware asset data quality and asset status. Use the dashboard to identify and resolve data quality issues within the CMDB through dedicated sections, filters, indicators, and visual reports. Gain valuable insights into CMDB performance related to HAM.

Targeted CMDB metrics focus remediation efforts. Regularly monitor these metrics and follow suggested remediation actions to systematically improve CMDB data quality over time.

**Important:** The dashboard data is filtered based on the Selected model categories and Date range filters. See [Filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard.md).

|Feature|Description|
|-------|-----------|
|CIs by model category|Displays the breakdown of operational CIs by associated model category to highlight CI distribution in the CMDB.|
|CIs by data integration source|Displays the breakdown of operational CIs by data integration source to highlight their contribution to CMDB population.|
|[CIs missing model data and other key attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard.md)|Displays key metrics related to CIs missing model details, ownership, and other key attributes, leading to incomplete records and operational inefficiencies.|
|[CI data quality issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard.md)|Displays key metrics related to CIs that have not been updated or may have duplicate records, leading to outdated information and inconsistencies in the CMDB.|
|[CI and asset-related issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard.md)|Displays key metrics related to mismatches and missing links between CIs and assets, leading to incomplete asset life cycle tracking and reporting issues.|

## Filters

Enables narrowing the data shown in graphs and metrics based on model category, date range, or stale CI threshold.

|Name|Type|Description|
|----|----|-----------|
|Model categories|List|Filters CIs based on the selected model categories.|
|Date range|Date|Filters the dashboard data based on the selected date range.|
|Stale CI|List|Filters stale CIs based on the number of days since their last update. Available values: `7`, `14`, `30`, `60`, and `90` days.|

## CIs missing model data and other key attributes

Displays key metrics related to CIs missing model details, ownership, and other key attributes, leading to incomplete records and operational inefficiencies.

|Card|Description|Indicators|
|----|-----------|----------|
|CIs missing model name|Operational CIs not associated with a model ID or associated with a model ID missing a name.|[CIs missing model name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|
|CIs missing model number|Operational CIs not associated with a model ID or associated with a model ID missing a model number.|[CIs missing model number](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|
|CIs missing model manufacturer|Operational CIs not associated with a model ID or associated with a model ID missing a manufacturer.|[CIs missing manufacturer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|
|CIs missing model ID|Operational CIs not associated with a model ID.|[CIs missing model ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|
|CIs missing assigned to|Operational CIs not assigned to a specific user, leading to unclear ownership and delayed action.|[CIs missing assigned to](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|
|CIs missing location|Operational CIs not associated with a location, leading to gaps in asset tracking and service mapping.|[CIs missing location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|
|CIs missing owner|Operational CIs not associated with an owner, leading to unclear accountability and delayed issue resolution.|[CIs missing owner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|
|CIs missing managed by group|Operational CIs not managed by a specific ownership group, leading to inefficient support assignment and operational risk.|[CIs missing managed by group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|
|CIs missing serial number|Operational CIs missing a serial number, leading to issues with duplicate identification.|[CIs missing serial number](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)|

**Note:** Select **Show more** in the CIs missing model data and other key attributes section to view all the cards.

## CI data quality issues

Displays key metrics related to CIs that haven’t been updated or may have duplicate records, leading to outdated information and inconsistencies in the CMDB.

<table id="table_r1m_mmj_fgc"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

CIs not updated

</td><td>

Operational CIs not updated, causing data gaps and inaccuracies in the CMDB. When you select a segment on the CIs not updated chart, the KPI Details page title reflects the Stale CI filter value selected at the time. For example, CIs not updated in last 30 days.

</td><td>

[CIs not updated in last 7 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)[CIs not updated in last 14 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

[CIs not updated in last 30 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

[CIs not updated in last 60 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

[CIs not updated in last 90 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

**Note:** The CIs not updated card data is additionally filtered based on the Stale CI filter. See [Filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard.md).

</td></tr><tr><td>

Duplicate CIs

</td><td>

Operational CIs identified as duplicates based on key matching attributes, causing data redundancy.

</td><td>

[Hardware CIs group by](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

</td></tr></tbody>
</table>## CI and asset-related issues

Displays key metrics related to mismatches and missing links between CIs and assets, leading to incomplete asset life cycle tracking and reporting issues.

<table id="table_ck3_zmj_fgc"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

CIs missing asset

</td><td>

Operational CIs not associated with an asset record, leading to incomplete asset life cycle tracking.

</td><td>

[CIs missing asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

</td></tr><tr><td>

Virtual CIs with asset

</td><td>

Virtual assets created for virtual CIs that are operational, leading to inaccurate consumption of HAM licenses.

</td><td>

[Assets created for virtual CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

</td></tr><tr><td>

Assets missing CI

</td><td>

Assets without a matching CI, caused by CIs not being discoverable on the network.

</td><td>

[Assets missing CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

</td></tr><tr><td>

CI install status vs. asset state

</td><td>

All CIs where the install status matches or differs from the corresponding asset state.

</td><td>

[CI install status vs. asset state matched](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)[CI install status vs. asset state mismatched](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-dashboard-indicators.md)

</td></tr></tbody>
</table>