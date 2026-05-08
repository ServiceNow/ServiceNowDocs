---
title: Configure the date range for a Discovery Operations Monitor visualization
description: Update the data time frame for individual visualizations on the Discovery Operations Monitor dashboard. By default, each visualization displays data from the last 7 days. You can extend the time frame up to 30 days, which is the maximum data retention period for this dashboard.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Discovery Operations Monitor dashboard, Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure the date range for a Discovery Operations Monitor visualization

Update the data time frame for individual visualizations on the Discovery Operations Monitor dashboard. By default, each visualization displays data from the last 7 days. You can extend the time frame up to 30 days, which is the maximum data retention period for this dashboard.

## Before you begin

Verify you're using Discovery Admin Workspace v1.15.0.

Role required: discovery\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **Discovery Operations Monitor**.

2.  Select **Edit**.

3.  Select the visualization you want to update.

4.  In the Configuration panel, under Data Sources, select the data source card for the visualization you want to update.

    For example, for the Transaction Duration visualization, select the **Discovery Transaction Load** card.![Discovery Transaction Load card](../image/disco-op-monitor-data-source.png)

    The Edit data source page displays.

5.  In the Filters section, select **Edit**.

6.  Select the **Last 7 Days** drop-down list to choose a new time frame for the filter condition.

    **Warning:** The list includes options beyond 30 days, but the dashboard retains data for a maximum of 30 days. Selecting a longer time frame doesn't display additional data.

7.  Select **Apply**.

    You're returned to the Discovery Operations Monitor dashboard. The visualization updates to display data for the selected time frame.

8.  Select **Exit editing mode**.


**Related topics**  


[Discovery Operations Monitor dashboard](../concept/disco-operations-monitor.md)

[Configure the time interval for a Discovery Operations Monitor visualization](config-interval-disco-op-mon.md)

[bundle-par.common-dashboard-tasks]

