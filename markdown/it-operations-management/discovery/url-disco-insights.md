---
title: URL Discovery insights dashboard
description: The Discovery Admin Workspace URL Discovery insights dashboard displays captured data and analytics for web domains accessed on managed Windows and macOS devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery/url-disco-insights.html
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# URL Discovery insights dashboard

The Discovery Admin Workspace URL Discovery insights dashboard displays captured data and analytics for web domains accessed on managed Windows and macOS devices.

To access the dashboard, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **URL Discovery insights for SAM**.

\[Omitted image "image.url-disco-insights-dash"\] Alt text: URL Discovery insights dashboard

## Prerequisites

-   **Verify that you have the required setup**
    -   ServiceNow AI Platform: Australia release, Zurich release, or Yokohama release, starting with Patch 6
    -   Software Asset Management Professional plugin \(com.snc.samp\)
    -   Agent Client Collector for Visibility - Content \(ACC-VC\), starting with v1.8.0
    -   ITOM URL Discovery, starting with v1.1.0
    -   Discovery Admin Workspace, starting with v1.14.0
-   **Enable the data collection**

    Role required: discovery\_admin or admin

    Set the **sn\_acc\_vis\_content.enable\_full\_monitoring** property to **True**.


## Required ServiceNow AI Platform roles

-   discovery\_admin
-   admin

## Key features

The URL Discovery insights dashboard enables you to make data-driven decisions through visualizations. The data is extracted from the Application Domain \[sn\_acc\_vis\_content\_application\_domain\] table.

Select the **More options** icon \(\[Omitted image "icon-menu-sow.png"\] Alt text: More options icon\), then select **Refresh** to refresh the data for each visualization in this section.

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

This section lists the targeted URLs visited across managed devices since a given date. Targeted URLs are those configured for monitoring in **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Settings** &gt; **URL Discovery**. For more information, see [Discovery Admin Workspace Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-admin-workspace-setup.md).

Select a URL from the list to open its domain details page, which displays domain-level usage metrics including total page views, total accessed time, last accessed time, and the number of distinct users.

**Note:** These metrics are aggregated per domain by the daily aggregation job and may not reflect current-day activity until the job runs.

Select the filter icon \(\[Omitted image "image.filter-icon-daw"\] Alt text: filter icon\) to apply filters to the table.

## Other URLs visited

The Broad URLs visited list displays URLs accessed on managed devices that aren't in the targeted URLs list and is populated only when broad URL discovery is enabled. The list includes the URL and the number of hits recorded for each domain. To add a URL to your targeted discovery list, select the check box next to the URL and select **Add to targeted discovery**. In the dialog, enter the following information:

<table id="table_u4h_nhy_v3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Internal or External

</td><td>

Whether the domain is internal or external. The default value is External.

</td></tr><tr><td>

Category

</td><td>

The URL category to assign to the domain. The Entity Categories \[sn\_acc\_vis\_content\_entity\_category\] table populates the available categories.

</td></tr><tr><td>

Product

</td><td>

The product associated with the domain. The Software Products \[samp\_sw\_product\] table populates the available products.**Note:** Beginning with URL Discovery v1.2.1, this field is optional. However, if you select a product, **Application Service** is set to a required field.

</td></tr><tr><td>

Publisher

</td><td>

The publisher of the product associated with the domain.

</td></tr><tr><td>

Application Service

</td><td>

The application service associated with the domain. The Service Instances \[cmdb\_ci\_service\_auto\] table populates the available services.**Note:** Beginning with URL Discovery v1.2.1, this field is optional unless a Product is selected.

</td></tr></tbody>
</table>Select **Save** to add the URL to the Targeted URL discovery. The URL is then monitored and appears in the **Targeted URLs visited** tab.

Select the filter icon \(\[Omitted image "image.filter-icon-daw"\] Alt text: filter icon\) to apply filters to the table.

**Note:** Mapping a SAM product to a URL requires the sam\_user role.

**Parent Topic:**[Discovery Admin Workspace Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/discovery-admin-workspace-insights.md)

