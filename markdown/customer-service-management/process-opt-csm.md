---
title: Integrating with Process Mining
description: Integrate Customer Service Management with the Process Mining application to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating Customer Service Management with other applications, Customer Service Management]
---

# Integrating with Process Mining

Integrate Customer Service Management with the Process Mining application to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.

For more information about enabling the Process Mining Content Pack for CSM, see [Activate Process Mining content packs](https://www.servicenow.com/docs/access?context=po-content-pack&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

## End user and roles

If you have the required roles, you can use Analyst Workbench to access the visualized process workflow data, and tools for analyzing data related to customer service cases. For more information, see [Overview of the Analyst Workbench](https://www.servicenow.com/docs/access?context=analyst-workbench-overview&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

The following combinations of roles are required for using the Process Mining application with Customer Service Management.

|Process Mining role|Customer Service Management role|
|-------------------|--------------------------------|
|sn\_process\_optimization\_admin|sn\_customerservice\_manager|
|sn\_process\_optimization\_power\_user|sn\_customerservice\_manager|
|sn\_process\_optimization\_analyst|sn\_customer\_service\_agent|

## Optimization project for customer service cases

The Process Mining Content Pack for CSM \(com.snc.csm\_process\_optimization\) adds a prebuilt project that includes a predefined **Customer Service Cases** process model definition for customer service cases. By default, the **Customer Service Cases** project filters customer service cases for the last two quarters. You can also configure a new process project based on the prebuilt project. For more information, see [Create a project using ServiceNow platform](https://www.servicenow.com/docs/access?context=create-proj&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

The **Customer Service Cases** process model definition includes default activity definitions and breakdown definitions for customer service cases. Use the definitions as they are or modify them for a custom configuration.

-   Use activity definitions to understand state transitions and analyze the linked processes such as Problem \(PRB\) records. Transitions can include, for example, going from the work in progress state to the solution proposed state.
-   Use breakdown definitions to filter records and analyze a process map by categories. For example, you can filter the customer service case data by different channels, products, assignment groups, and locations.

## Continual Improvement Management initiative for customer service cases

If the Continual Improvement Management \(CIM\) application is enabled, the CIM project from the Analyst Workbench can be used to track customer service case improvement initiative progress. The improvement initiative and the process mining model are automatically linked. For more information, see [Integration with Continual Improvement Management](https://www.servicenow.com/docs/access?context=integrate-with-continuous-i&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

## Performance Analytics for customer service cases

If the Performance Analytics application is enabled, the available template configurations can also open the Process Mining application from a Performance Analytics \(PA\) indicator based on the customer service case data. For more information, see [Integration with Performance Analytics \(PA\)](https://www.servicenow.com/docs/access?context=integrate-pa&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

**Related topics**  


[Process Optimization for CSM](https://www.servicenow.com/docs/access?context=example-po-csm&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

