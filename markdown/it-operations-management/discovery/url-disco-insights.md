---
title: URL Discovery Insights dashboard
description: The Discovery Admin Workspace URL Discovery Insights dashboard displays captured data and analytics for web domains accessed on managed Windows and macOS devices.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# URL Discovery Insights dashboard

The Discovery Admin Workspace URL Discovery Insights dashboard displays captured data and analytics for web domains accessed on managed Windows and macOS devices.

To access the dashboard, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **URL Discovery Insights**.

![URL Discovery insights dashboard](../image/url-disco-insights-dash.png)

## Prerequisites

-   **Verify that you have the required setup**
    -   Australia, Zurich, or YP6 or later version of the ServiceNow AI Platform
    -   Agent Client Collector for Visibility - Content \(ACC-VC\) v1.7.0 or later
    -   URL Discovery and Monitoring v1.0.0 or later
    -   Discovery Admin Workspace v1.14.0 or later
-   **Enable the data collection**

    Role required: discovery\_admin or admin

    Set the **sn\_acc\_vis\_content.enable\_full\_monitoring** property to **True**.

    For more information, see [Collect web usage data using Agent Client Collector for Visibility - Content](../../agent-client-collector/task/collect-web-data-usage-accvc.md).


## Required ServiceNow AI Platform roles

-   discovery\_admin
-   admin

## Key features

The URL Discovery insights dashboard enables you to make data-driven decisions through powerful visualizations. The data is extracted from the Application Domain \[sn\_acc\_vis\_content\_application\_domain\] table.

Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), then select **Refresh** to refresh the data for each visualization in this section.

<table id="table_jsk_zl3_cfc"><thead><tr><th>

Report title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All visited URLs

</td><td>

Data count

</td><td>

Displays the total number of URLs visited across managed devices since a given date.**Note:** This data count displays only when Broad discovery is enabled.

</td></tr><tr><td>

Top 5 URLs with the most visits

</td><td>

Bar chart

</td><td>

Displays the five URLs with the highest visit counts across managed devices since a given date.

</td></tr><tr><td>

Targeted URLs visited by category

</td><td>

Donut chart

</td><td>

Displays the distribution of targeted URL visits grouped by URL category since a given date.

</td></tr></tbody>
</table>**Note:** Daily aggregation jobs update domain-level metrics, including total page views and last accessed time. Data may not reflect activity from the current day until the job has run.

## Targeted URLs visited

This section lists the targeted URLs visited across managed devices since a given date. Targeted URLs are those configured for monitoring in **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Settings** &gt; **URL Discovery**. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

Select a URL from the list to view detailed information about it. Select the filter icon \(![filter icon](../image/filter-icon-daw.png)\) to apply filters to the table.

## Other URLs visited

The Broad URLs visited list displays URLs accessed on managed devices that are not in the targeted URLs list and is populated only when broad URL discovery is enabled. The list includes the URL and the number of hits recorded for each domain. To add a URL to your targeted discovery list, select the check box next to the URL and select **Add to targeted discovery**. In the dialog, enter the following information:

|Field|Description|
|-----|-----------|
|Internal or External|Indicates whether the domain is internal or external. The default value is External.|
|Category|The URL category to assign to the domain.|
|Product|The product associated with the domain.|
|Publisher|The publisher of the product associated with the domain.|
|Application Service|The application service associated with the domain.|

Select **Save** to add the URL to the Targeted URL discovery. The URL is then monitored and appears in the **Targeted URLs visited** tab.

Select the filter icon \(![filter icon](../image/filter-icon-daw.png)\) to apply filters to the table.

