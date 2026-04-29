---
title: Content pack for Customer Service Management
description: Using the Process Mining content pack for Customer Service Management enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.Analyze a process for customer service cases and identify bottlenecks to minimize delays in the case flow for a better customer experience.Use the SLA breach analysis project in Process Mining to identify and analyze cases where service level agreements \(SLAs\) have been violated.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Content pack for Customer Service Management

Using the Process Mining content pack for Customer Service Management enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.

For more information about enabling the Process Mining Content Pack for CSM, see [Activate content packs](../task/activate-po-content-pack.md).

## End user and roles

If you have the required roles, you can use Analyst workbench to access the visualized process workflow data, and tools for analyzing the data related to customer service cases. For more information, see [Analyst workbench page](analyst-workbench-dashboard.md).

The following combinations of roles are required for using the Process Mining application with Customer Service Management.

|Process Mining role|Customer Service Management role|
|-------------------|--------------------------------|
|sn\_process\_mining\_admin|sn\_customerservice\_manager|
|sn\_process\_mining\_power\_user|sn\_customerservice\_manager|
|sn\_process\_mining\_analyst|sn\_customer\_service\_agent|

## Optimization project for customer service cases

The Process Mining Content Pack for CSM \(sn\_csm\_po\) adds a prebuilt project that includes a predefined **Customer Service Cases** project definition for customer service cases. By default, the **Customer Service Cases** project filters customer service cases for the last two quarters. You can also configure a new process project based on the prebuilt project. For more information, see [Create a project or template using Project Builder](../task/define-workflow-model.md).

The **Customer Service Cases** project includes default activity definitions and breakdown definitions for customer service cases that you can use as they’re or modify them for a custom configuration.

-   Use activity definitions to understand state transitions such as cases transitioning from the work in progress state to the solution proposed state and analyze the linked processes such as Problem \(PRB\) records.
-   Use breakdown definitions to filter records and analyze a process map by categories. For example, you can filter the customer service case data by different channels, products, assignment groups, and locations.

## SLA breach analysis project for customer service cases

The Process Mining Content Pack for CSM \(sn\_csm\_po\) adds a pre-built project that includes a predefined **SLA Breach Analysis** project definition for customer service cases. For more information, see [SLA Breach Analysis project](csm-integration-po.md#).

## Continual Improvement Management initiative for customer service cases

If the Continual Improvement Management \(CIM\) application is enabled, you can also use the CIM project from Analyst workbench to track the progress of improvement initiatives for customer service cases. The improvement initiative and Process Mining projects are automatically linked. For more information, see [Integration with Continual Improvement Management](integrate-with-continuous-i.md#).

## Performance Analytics for customer service cases

If the Performance Analytics application is enabled, you can also use the available template configurations to open the Process Mining application from a Performance Analytics \(PA\) [indicator](../../../use/performance-analytics/concept/performance-analytics-glossary.md#) based on the customer service case data. For more information, see [Integration with Performance Analytics](integrate-pa.md#).

**Parent Topic:**[Activate content packs](../task/activate-po-content-pack.md)

**Related topics**  


[Example of Process Mining for CSM](csm-integration-po.md#)

## Example of Process Mining for CSM

Analyze a process for customer service cases and identify bottlenecks to minimize delays in the case flow for a better customer experience.

Say you are a process analyst in the ACME corporation where you must submit analysis on current processes associated with customer service cases. You use Analyst workbench to access the mined processes for the **Customer Service Cases** project.

You would analyze the case process flow and suggest ways to improve the processes by using the following workflow:

1.  Select **View in Workspace** from the **Customer Service Cases** project definition. Analyst workbench is opened in a new tab.

    You observe that the customer service case records take an average duration of 16 days to close a case.

2.  View metrics of the process map by setting the Primary Metric and Secondary Metric lists to **Unique Occurrences** and **Average Duration**, respectively.
3.  Refine the process map by selecting **Refine** and selecting a connection width to see the full list of metrics.

    You observe that the **Work In Progress - Awaiting Info** transition state is taking more than two days.

4.  In the **Filters** tab, set the Breakdown filters list to **Assignment group** and use the activity filter to view the process flow between the **Work In Progress - Awaiting Info** and **Work In Progress** activities.
5.  In the **Routes** tab, you want to see all the records that took longer than average duration of two days between the selected activities so you select **Most records** in the Sort by list. You then select any process paths to view the cases in that route.

    You observe that most of the cases are related to emails.

6.  Add notes to the project by selecting the notes icon \(![Notes icon](../image/notes-icon.png)\) and submit an analysis.

    In your notes, you suggest using a standardized template for improving the email transactions between agents and customers.


![Example: Process Mining Analyst workbench for CSM](../image/example-po-csm2.png "Process Mining for customer service cases")

**Related topics**  


[Analyzing and getting process insights](analyze-get-process-insights.md)

[Content pack for Customer Service Management](csm-integration-po.md#)

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

Use the SLA Breach Analysis project to analyze the reasons why customers are breaching SLAs and help them get to the root cause. This project is available with the [Process Mining Content Pack for CSM](csm-integration-po.md#) \(sn\_csm\_po\).

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


