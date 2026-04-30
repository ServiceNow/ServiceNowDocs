---
title: HR Service Delivery Process Mining
description: Integrating the Process Mining application with the HR Service Delivery application enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with HR service cases and, if installed, Lifecycle Events cases.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Explore and use HR Case and Knowledge Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR Service Delivery Process Mining

Integrating the Process Mining application with the HR Service Delivery application enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with HR service cases and, if installed, Lifecycle Events cases.

## Process Mining for HR Service Delivery feature overview

Process Mining for HR Service Delivery enables companies to analyze and improve service delivery processes. It leverages Process Mining capabilities in the ServiceNow platform and offers a best practice content pack for HR Service Delivery.

The HRSD Process Mining content pack contains preconfigured process mining models that help analysts and process owners understand the effectiveness of their processes, including opportunities for continued performance improvement.

**Note:** As a process mining analyst, you can mark the content pack configurations as read-only, to preserve their custom configurations across upgrades.

Use Process Mining to discover, streamline, visualize, analyze, monitor, and more.

-   **Visualize your processes**: Map processes across system and functional boundaries based on data analysis.​
-   **Streamline your processes**: Identify bottlenecks, siloes, redundancies, and other inefficiency drivers.
-   **Automate your processes**: Identify frequent, consistent, and repeated tasks that are suitable for automation.
-   **Improve your processes**: Link process maps to KPIs to perform root cause analysis and identify drivers of performance.

For complete information about the Process Mining application and how it relates to and integrates with HR Service Delivery, see [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

To enable the Process Mining content pack for HR Service Delivery, see [Activate Process Mining content packs](https://www.servicenow.com/docs/access?context=po-content-pack&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

## HR Service Delivery Process Mining configuration model

HR Service Delivery Process Mining configuration model includes process definitions for standard HR services, as well as a process map that uses multi-dimensional mining for Lifecycle Events if this application is installed.

Process maps and transitions look across your portfolio of HR services to find and visualize problem areas, opportunities for enhancements, and process compliance​.

|All standard HR services|Lifecycle Events \(if installed\)|
|------------------------|---------------------------------|
|Looks across HRSD to find deviations and problem areas.|Provides a Lifecycle Event process map using multi-dimensional intelligent mining.|
|Provides a single HR service view, enabling you to drill down to find bottlenecks and other fulfillment issues.|Access automated end-to-end process visibility on multi-relational processes and tables​.|
|Automatically notifies process owners when common issues are detected using process configurations, such as channel performance degradation, KPI obtainment trends \(for example, SLA\), or too much variation between what is expected versus what is actual.|Quickly find key drivers behind process problems using an AI-based root cause analyzer.|

## End user and roles

If you have the required roles, you can use Analyst Workbench to access the visualized process workflow data, and tools for analyzing the data related to HR service cases. For more information, see [Overview of the Analyst Workbench](https://www.servicenow.com/docs/access?context=analyst-workbench-overview&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

The following combinations of roles are required for using the Process Mining application with HR Service Delivery.

|Process Mining role|HR Service Delivery role|
|-------------------|------------------------|
|sn\_process\_optimization\_admin|sn\_hr\_core.admin|
|sn\_process\_optimization\_power\_user|sn\_hr\_core.case\_writer|
|sn\_process\_optimization\_analyst|sn\_hr\_core.basic|

## Optimization project for HR service cases

The HRSD Process Mining content pack \(com.sn\_hr\_process\_mining\) adds a prebuilt project that includes predefined HR service cases and, if installed, Lifecycle Events cases process model definitions. By default, the project filters cases for the last two quarters. You can also configure a new process project based on the prebuilt project. For more information, see [Using Process Mining](https://www.servicenow.com/docs/access?context=use-process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

The process model definitions include default activity definitions and breakdown definitions for cases that you can use as they are or modify for a custom configuration.

-   Use activity definitions to understand state transitions such as cases transitioning from the work in progress state to the solution proposed state and analyze the linked processes such as Problem \(PRB\) records.

    **Note:** The content pack activity definitions can be set to either ALL or INCLUDE based on whether the field values are populated or not in the `field_values_selection_type` column in the `promin_activity_def` table, so that the correct number of activities are available by default for each project.

-   Use breakdown definitions to filter records and analyze a process map by categories. For example, you can filter the HR service case data by different channels, products, assignment groups, and locations.

## Continual Improvement Management initiative for HR cases

If the Continual Improvement Management \(CIM\) application is enabled, you can also use the CIM project from the Analyst Workbench to track the progress of improvement initiatives for HR cases. The improvement initiative and process optimization model are automatically linked. For more information, see [Integration with Continual Improvement Management](https://www.servicenow.com/docs/access?context=integrate-with-continuous-i&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

## Performance Analytics for HR cases

If the Performance Analytics \(PA\) application is enabled, you can also use the available template configurations to open the Process Mining application from a PA indicator based on the HR service case data. For more information, see [Integration with Performance Analytics \(PA\)](https://www.servicenow.com/docs/access?context=integrate-pa&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Explore and use HR Case and Knowledge Management](hr-ckm-use-explore.md)

