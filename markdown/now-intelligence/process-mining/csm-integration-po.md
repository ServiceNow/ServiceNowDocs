---
title: Content pack for Customer Service Management
description: Using the Process Mining content pack for Customer Service Management enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.Use the SLA breach analysis project in Process Mining to identify and analyze cases where service level agreements \(SLAs\) have been violated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/csm-integration-po.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Automatic content pack delivery, Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Content pack for Customer Service Management

Using the Process Mining content pack for Customer Service Management enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.

This content pack loads automatically when CSM is installed on your instance and the relevant tables are present. For more information, see [Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md).

## Templates shipped with content pack

|Content pack|Template name|Table|
|------------|-------------|-----|
|CSM|Standard template for Cases|sn\_customerservice\_case|

## What you get with this content pack

This content pack analyzes your customer service case processes. It gives you visibility into common process issues, such as:

-   Cases that take longer than expected to resolve
-   Rework, such as cases that get reopened or bounced back between teams
-   Deviations from the expected process flow
-   Work that stalls with a particular team or agent longer than expected

## End user and roles

If you have the required roles, you can use Analyst workbench to access the visualized process workflow data, and tools for analyzing the data related to customer service cases. For more information, see [Analyst workbench page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/analyst-workbench-dashboard.md).

The following combinations of roles are required for using the Process Mining application with Customer Service Management.

|Process Mining role|Customer Service Management role|
|-------------------|--------------------------------|
|sn\_process\_mining\_admin|sn\_customerservice\_manager|
|sn\_process\_mining\_power\_user|sn\_customerservice\_manager|
|sn\_process\_mining\_analyst|sn\_customer\_service\_agent|

**Parent Topic:**[Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md)

## SLA Breach Analysis project

Use the SLA breach analysis project in Process Mining to identify and analyze cases where service level agreements \(SLAs\) have been violated.

The SLA breach analysis project provides insights into the root causes of breaches, highlights bottlenecks, and suggests improvements to optimize process performance.

### SLA breach analysis overview

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
</table>### Using the SLA Breach Analysis project

Use the SLA Breach Analysis project to analyze the reasons why customers are breaching SLAs and help them get to the root cause. This project is available with the [Process Mining Content Pack for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/csm-integration-po.md) \(sn\_csm\_po\).

To access the SLA Breach Analysis project:

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.
2.  Select **All** to display the use case projects.
3.  Select **SLA Breach Analysis Project**.
4.  Select the More options menu.
5.  Select **Mine Project \(Full\)**.
6.  On the Summary and Insights tab you can view the following information:
    -   Project Metrics: Displays metric data such as Average time to completion of records over time.
    -   Improvement Opportunities: Displays metric data and a list of cases with different types of SLA breaches, such as Ping-Pong \(case reassignment\) and Extreme duration.
7.  To view the process map for a case, select **Action** and then select **View in workbench** to display the [Analyst Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/analyst-workbench-dashboard.md).

    Use this workbench to access the visualized process workflow data and tools for analyzing the data related to SLA breaches.

    For example, if a case is reassigned to multiple assignment groups, you can view the following information:

    -   Case table map: View the different assignment groups from process start to end.
    -   Task SLA map: View the points at which the case is breaching the SLA.
8.  Select a node or transition line within a map to view additional details about the selected item in a modal window.

    For more information about using Analyst workbench, including breakdown filters and process maps, see the details in the [Analyst Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/analyst-workbench-dashboard.md) topic.


