---
title: Run historical data collection for Virtual Machine Explorer
description: After installing Discovery Admin Workspace, run historical data collection jobs to populate the Virtual machines with server CI and Virtual machines with no deep dive discovery reports on the Virtual Machine Explorer dashboard.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Virtual Machine Explorer dashboard, Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Run historical data collection for Virtual Machine Explorer

After installing Discovery Admin Workspace, run historical data collection jobs to populate the Virtual machines with server CI and Virtual machines with no deep dive discovery reports on the Virtual Machine Explorer dashboard.

## Before you begin

The application scope must be set to **Global**.

Role required: pa\_data\_collector or admin

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Data Collector** &gt; **Jobs**.

2.  Select the **filter** icon.

3.  **\[Name\]****\[contains\]**`historic`**AND \[Name\]\[contains\]**`VM`.

4.  Run the filter by selecting **Run**.

5.  Select **\[PA VMs with links\] Historic Data Collection** from the table.

6.  Select **Execute Now**.

    The historical data collection job collects data for the last 60 days.

7.  Select the **back** icon to return to the previous table.

8.  Select **\[PA VMs with NO links\] Historic Data Collection** from the table.

9.  Select **Execute Now**.

    The historical data collection job collects data for the last 60 days.


## What to do next

Manually refresh the indicators on the Virtual Machine Explorer dashboard to populate the Virtual machines with server CI and Virtual machines with no deep dive discovery reports, enabling you to view relevant data and trends. For more information, see [Virtual Machine Explorer dashboard](../concept/vm-explorer.md).

