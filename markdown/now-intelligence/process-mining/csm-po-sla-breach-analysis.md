---
title: SLA Breach Analysis project
description: Use the SLA breach analysis project in Process Mining to identify and analyze cases where service level agreements \(SLAs\) have been violated.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Content pack for Customer Service Management, Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# SLA Breach Analysis project

Use the SLA breach analysis project in Process Mining to identify and analyze cases where service level agreements \(SLAs\) have been violated.

The SLA breach analysis project provides insights into the root causes of breaches, highlights bottlenecks, and recommends improvements to optimize process performance.

## SLA breach analysis overview

The following table describes the steps that the system takes to identify and analyze SLA breaches.

<table id="table_l5y_w5m_5fc"><thead><tr><th>

Step

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

1

</td><td>

Breach identification

</td><td>

-   Automatically detects and flags SLA breaches based on predefined thresholds.
-   Displays breach details including timestamps, duration, and associated SLA type.

</td></tr><tr><td>

2

</td><td>

Surfacing of improvement areas

</td><td>

-   Identifies key process inefficiencies contributing to SLA breaches.
-   Highlights potential root causes such as long routing time, extended idle time, and excessive wait times.

</td></tr><tr><td>

3

</td><td>

Parent and child table process map

</td><td>

-   Provides a process map that visualizes the relationship between the case table \(parent\) and task SLA table \(child\).
-   Ensures clear mapping of SLA events to corresponding process steps for deeper analysis.

</td></tr><tr><td>

4

</td><td>

Breakdown by channels, product, and assignment group

</td><td>

-   Enables filtering and analysis based on customer interaction channels \(for example, email, phone, or chat\).
-   Supports SLA breach breakdown by product categories for targeted process improvements.
-   Allows segmentation of breaches by assignment groups to pinpoint accountability and workload distribution.

</td></tr></tbody>
</table>## Using the SLA Breach Analysis project

Use the SLA Breach Analysis project to analyze the reasons why customers are breaching SLAs and help them get to the root cause. This project is available with the [Process Mining Content Pack for CSM](csm-integration-po.md) \(sn\_csm\_po\).

To access the SLA Breach Analysis project:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Select **All** to display the use case projects.
3.  Select **SLA Breach Analysis Project**.
4.  Select the More options menu.
5.  Select **Mine Project \(Full\)**.
6.  On the Summary and Insights tab you can view the following information:
    -   Project Metrics: Displays metric data such as Average time to completion of records over time.
    -   Improvement Opportunities: Displays metric data and a list of cases with different types of SLA breaches, such as Ping-Pong \(case reassignment\) and Extreme duration.
7.  To view the process map for a case, select **Action** and then select **View in workbench** to display the [Analyst Workbench](analyst-workbench-dashboard.md).

    Use this workbench to access the visualized process workflow data and tools for analyzing the data related to SLA breaches.

    For example, if a case is reassigned to multiple assignment groups, you can view the following information:

    -   Case table map: View the different assignment groups from process start to end.
    -   Task SLA map: View the points at which the case is breaching the SLA.
8.  Select a node or transition line within a map to view additional details about the selected item in a modal window.

    For more information about using Analyst workbench, including breakdown filters and process maps, see the details in the [Analyst Workbench](analyst-workbench-dashboard.md) topic.


**Parent Topic:**[Content pack for Customer Service Management](csm-integration-po.md)

