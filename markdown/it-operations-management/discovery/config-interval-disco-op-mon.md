---
title: Configure the time interval for a Discovery Operations Monitor visualization
description: Update the data collection time interval for individual visualizations on the Discovery Operations Monitor dashboard. By default, each visualization displays data in 15-minute intervals.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Discovery Operations Monitor dashboard, Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure the time interval for a Discovery Operations Monitor visualization

Update the data collection time interval for individual visualizations on the Discovery Operations Monitor dashboard. By default, each visualization displays data in 15-minute intervals.

## Before you begin

Verify you're using Discovery Admin Workspace v1.15.0.

Role required: discovery\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **Discovery Operations Monitor**.

2.  Select **Edit**.

3.  Select the visualization that you want to update.

    For example, to update the Transaction Duration visualization, select that chart while in editing mode.

4.  In the Configuration panel, under Trendy by, select the edit icon \(![](../../cloud-workspace/image/edit-icon-workspace.png)\) on the Minute by interval end time card.

5.  Select a time interval from the **Interval in minutes** drop-down list.

    ![Interval in minutes drop-down list](../image/disco-op-monitor-interval.png)

    **Warning:** Available intervals include 1, 15, 30, and 60 minutes. Although 1 minute appears in the list, it isn't a supported interval and may produce unreliable results.

6.  Select **Apply**.

    The visualization updates to display data at the new interval.

7.  Select **Save**.

8.  Then, select **Exit editing mode**.


**Related topics**  


[Discovery Operations Monitor dashboard](../concept/disco-operations-monitor.md)

[Configure the date range for a Discovery Operations Monitor visualization](config-time-frame-disco-op-mon.md)

[Common dashboard tasks in the in-line editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/common-dashboard-tasks.md)

