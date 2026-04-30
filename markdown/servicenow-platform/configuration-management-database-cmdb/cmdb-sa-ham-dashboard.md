---
title: Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for HAM
description: The CMDB success advisor for HAM dashboard enables CMDB administrators to identify and address data quality issues specific to HAM in the Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Use HAM advisor, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Monitoring CMDB data quality using dashboard metrics in CMDB success advisor for HAM

The CMDB success advisor for HAM dashboard enables CMDB administrators to identify and address data quality issues specific to HAM in the Configuration Management Database \(CMDB\).

**Important:** When you select a segment or count on a chart from a CMDB success advisor dashboard, the KPI Details page opens. On the page, you can analyze how a specific metric trends over time. Additionally, the Remediation actions panel appears when remediation actions are available for that card. Use the panel to improve the quality of CMDB. To learn more, see [KPI Details](https://www.servicenow.com/docs/access?context=kpi-details&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) and [Improving CMDB data quality for HAM](cmdb-sa-ham-remediation.md).

![CMDB success advisor for HAM dashboard overview.](../image/cmdb-sa-ham-dashboard.png)

## Access the dashboard

To open the dashboard, select **View insights** for HAM on the CMDB success advisor landing page. See [Viewing the CMDB success advisor landing page](cmdb-sa-landing-page.md).

**Note:** The CMDB success advisor for HAM dashboard is available only after the setup process is complete. For more information, see [Set up CMDB success advisor for HAM](cmdb-sa-ham-config-settings.md).

## Required roles

|Role|Description|
|----|-----------|
|sn\_cmdb\_admin|Required to access the dashboard.|
|pa\_viewer|Required to filter data by model categories.|
|pa\_data\_collector|Required to view the last updated data timestamp on the dashboard.|

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

**Important:** The dashboard data is filtered based on the Selected model categories and Date range filters. See [Filters](cmdb-sa-ham-dashboard.md#section_an4_nnj_fgc).

|Feature|Description|
|-------|-----------|
|CIs by model category|Displays the breakdown of operational CIs by associated model category to highlight CI distribution in the CMDB.|
|CIs by data integration source|Displays the breakdown of operational CIs by data integration source to highlight their contribution to CMDB population.|
|[CIs missing model data and other key attributes](cmdb-sa-ham-dashboard.md#section_tgc_yz3_fgc)|Displays key metrics related to CIs missing model details, ownership, and other key attributes, leading to incomplete records and operational inefficiencies.|
|[CI data quality issues](cmdb-sa-ham-dashboard.md#section_rzg_2mj_fgc)|Displays key metrics related to CIs that have not been updated or may have duplicate records, leading to outdated information and inconsistencies in the CMDB.|
|[CI and asset-related issues](cmdb-sa-ham-dashboard.md#section_hmb_vmj_fgc)|Displays key metrics related to mismatches and missing links between CIs and assets, leading to incomplete asset life cycle tracking and reporting issues.|

## Filters

Enables narrowing the data shown in graphs and metrics based on model category, date range, or stale CI threshold.

<table id="table_dsk_4nj_fgc"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selected model categories

</td><td>

List

</td><td>

Filters CIs based on the selected model categories.**Note:** Requires the `pa_viewer` role.

</td></tr><tr><td>

Date range

</td><td>

Date

</td><td>

Filters the dashboard data based on the selected date range.

</td></tr><tr><td>

Stale CI

</td><td>

List

</td><td>

Filters stale CIs based on the number of days since their last update. Available values: `7`, `14`, `30`, `60`, and `90` days.

</td></tr></tbody>
</table>## CIs missing model data and other key attributes

Displays key metrics related to CIs missing model details, ownership, and other key attributes, leading to incomplete records and operational inefficiencies.

|Card|Description|Indicators|
|----|-----------|----------|
|CIs missing model name|Operational CIs not associated with a model ID or associated with a model ID missing a name.|[CIs missing model name](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-model-name)|
|CIs missing model number|Operational CIs not associated with a model ID or associated with a model ID missing a model number.|[CIs missing model number](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-model-number)|
|CIs missing model manufacturer|Operational CIs not associated with a model ID or associated with a model ID missing a manufacturer.|[CIs missing manufacturer](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-manufacturer)|
|CIs missing model ID|Operational CIs not associated with a model ID.|[CIs missing model ID](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-model-id)|
|CIs missing assigned to|Operational CIs not assigned to a specific user, leading to unclear ownership and delayed action.|[CIs missing assigned to](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-assigned-to)|
|CIs missing location|Operational CIs not associated with a location, leading to gaps in asset tracking and service mapping.|[CIs missing location](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-location)|
|CIs missing owner|Operational CIs not associated with an owner, leading to unclear accountability and delayed issue resolution.|[CIs missing owner](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-owner)|
|CIs missing managed by group|Operational CIs not managed by a specific ownership group, leading to inefficient support assignment and operational risk.|[CIs missing managed by group](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-managed-by-grp)|
|CIs missing serial number|Operational CIs missing a serial number, leading to issues with duplicate identification.|[CIs missing serial number](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-serial-number)|

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

Operational CIs not updated, causing data gaps and inaccuracies in the CMDB.

</td><td>

[CIs not updated in last 7 days](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-not-updated-7)[CIs not updated in last 14 days](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-not-updated-14)

[CIs not updated in last 30 days](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-not-updated-30)

[CIs not updated in last 60 days](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-not-updated-60)

[CIs not updated in last 90 days](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-not-updated-90)

**Note:** The CIs not updated card data is additionally filtered based on the Stale CI filter. See [Filters](cmdb-sa-ham-dashboard.md#section_an4_nnj_fgc).

</td></tr><tr><td>

Duplicate CIs

</td><td>

Operational CIs identified as duplicates based on key matching attributes, causing data redundancy.

</td><td>

[Hardware CIs group by](../reference/cmdb-sa-ham-dashboard-indicators.md#hw-ci-group-by)

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

[CIs missing asset](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-missing-asset)

</td></tr><tr><td>

Virtual CIs with asset

</td><td>

Virtual assets created for virtual CIs that are operational, leading to inaccurate consumption of HAM licenses.

</td><td>

[Assets created for virtual CIs](../reference/cmdb-sa-ham-dashboard-indicators.md#asset-created-virtual-ci)

</td></tr><tr><td>

Assets missing CI

</td><td>

Assets without a matching CI, caused by CIs not being discoverable on the network.

</td><td>

[Assets missing CI](../reference/cmdb-sa-ham-dashboard-indicators.md#assets-missing)

</td></tr><tr><td>

CI install status vs. asset state

</td><td>

All CIs where the install status matches or differs from the corresponding asset state.

</td><td>

[CI install status vs. asset state matched](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-install-status-asset-state-matched)[CI install status vs. asset state mismatched](../reference/cmdb-sa-ham-dashboard-indicators.md#ci-install-status-asset-state-mismatched)

</td></tr></tbody>
</table>