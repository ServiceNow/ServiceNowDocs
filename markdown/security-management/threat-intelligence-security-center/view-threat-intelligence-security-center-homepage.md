---
title: TISC Workspace
description: View a centralized dashboard of threat intelligence data including feeds overview, trending threats, and intelligence sharing metrics. Monitor your security posture with trending intelligence data.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Threat Intelligence Security Center, Security Operations]
---

# TISC Workspace

View a centralized dashboard of threat intelligence data including feeds overview, trending threats, and intelligence sharing metrics. Monitor your security posture with trending intelligence data.

## Before you begin

Access to the Home page is required to visualize threat intelligence data.

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat intelligence Security Center**.

    The TISC Home page is displayed.

    ![Screen shot showing the TISC home page dashboard with threat intelligence trending data and charts.](../image/tisc-homepage-view.png)

2.  Review the TISC home page widgets.

    The home page view consists of three different tabs: **Feeds Overview**, **Trending Threats**, and **Intelligence Sharing**. The content on the home page comes from various sources such as observables, indicators, and data feeds.

    1.  Select the **Feeds Overview** tab to view different sources where data is ingested and sources configured for data ingestion.

        |Widget Name|Description|Action|
        |-----------|-----------|------|
        |Number of Sources|Displays the number of sources by status such as draft, enabled, and turned off in the application.|Selecting this widget opens the list page with filtered records.|
        |Active Sources by Source Type|Displays the distribution of active sources by source type.|Selecting this widget opens the list page with filtered records.|
        |Active Sources by Feed Format|Displays the number of enabled sources by Feed Type.|Selecting this widget opens the list page with filtered records.|
        |Total Active Observables \(30 days\)|Displays the top 10 sources by volume of intelligence records that were created in the last 30 days.|Selecting this widget opens the KPI details page for the selected filter in a new tab.|
        |Active Observables by Type|Displays the top total volume of observable aggregates that were created in the last 30 days.|Selecting this widget opens the KPI details page for the selected filter in a new tab.|
        |Active Indicators by Pattern Type|Displays the total volume of Indicator aggregates by pattern type that were created in the last 30 days.|Selecting this widget opens the KPI details page for the selected filter in a new tab.|
        |Total Active Indicators \(30 days\)|Displays the total volume of indicator aggregates that were created in the last 30 days.|Selecting this widget opens the KPI details page for the selected filter in a new tab.|
        |Top Sources by False Positives Count \(30 days\)|Displays the total volume of False Positive observables that were created in the last 30 days.|Selecting this widget opens the list page with filtered records.|

    2.  Select the **Trending Threats** tab to view trending threats.

<table id="table_qtn_zpy_g1c"><thead><tr><th>

Widget Name

</th><th>

Description

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Latest Reports \(Top 10\)

</td><td>

Displays the list of reports and links - Top 10 order by published date.

</td><td>

Selecting a record from this list view opens it in a new tab on the home page.

</td></tr><tr><td>

Latest RSS Feeds \(Top 10\)

</td><td>

Displays the list of RSS feeds and links - Top 10 order by published date.

</td><td>

Selecting a record from this list view opens it in a new tab on the home page.

</td></tr><tr><td>

Active Observables by Threat Score Range \(30 days\)

</td><td>

Displays the observables count that were created in the last 30 days distributed by Threat Score ranges.

</td><td>

Selecting this widget opens the KPI details page for the selected filter in a new tab.

</td></tr><tr><td>

Active Observables by Reputation \(30 days\)

</td><td>

Displays the observables count that were created in the last 30 days distributed by Reputation.

</td><td>

Selecting this widget opens the KPI details page for the selected filter in a new tab.

</td></tr><tr><td>

Top tags \(30 Days\)

</td><td>

Displays the top tags on the records created in the last 30 days based on the frequency of usage.

</td><td>

Select a tag from the chart and this opens the list view filtered by the selected tag.-   A horizontal bar chart displaying the most frequently used tags.
-   Indicates which tags are commonly applied to observables or feeds.
-   Helps identify trending classifications or recurring patterns in threat data.


</td></tr><tr><td>

Most Targeted Sectors \(30 days\)

</td><td>

Displays the top 10 sectors ranked by activities reported that were created in the last 30 days.

</td><td>

Select a sector in the chart and this opens the list view filtered by the selected sector.-   A bar chart highlighting sectors \(such as Commercial, Government, Aerospace, and so on\) most targeted by threats.
-   Shows the frequency of targeting per sector.
-   Use this to understand industry specific threat trends and prioritization.


</td></tr></tbody>
</table>    3.  Select the **Intelligence Sharing** tab to view intelligence sharing information.

        |Widget Name|Description|Action|
        |-----------|-----------|------|
        |Inbound intelligence - Record Count \(30 days\)|Displays the number of inbound intelligence records received in the last 30 days, categorized by type \(Observable, Object, Indicator\).|Selecting this widget opens the list page with filtered records.|
        |Outbound intelligence - Record Count \(30 days\)|Displays the number of outbound intelligence records shared in the last 30 days, categorized by type \(Observable, Object, Indicator\).|Selecting this widget opens the list page with filtered records.|
        |Inbound intelligence - Distribution by Status \(30 days\)|Displays the distribution of inbound intelligence records by status over the last 30 days.|Selecting this widget opens the list page with filtered records.|
        |Outbound intelligence - Distribution by Status \(30 days\)|Displays the distribution of outbound intelligence records by status over the last 30 days.|Selecting this widget opens the list page with filtered records.|
        |Inbound intelligence - Top Sharing Profile \(30 days\)|Displays the top profiles based on inbound intelligence received over the last 30 days.|Selecting this widget opens the list page with filtered records.|
        |Outbound intelligence - Top Shared Profile \(30 days\)|Displays the top profiles based on outbound intelligence shared over the last 30 days.|Selecting this widget opens the list page with filtered records.|
        |Inbound intelligence - Most Shared Types \(30 days\)|Displays the most frequently received intelligence types \(Object, Indicator, Observable\) over the last 30 days.|Selecting this widget opens the list page with filtered records.|
        |Outbound intelligence - Most Shared Types \(30 days\)|Displays the most frequently shared intelligence types \(Object, Indicator, Observable\) over the last 30 days.|Selecting this widget opens the list page with filtered records.|
        |Inbound intelligence - Distribution by Format \(30 days\)|Displays the format distribution \(for example, MISP, STIX\) of inbound intelligence over the last 30 days.|Selecting this widget opens the list page with filtered records.|
        |Outbound intelligence - Distribution by Format \(30 days\)|Displays the format distribution \(for example, MISP, STIX\) of outbound intelligence over the last 30 days.|Selecting this widget opens the list page with filtered records.|


**Parent Topic:**[Explore](../reference/threat-intelligence-security-center-overview.md)

**Related topics**  


[TISC Key terminology](../reference/tisc-key-terminology.md)

