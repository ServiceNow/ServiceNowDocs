---
title: Home page in TISC Workspace
description: The TISC home page serves the landing page and provides a summary of Feeds Overview, Trending Threats, and Intelligence Sharing enabling visualization of threat intelligence data.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Threat Intelligence Security Center, Security Operations]
---

# Home page in TISC Workspace

The TISC home page serves the landing page and provides a summary of **Feeds Overview**, **Trending Threats**, and **Intelligence Sharing** enabling visualization of threat intelligence data.

## Before you begin

Role required: sn\_sec\_tisc.analyst

On the Home page, you can perform the following procedure to visualize the threat intelligence data.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Security Center**.

    The TISC Home page is displayed.

    ![TISC home page](../image/tisc-homepage-view.png)

2.  View the TISC home page with different widgets data.

    The home page view consists of three different tabs: **Feeds Overview**, **Trending Threats**, and **Intelligence Sharing**. The content on the home page comes from various sources such as observables, indicators, and data feeds.

    1.  **Feeds Overview**: This tab provides a high level overview of different sources that the data is ingested and sources that are configured for the data ingestion.

        |Widget Name|Description|Action|
        |-----------|-----------|------|
        |Number of Sources|Displays the number of sources by status such as draft, enabled, and disabled in the system.|When this widget is clicked, the list page is opened with the filtered records.|
        |Active Sources by Source Type|Displays the distribution of active sources by source type.|When this widget is clicked, the list page is opened with the filtered records.|
        |Active Sources by Feed Format|Displays the number of enabled sources by Feed Type.|When this widget is clicked, the list page is opened with the filtered records.|
        |Total Active Observables \(30 days\)|Displays the top 10 sources by volume of intelligence records that were created in the last 30 days.|When this widget is clicked, the KPI details page of the widget for the selected filter is opened in a new tab.|
        |Active Observables by Type|Displays the top total volume of observable aggregates that were created in the last 30 days.|When this widget is clicked, the KPI details page of the widget for the selected filter is opened in a new tab.|
        |Active Indicators by Pattern Type|Displays the total volume of Indicator aggregates by pattern type that were created in the last 30 days.|When this widget is clicked, the KPI details page of the widget for the selected filter is opened in a new tab.|
        |Total Active Indicators \(30 days\)|Displays the total volume of indicator aggregates that were created in the last 30 days.|When this widget is clicked, the KPI details page of the widget for the selected filter is opened in a new tab.|
        |Top Sources by False Positives Count \(30 days\)|Displays the total volume by of False Positive observables that were created in the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|

    2.  **Trending Threats**: This tab provides a high level overview of the trending threats.

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

When this widget is clicked, the KPI details page of the widget for the selected filter is opened in a new tab.

</td></tr><tr><td>

Active Observables by Reputation \(30 days\)

</td><td>

Displays the observables count that were created in the last 30 days distributed by Reputation.

</td><td>

When this widget is clicked, the KPI details page of the widget for the selected filter is opened in a new tab.

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
-   Useful for understanding industry-specific threat trends and prioritization.


</td></tr></tbody>
</table>    3.  **Intelligence Sharing**: This tab provides a high level overview of the intelligence sharing.

        |Widget Name|Description|Action|
        |-----------|-----------|------|
        |Inbound Intel - Record Count \(30 days\)|Displays the number of inbound intel records received in the last 30 days, categorized by type \(Observable, Object, Indicator\).|When this widget is clicked, the list page is opened with the filtered records.|
        |Outbound Intel - Record Count \(30 days\)|Displays the number of outbound intel records shared in the last 30 days, categorized by type \(Observable, Object, Indicator\).|When this widget is clicked, the list page is opened with the filtered records.|
        |Inbound Intel - Distribution by Status \(30 days\)|Displays the distribution of inbound intelligence records by status over the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|
        |Outbound Intel - Distribution by Status \(30 days\)|Displays the distribution of outbound intelligence records by status over the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|
        |Inbound Intel - Top Sharing Profile \(30 days\)|Displays the top profiles based on inbound intel received over the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|
        |Outbound Intel - Top Shared Profile \(30 days\)|Displays the top profiles based on outbound intel shared over the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|
        |Inbound Intel - Most Shared Types \(30 days\)|Displays the most frequently received intel types \(Object, Indicator, Observable\) over the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|
        |Outbound Intel - Most Shared Types \(30 days\)|Displays the most frequently shared intel types \(Object, Indicator, Observable\) over the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|
        |Inbound Intel - Distribution by Format \(30 days\)|Displays the format distribution \(e.g., MISP, STIX\) of inbound intel over the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|
        |Outbound Intel - Distribution by Format \(30 days\)|Displays the format distribution \(e.g., MISP, STIX\) of outbound intel over the last 30 days.|When this widget is clicked, the list page is opened with the filtered records.|


**Parent Topic:**[Explore](../reference/threat-intelligence-security-center-overview.md)

**Related topics**  


[TISC Key terminology](../concept/tisc-key-terminology.md)

