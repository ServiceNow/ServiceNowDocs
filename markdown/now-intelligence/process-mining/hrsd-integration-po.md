---
title: Content pack for HR Service Delivery
description: Using the Process Mining content pack for HR Service Delivery enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Content pack for HR Service Delivery

Using the Process Mining content pack for HR Service Delivery enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

For more information about enabling the HRSD Process Mining Content Pack, see [Activate Process Mining content packs](po-content-pack.md).

## End user and roles

If you have the required roles, you can use Analyst Workbench to access the visualized process workflow data, and tools for analyzing the data related to customer service cases. For more information, see [Analyst Workbench](analyst-workbench-dashboard.md).

The following combinations of roles are required for using the Process Mining application with HR Service Delivery.

|Process Mining role|HR Service Delivery role|
|-------------------|------------------------|
|sn\_process\_optimization\_admin|sn\_hr\_core.admin|
|sn\_process\_optimization\_power\_user|sn\_hr\_core.case\_writer|
|sn\_process\_optimization\_analyst|sn\_hr\_core.basic|

## Optimization project for HR cases

The HRSD Process Mining Content Pack \(com.sn\_hr\_process\_optimization\) adds a pre-built project that includes predefined HR service cases and, if installed, Lifecycle Events cases project definitions. By default, the project filters cases for the last two quarters. You can also configure a new process project based on the pre-built project. For more information, see [Create a project or template using Project Builder](../task/define-workflow-model.md).

The project definition includes default activity definitions and breakdown definitions for cases that you can use as they are or modify for a custom configuration.

-   Use activity definitions to understand state transitions such as cases transitioning from the work in progress state to the solution proposed state and analyze the linked processes such as Problem \(PRB\) records.
-   Use breakdown definitions to filter records and analyze a process map by categories. For example, you can filter the case data by different channels, products, assignment groups, and locations.

## Continual Improvement Management initiative for HR cases

If the Continual Improvement Management \(CIM\) application is enabled, you can also use the CIM project from the Analyst Workbench to track the progress of improvement initiatives for HR cases. The improvement initiative and Process Mining project are automatically linked. For more information, see [Integration with Continual Improvement Management](integrate-with-continuous-i.md#).

## Performance Analytics for HR cases

If the Performance Analytics \(PA\) application is enabled, you can also use the available template configurations to open the Process Mining application from a Performance Analytics [indicator](../../../use/performance-analytics/concept/performance-analytics-glossary.md#) based on the customer service case data. For more information, see [Integration with Performance Analytics](integrate-pa.md).

-   **[Example of Process Mining for HR Service Delivery](example-po-hrsd.md)**  
Analyze a process for your HR service or, if installed, Lifecycle Events cases and identify bottlenecks to minimize delays in the case flow for a better user experience.

**Parent Topic:**[Activate Process Mining content packs](po-content-pack.md)

