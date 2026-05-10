---
title: Integrating with Process Mining
description: Integrate Customer Service Management with the Process Mining application to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, Customer Service Management]
---

# Integrating with Process Mining

Integrate Customer Service Management with the Process Mining application to analyze processes relevant to your KPIs, and identify bottlenecks associated with customer service cases.

For more information about enabling the Process Mining Content Pack for CSM, see [Activate content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/activate-po-content-pack.md).

## End user and roles

If you have the required roles, you can use Analyst Workbench to access the visualized process workflow data, and tools for analyzing data related to customer service cases. For more information, see [Overview of the Analyst Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/analyst-workbench-overview.md).

The following combinations of roles are required for using the Process Mining application with Customer Service Management.

|Process Mining role|Customer Service Management role|
|-------------------|--------------------------------|
|sn\_process\_optimization\_admin|sn\_customerservice\_manager|
|sn\_process\_optimization\_power\_user|sn\_customerservice\_manager|
|sn\_process\_optimization\_analyst|sn\_customer\_service\_agent|

## Projects included with Process Mining Content Pack for CSM

Several projects are included with the Process Mining Content Pack for CSM \(sn\_csm\_po\) that customers can use to get started:

-   [Case evaluation project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/evaluation-pm-csm.md): Use this project to evaluate Process Mining and become familiar with the Process Mining capabilities.
-   **Long resolution time analysis project**: Use this project to identify bottlenecks to minimize delays in the case flow.
-   [SLA Breach Analysis project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/csm-integration-po.md): Use this project to identify and analyze customer service cases where service level agreements \(SLAs\) have been violated.

## Optimization project for customer service cases

The Process Mining Content Pack for CSM \(com.snc.csm\_process\_optimization\) adds a prebuilt project that includes a predefined **Customer Service Cases** process model definition for customer service cases. By default, the **Customer Service Cases** project filters customer service cases for the last two quarters. You can also configure a new process project based on the prebuilt project. For more information, see [Create a project using ServiceNow platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/create-proj.md).

The **Customer Service Cases** process model definition includes default activity definitions and breakdown definitions for customer service cases. Use the definitions as they are or modify them for a custom configuration.

-   Use activity definitions to understand state transitions and analyze the linked processes such as Problem \(PRB\) records. Transitions can include, for example, going from the work in progress state to the solution proposed state.
-   Use breakdown definitions to filter records and analyze a process map by categories. For example, you can filter the customer service case data by different channels, products, assignment groups, and locations.

## Continual Improvement Management initiative for customer service cases

If the Continual Improvement Management \(CIM\) application is enabled, the CIM project from the Analyst Workbench can be used to track customer service case improvement initiative progress. The improvement initiative and the process mining model are automatically linked. For more information, see [Integration with Continual Improvement Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/integrate-with-continuous-i.md).

## Performance Analytics for customer service cases

If the Performance Analytics application is enabled, the available template configurations can also open the Process Mining application from a Performance Analytics \(PA\) indicator based on the customer service case data. For more information, see [Integration with Performance Analytics \(PA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/integrate-pa.md).

## Process configuration for customer service cases

Select the Process Mining Content Pack for CSM \(com.snc.csm\_process\_optimization\) templates to quickly set up projects with pre-configured default settings. Process configurations specify preferences that activate key functionalities within the Process Mining workspace and streamline project setup for cases. Fully configured processes allow users to build projects autonomously and derive insights efficiently, supporting enterprise-wide scalability of process mining. For more information, see [Creating process configurations using content pack templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/content-pack-config.md).

**Related topics**  


[Process Optimization for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/csm-integration-po.md)

