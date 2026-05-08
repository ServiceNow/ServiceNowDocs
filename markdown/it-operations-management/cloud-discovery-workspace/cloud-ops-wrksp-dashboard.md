---
title: Cloud Discovery Workspace dashboard
description: The ServiceNow Cloud Discovery Workspace dashboard provides a summary of the cloud operations of your organization and shows the ServiceNow applications that you can use to manage them.
locale: en-US
release: australia
product: Cloud Discovery Workspace
classification: cloud-discovery-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cloud Discovery Workspace, ITOM Visibility, IT Operations Management]
---

# Cloud Discovery Workspace dashboard

The ServiceNow® Cloud Discovery Workspace dashboard provides a summary of the cloud operations of your organization and shows the ServiceNow applications that you can use to manage them.

**Important:** Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Required ServiceNow AI Platform roles

sn\_cloud\_ops\_ws.cloud\_ops\_admin.

## Access the Cloud Discovery Workspace dashboard

To open the dashboard, navigate to **All** &gt; **Cloud Discovery Workspace**.

## Use cases

<table id="table_brv_npc_ltb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

sn\_cloud\_ops\_ws.cloud\_ops\_admin

</td><td>

-   Gain insight into the trend of CI discovery, trend of Cloud Discovery events, and Cloud Discovery errors
-   Select the cloud provider of your organization.
-   Access the applications that you can use to manage the cloud operations of your organization.

</td></tr></tbody>
</table>## Indicators

Discovery errors today: Count of all Cloud Discovery errors that occurred during the scheduled discoveries over the last 24 hours.

## Reports

The following reports are available in the Cloud Discovery Workspace dashboard:

<table id="table_cb2_yjv_fsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total configuration items

</td><td>

Line and area chart![Line and area chart.](../../../use/reporting/image/icon-area-report-p.png)

</td><td>

cmdb\_ci

</td><td>

This report displays the number of CIs discovered over time.Select the report to view the list of all the configuration items discovered so far. You can select any CI record to view more information about the CI and its multi-source data if available.

</td></tr><tr><td>

Events by provider - last 24 hours

</td><td>

Line chart![Line chart.](../../../use/reporting/image/icon-line-report-p.png)

</td><td>

sn\_cmp\_cloud\_event\_list

</td><td>

This report displays the trend of the cloud events received over the last 24 hours. The report contains a separate trend line for each cloud provider.

</td></tr></tbody>
</table>In addition, the dashboard cards display the applications that you can use to manage the cloud operations of your organization. Use the Cloud provider selection page to select the cloud providers of your organization. The selection helps to customize the menus of the Cloud Discovery Workspace applications and display only the cloud providers that are relevant for your organization.

**Related topics**  


[bundle-platux.list-of-workspaces]

