---
title: Cloud Configuration Governance dashboard
description: Cloud Configuration Governance is a tool used to manage the configuration of the cloud resources as per your organizational standards and established security standards. Use the dashboard to review the health score of the cloud, policy violation statistics, policy violation trend, remediations overview, and more.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance dashboard

Cloud Configuration Governance is a tool used to manage the configuration of the cloud resources as per your organizational standards and established security standards. Use the dashboard to review the health score of the cloud, policy violation statistics, policy violation trend, remediations overview, and more.

![Cloud Configuration Governance dashboard.](../image/ccg-dashboard.gif "Cloud Configuration Governance dashboard")

## Required ServiceNow AI Platform roles

sn\_itom\_ccg.ccg\_operator or sn\_itom\_ccg.report\_viewer roles are required to view the dashboard and its widgets.

## Access the Cloud Configuration Governance dashboard

To open the dashboard, navigate to **Cloud Configuration Governance** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_cz3_stk_hsb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

sn\_itom\_ccg.ccg\_operator or sn\_itom\_ccg.report\_viewer

</td><td>

-   Review the cloud heath score.
-   Time taken to remediate the identified policy violations.
-   Understand the trend of the policy violation.

</td></tr></tbody>
</table>## Reports

<table id="table_hz3_stk_hsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud health score

</td><td>

Speedo chart

</td><td>

sn\_itom\_ccg\_scan\_summary

</td><td>

Percentage of scanned cloud resources that doesn’t have any audit issue.

</td></tr><tr><td>

Violating resources

</td><td>

Stacked bar chart

</td><td>

sn\_itom\_ccg\_scan\_summary

</td><td>

Severity of the detected audit issues per cloud resource type.

</td></tr><tr><td>

Violations count

</td><td>

Donut chart

</td><td>

sn\_itom\_ccg\_violation\_stats

</td><td>

Violation per severity of the audit issue.

</td></tr><tr><td>

Scanned resources

</td><td>

Donut chart

</td><td>

sn\_itom\_ccg\_scan\_summary

</td><td>

Number of cloud resources scanned per cloud resource type.Use the **CCG Drilldown Filters** to filter the data and visualize the data of interest.

</td></tr><tr><td>

Issues

</td><td>

Horizontal bar chart

</td><td>

sn\_itom\_ccg\_audit\_stats

</td><td>

Number of violations reported per violation definition.The chart can display a maximum of 10 bars, that is one per violation definition type. If the data contains more than 10 violation definition types, all the additional violation definition types are merged under the **Others** bar.

 Use the **CCG Drilldown Filters** to filter the data and visualize the data of interest.

</td></tr><tr><td>

Policy compliance

</td><td>

Embedded lists

</td><td>

sn\_itom\_ccg\_policy\_compliance\_stats

</td><td>

Displays the following information for the given policy:-   Count of compliant resources
-   Count of non-compliant resources

</td></tr><tr><td>

Policy set compliance

</td><td>

Embedded lists

</td><td>

sn\_itom\_ccg\_policy\_set\_compliance\_stats

</td><td>

Displays the following information for the given policy set:-   Count of compliant resources
-   Count of non-compliant resources

</td></tr><tr><td>

Total issues remediated

</td><td>

Half donut chart

</td><td>

sn\_itom\_ccg\_remediation\_daily\_trend

</td><td>

Remediations performed per violation definition type.

</td></tr><tr><td>

Remediations by type

</td><td>

Pie chart

</td><td>

sn\_itom\_ccg\_remediation\_daily\_trend

</td><td>

Remediations performed per cloud resource type.

</td></tr><tr><td>

Remediated on

</td><td>

Half donut chart

</td><td>

sn\_itom\_ccg\_remediation\_daily\_trend

</td><td>

Time taken to remediate the violations.

</td></tr><tr><td>

Trend

</td><td>

Line chart

</td><td>

sn\_itom\_ccg\_daily\_trend

</td><td>

Trend of reporting violations over time.

</td></tr></tbody>
</table>## Filters

|Name|Type|Description|
|----|----|-----------|
|**CCG Drilldown filter**|Choice-based filter|Use this filter to select the cloud provider, cloud account, and regions for visualizing their scanned resources and issues data.|

**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

