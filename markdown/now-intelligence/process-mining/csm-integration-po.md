---
title: Content pack for Customer Service Management
description: Using the Process Mining content pack for Customer Service Management enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Content pack for Customer Service Management

Using the Process Mining content pack for Customer Service Management enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.

For more information about enabling the Process Mining Content Pack for CSM, see [Activate Process Mining content packs](po-content-pack.md).

## End user and roles

If you have the required roles, you can use Analyst Workbench to access the visualized process workflow data, and tools for analyzing the data related to customer service cases. For more information, see [Analyst Workbench](analyst-workbench-dashboard.md).

The following combinations of roles are required for using the Process Mining application with Customer Service Management.

|Process Mining role|Customer Service Management role|
|-------------------|--------------------------------|
|sn\_process\_optimization\_admin|sn\_customerservice\_manager|
|sn\_process\_optimization\_power\_user|sn\_customerservice\_manager|
|sn\_process\_optimization\_analyst|sn\_customer\_service\_agent|

## Optimization project for customer service cases

The Process Mining Content Pack for CSM \(sn\_csm\_po\) adds a pre-built project that includes a predefined **Customer Service Cases** project definition for customer service cases. By default, the **Customer Service Cases** project filters customer service cases for the last two quarters. You can also configure a new process project based on the pre-built project. For more information, see [Create a project or template using Project Builder](../task/define-workflow-model.md).

The **Customer Service Cases** project includes default activity definitions and breakdown definitions for customer service cases that you can use as they are or modify them for a custom configuration.

-   Use activity definitions to understand state transitions such as cases transitioning from the work in progress state to the solution proposed state and analyze the linked processes such as Problem \(PRB\) records.
-   Use breakdown definitions to filter records and analyze a process map by categories. For example, you can filter the customer service case data by different channels, products, assignment groups, and locations.

## Continual Improvement Management initiative for customer service cases

If the Continual Improvement Management \(CIM\) application is enabled, you can also use the CIM project from the Analyst Workbench to track the progress of improvement initiatives for customer service cases. The improvement initiative and Process Mining projects are automatically linked. For more information, see [Integration with Continual Improvement Management](integrate-with-continuous-i.md#).

## Performance Analytics for customer service cases

If the Performance Analytics application is enabled, you can also use the available template configurations to open the Process Mining application from a Performance Analytics \(PA\) [indicator](../../../use/performance-analytics/concept/performance-analytics-glossary.md#) based on the customer service case data. For more information, see [Integration with Performance Analytics](integrate-pa.md).

-   **[Example of Process Mining for CSM](example-po-csm.md)**  
Analyze a process for customer service cases and identify bottlenecks to minimize delays in the case flow for a better customer experience.

**Parent Topic:**[Activate Process Mining content packs](po-content-pack.md)

**Related topics**  


[Example of Process Mining for CSM](example-po-csm.md)

