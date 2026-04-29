---
title: Cloud Discovery home page in Cloud Discovery Workspace
description: The Cloud Discovery home page displays a summary of the discoveries triggered through a discovery schedule. You can view the count of CIs discovered and errors encountered over time. You can also select any dashboard report to view additional information.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [Discovery monitoring and issue resolution, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Cloud Discovery home page in Cloud Discovery Workspace

The Cloud Discovery home page displays a summary of the discoveries triggered through a discovery schedule. You can view the count of CIs discovered and errors encountered over time. You can also select any dashboard report to view additional information.

**Important:** Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

![Cloud Discovery dashboard.](../image/cow-cloud-disco-dashboard.gif)

## Required ServiceNow AI Platform roles

sn\_cloud\_ops\_ws.cloud\_ops\_admin

## Access the Cloud Discovery home page

To open the dashboard, navigate to **Cloud Discovery Workspace** &gt; **Cloud Discovery** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_edx_n53_jsb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

sn\_cloud\_ops\_ws.cloud\_ops\_admin

</td><td>

The sn\_cloud\_ops\_ws.cloud\_ops\_admin can review the following information in the Cloud Discovery dashboard: -   30 day discovery runs
-   Upcoming schedules
-   Total configuration items
-   Cloud discovery errors
-   Credentials
-   MID Servers
-   Service accounts
-   Cloud VMs by datacenter

</td></tr></tbody>
</table>## Indicators

-   **Credentials**

    This indicator displays the total count of credentials defined in the system and their breakdown according to cloud provider.

    Select the number mentioned under any credential type to see a filtered list of matching credentials.

-   **Service accounts**

    This indicator displays the total count of service accounts defined in the system and their breakdown according to cloud provider.

    Select the number mentioned under any cloud provider to see a filtered list of matching service accounts.


## Reports

<table id="table_jdx_n53_jsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

30 day discovery runs

</td><td>

Donut chart![Line and area chart.](../../../use/reporting/image/icon-area-report-p.png)

</td><td>

discovery\_status

</td><td>

This report displays the count and the state of the discovery runs over the last 30 days. Cloud Discovery displays the following states in the report:-   Active
-   Canceled
-   Completed

 Select the report to view the list of all the discoveries.

</td></tr><tr><td>

Upcoming schedules

</td><td>

List

</td><td>

discovery\_schedule

</td><td>

This report displays information about up to eight upcoming scheduled discoveries.Select any schedule to view its details.

</td></tr><tr><td>

Total configuration items

</td><td>

Line and area chart![Line and area chart.](../../../use/reporting/image/icon-area-report-p.png)

</td><td>

cmdb\_ci

</td><td>

This report displays the number of CIs discovered over time.Select the report to view the list of all the configuration items discovered so far. You can select any CI record to view more information about the CI and its multi-source data if available.

</td></tr><tr><td>

Cloud discovery errors

</td><td>

Line and area chart![Line and area chart.](../../../use/reporting/image/icon-area-report-p.png)

</td><td>

discovery\_log

</td><td>

This report displays the number of Cloud Discovery errors over time.Select the report to view the list of all Cloud Discovery errors in the Discovery log. Alternatively, you can access this information, by navigating to **Diagnostics** &gt; **Discovery log**.

</td></tr><tr><td>

Credentials

</td><td>

Indicator

</td><td>

discovery\_credential

</td><td>

This report displays the total count of credentials defined in the system and their breakdown per cloud provider.Select the number mentioned under any credential type to see a filtered list of matching credentials.

</td></tr><tr><td>

MID servers

</td><td>

Donut chart![Donut chart.](../../../use/reporting/image/icon-donut-report-p.png)

</td><td>

ecc\_agent

</td><td>

This report displays the total count of MID Servers and their status.

</td></tr><tr><td>

Service accounts

</td><td>

Indicator

</td><td>

cmdb\_ci\_cloud\_service\_account

</td><td>

This report displays the total count of service accounts defined in the system and their breakdown per cloud provider.Select the number mentioned under any cloud provider to see a filtered list of matching service accounts.

</td></tr><tr><td>

Cloud VMs by datacenter

</td><td>

Horizontal bar chart![Horizontal bar chart.](../../../use/reporting/image/icon-horizontal-bar-report-p.png)

</td><td>

sn\_disco\_cd\_vm\_analytics

</td><td>

This report displays the count of VMs discovered per datacenter.Cloud Discovery displays this report for Microsoft Azure, Amazon Web Services \(AWS\), and vCenter datacenters only.

</td></tr></tbody>
</table>