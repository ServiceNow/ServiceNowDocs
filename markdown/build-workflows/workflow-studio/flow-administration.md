---
title: Flow administration
description: Identify and troubleshoot potential issues by reviewing action and flow executions, their result state, and their runtime duration.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Flow administration

Identify and troubleshoot potential issues by reviewing action and flow executions, their result state, and their runtime duration.

Workflow Studio provides administrators and flow operators these modules to manage flows.

-   **Today's Executions**

    Displays a list of flow context records for flows run today. Use this information to identify flows run today.

-   **Active flows**

    Displays a list of flow context records for running flows where the **State** is **Waiting**. Use this information to identify flows that are waiting for a trigger or condition to continue.

-   **Event Queue**

    Displays a filtered list of event records where the **Queue** is **flow\_engine** and the **State** is **Ready**. Use this information to identify flows that are waiting on event processing.

-   **Operations Dashboard**

    Displays a responsive dashboard containing a count of flows run and the average flow runtime. View statistics for today or over the last 30 days. Use this information to determine the health and performance of flow execution.

-   **Settings**

    Displays the list of Flow and Action Settings records. Use this table to identify which actions and flows have had reporting disabled. Create records on this table to control whether reporting is done on an action or flow.

-   **Properties**

    Displays the system properties used to configure how the system processes flows.

-   **Complex Object Templates**

    Displays templates for complex objects that you can use in flows with Integration Hub integrations. To learn more about creating and using complex object templates, see [create an action](../task/create-action.md) and the [Object data type](../reference/object-data.md).

-   **Usage Overview**

    Displays transaction counts between your instance and third-party systems. The Usage Overview is not available in the base system and requires the ServiceNow® Integration Hub subscription.


-   **[Flow execution details retention](flow-reporting.md)**  
Due to the large amount of data consumed by flow execution details, your instance uses data retention policies to delete this data after a set time period.
-   **[Flow execution settings](flow-execution-settings.md)**  
Specify the runtime settings for an individual flow, subflow, or action such as the run priority, reporting level, and logging level.
-   **[Activate flow reporting](../task/enable-flow-reporting.md#)**  
Choose whether to generate execution details for all flows and actions run, just for individual flows and actions, or just when you test a flow or action. Specify the level of detail the execution details contain.
-   **[FDIH Dashboard](fdih-dashboard.md)**  
Use a single dashboard to view usage, execution, and debug information for Workflow Studio and Integration Hub transactions. Open links to related Workflow Studio properties, logs, events, and editors.
-   **[Flow priority](flow-priority.md)**  
Specify the priority that you want a background flow to have in relation to other flows waiting to be run. Run a group of higher priority flows before running any lower priority flows.
-   **[See related flows for action](../task/see-related-flows-for-action.md)**  
See the list of flows that include a custom action. Determine the impact that changes to an action have on published and draft flows.

**Parent Topic:**[Configuring flows](configuring-flow-designer.md)

