---
title: Process Mining for Field Service Management
description: Integrating the Process Mining application with the Field Service Management application enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with work order tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrated work order entry, Exploring Field Service Management, Field Service Management]
---

# Process Mining for Field Service Management

Integrating the Process Mining application with the Field Service Management application enables you to analyze processes relevant to your KPIs, and identify bottlenecks associated with work order tasks.

Process Mining for FSM creates business process flows from the work order task data in audit trails, allowing process owners to perform in-depth analysis and discover process insights to improve business outcomes.

Use Process Mining Content Pack for FSM \(com.snc.fsm\_process\_optimization\) plugin to activate Process Mining Content Pack for FSM. For more information, see [Additional plugins for Field Service Management](../reference/field-service-additional-plugins.md).

## End user and roles

If you have the required roles, you can use Analyst Workbench to access the visualized process workflow data, and tools for analyzing the data related to customer service cases. For more information, see [Overview of the Analyst Workbench](https://www.servicenow.com/docs/access?context=analyst-workbench-overview&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

The following roles are required for using the Process Mining Content Pack for FSM.

-   sn\_process\_optimization\_viewer
-   sn\_process\_optimization\_admin
-   sn\_process\_optimization\_analyst
-   sn\_process\_optimization\_power\_user

## Optimization project for work order tasks

The Process Mining Content Pack for FSM adds a pre-built project that includes a predefined **Work order tasks** process model definition for work orders. By default, the **Work order tasks** project filters work order tasks for the last two quarters. You can also configure a new process project based on the pre-built project.

The **Work order tasks** process model definition includes default activity definitions and breakdown definitions for work order tasks that you can use as they are or modify them for a custom configuration.

-   Use activity definitions to understand state transitions such as tasks transitioning from the work in progress state to the solution proposed state.
-   Use breakdown definitions to filter records and analyze a process map by categories. For example, you can filter the work order tasks data by agents, assignment groups, and locations.

## Continual Improvement Management initiative for work order tasks

If the Continual Improvement Management \(CIM\) application is enabled, you can also use the CIM project from the Analyst Workbench to track the progress of improvement initiatives for work order tasks. The improvement initiative and Process Mining model are automatically linked. For more information, see [Integration with Continual Improvement Management](https://www.servicenow.com/docs/access?context=integrate-with-continuous-i&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

## Performance Analytics for work order tasks

If the Performance Analytics application is enabled, you can also use the available template configurations to open the Process Mining application from a Performance Analytics \(PA\) indicator based on the work order task data. For more information, see [Integration with Performance Analytics \(PA\)](https://www.servicenow.com/docs/access?context=integrate-pa&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

**Related topics**  


[Example of content pack for FSM](https://www.servicenow.com/docs/access?context=example-po-fsm&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

