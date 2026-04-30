---
title: Flow execution details
description: View run-time information about an action or flow directly from the design environment, such as the current state, items run, and values produced. Open related records from embedded ServiceNow AI Platform editors or in a new tab.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-05-15"
reading_time_minutes: 11
breadcrumb: [Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Flow execution details

View run-time information about an action or flow directly from the design environment, such as the current state, items run, and values produced. Open related records from embedded ServiceNow AI Platform editors or in a new tab.

Each time you test a flow, the system generates information about the configuration and runtime values produced as flow execution details. You can view flow execution details from the **Operations** tab of Workflow Studio. Select a flow execution to open its associated execution details page.

![List of flow execution details for today's executions.](../../workflow-studio/images/example-workflow-studio-operations-flows-todays-executions.png "Example flow execution details for today's executions")

Each execution details page displays runtime information about the flow.

-   Name of the flow
-   Refresh flow data
-   Flow state
-   Related record options
-   Flow Statistics

![Sample execution details](../images/execution-details-example.png "Sample execution details")

## Reporting level

The reporting level determines what execution details a flow, subflow, or action generates during normal operations. By default, Workflow Studio doesn’t generate any execution details during normal operations. Workflow Studio generates full flow execution details when you test an individual flow, subflow, or action. When your instance generates and stores more execution details, reporting has more performance impact on your instance.

Each reporting level generates progressively more flow execution details.

-   **Off**

    The system doesn't generate flow execution details. The system only generates execution details when you run a test.

    **Note:** Testing an action or flow generates execution details at the Trace level.

-   **Basic: Runtime states and durations only**

    The system generates runtime execution details for each flow, subflow, and action run. You can see the runtime state and duration for these basic items. You can also see configuration and runtime values for flow triggers, subflow inputs, and subflow outputs.

-   **Full: Action configuration and runtime values \(for debugging only\)**

    The system generates configuration and runtime execution details for each flow, subflow, and action run. You can see the runtime state, duration, input values, and output values for all items. For custom actions, you can also see the runtime state, duration, input values, and output values of its steps. You can also see the configuration values for flow triggers, subflows, actions, and steps that are part of a custom action.

    **Important:** Only users with the fd\_read\_operations\_all role can see configuration and runtime information such as record values in the flow execution details. Users without this role will only see basic details about the state and duration.

-   **Trace: All values \(for testing and Support only\)**

    The system generates configuration and runtime execution details for each flow, subflow, action, and step run. You can see the runtime state, duration, input values, and output values for all items. You can also see the configuration values for flow triggers, subflows, actions, and steps.

    **Important:** Only users with the fd\_read\_operations\_all role can see configuration and runtime information such as record values in the flow execution details. Users without this role will only see basic details about the state and duration. Testing an action or flow generates execution details at the Trace level.


If a flow runs while reporting is off, past execution details are never available for the flow, even if the reporting level later changes. If a flow runs while reporting is on, execution details are available for that flow execution, even if the reporting level changes. The reporting level has no effect on context and log records.

You can configure the default reporting level the system uses to generate execution details each time a flow is run. For more information, see [Activate flow reporting](../task/enable-flow-reporting.md#).

## Refresh flow data

Update flow runtime data as needed. Set a flow preference to refresh flow data automatically when you run a test. See [User preferences for flows](../reference/flow-preferences.md).

## Flow state

All active flows are in one of these states.

-   **Completed**

    The flow successfully ran all actions. The flow statistics display configuration and runtime details for each action.

-   **Cancelled**

    The flow was either stopped because the flow's run time duration exceeded the flow time out value, or someone manually cancelled the flow.

-   **Waiting**

    The flow paused on an action that is waiting for some condition to be met before continuing. The flow statistics display configuration and runtime details for completed actions as well as any actions waiting for a condition to be met. Flows in the Waiting state display a **Cancel Flow** UI action in the header.

-   **Paused**

    The flow paused to enable higher priority flows to run or to enable a graceful node shutdown. The flow statistics display configuration and runtime details for completed actions.

-   **Presumed Interrupted**

    The flow has been running for more than 15 minutes and no longer has a valid transaction ID for the current node. Alternatively, the flow has been running for more than eight hours on another node. The flow may have stopped because of an unexpected interruption such as its transaction being terminated or its node being restarted.

-   **Error**

    The flow stopped with an error. The flow statistics display configuration and runtime details for completed actions and configuration details for the action that produced the error. Flows in the Error state display a **Go to error** UI action in the header.

    **Note:** When an action results in an error, the flow stops executing at that point and results in an error state.


## Related record options

From the Execution details page, you can access records related to the current flow.

-   **Open Flow**

    Use this option to make configuration changes and publish a new instance of the flow. Changing the flow configuration doesn’t change any currently active flow.

-   **Open Context Record**

    Use this option to view the flow state, run duration, and related log entries from a standard form view. This option opens the context record in a new tab.

-   **Open Flow Logs**

    Use this link to view detailed log information about each action. This link opens the log entries list in a new tab.

-   **Open Current Record**

    For flows that have a record-based trigger, use this link to view the triggering record in a pop-up window.

-   **Open Action**

    Use this link to make configuration changes and publish a new instance of the action. Changing the action configuration doesn’t change any currently active flow. This link is unavailable for the core actions provided by ServiceNow.


## Flow statistics

Use flow statistics to see configuration details and runtime values for each flow component. Selecting a trigger or action expands the row and displays configuration and runtime details about it.

![Sample flow statistics](../images/execution-details-example-flow-stats.png "Sample flow statistics")

The following types of execution details are available.

-   **Calling source**

    View the calling source that started a flow, subflow, or action.

-   **Run as**

    Identify whether the flow was **Run as** the system or the user who triggered the flow.

-   **Run with roles**

    Identify the roles granted to the user who triggered the flow.

-   **Integration Metadata**

    View transaction data such as connection and credential used, MID Server used, target host, and payload size. Integration Metadata is only displayed for integration steps and requires a separate Integration Hub subscription. For more information, see [Integration steps](https://www.servicenow.com/docs/access?context=integration-steps&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **Configuration Details**

    View the list of input variables to identify any configuration errors with the action. Each variable has its own row displaying its name, data type, configuration settings, and runtime value. The configuration settings display dynamic values as pills. The runtime values display generated records as a link.

    **Note:** Variables that have transform functions only display one runtime value, which is the result of all transformations.

-   **Output Data**

    View the list of output variables to identify any configuration errors with the action.

-   **Logs**

    Use the log entries to identify potential processing or performance issues. Each log entry has its own row displaying the creation date, log level, and log message. If the action doesn’t generate any logs, the statistics displays the string `No Logs`.

    **Note:** Logs display time in UTC format because logs must be saved as strings so that the instance can share the log data between its multiple nodes. Because each node can reside in a different time zone, the UTC format is used as a common format to preserve correct time values.

-   **Steps**

    Use the list of steps to identify any configuration errors with the action. Each step has its own row displaying the variable name, data type, configuration settings, and runtime value. Core actions don’t display steps because you can’t change their configuration.

    Change the **com.snc.process\_flow.reporting.serialized.val\_size\_limit** system property to truncate runtime values in the flow execution details step configuration. To learn more, see [Workflow Studio flow system properties](../reference/flow-designer-system-properties.md).

-   **Start time**

    View the local time when an action started.

-   **Run duration**

    Use the run duration to identify potential processing or performance issues. The run duration is measured in milliseconds. As of the Washington DC release, the run duration lists the total time to execute an item. The total time includes these items.

    -   Time in the event queue
    -   Time in the ECC queue
    -   Time processing the event
    -   Time running in the flow engine
    -   Time communicating with a MID Server
-   **Retry Info**

    Use the retry info section to view details about the retry policy. Details include the type of retry strategy, elapsed time, and the next scheduled retry request. The Retry Info section appears only when the retry policy is enabled in the step. For more information, see [Retry policy](retry-policy.md#).


## Calling source

The calling source lists what started a flow, subflow, or action.

|Source|Description|
|------|-----------|
|Workflow Studio Test|The flow started because someone selected the **Test** option from the Workflow Studio interface. The flow trigger conditions were ignored.|
|CRUD Trigger|The flow started when the record-based trigger conditions were met.|
|Date Trigger|The flow started when the schedule-based trigger conditions were met.|
|Metric Trigger|The flow started when the MetricBase trigger conditions of a [MetricBase](https://www.servicenow.com/docs/access?context=metricbase&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) were met.|
|Service Catalog Trigger|The flow started when a Service Catalog item was requested.|
|Script|The flow started from a method call in a script, such as a business rule.|
|Background Script|The flow started from a method call in the **Scripts - Background** module.|

## Embedded text viewer

Workflow Studio displays large text-based configuration and runtime output records, such as email output, XML payloads, or script steps using an embedded text viewer. The embedded text viewer can format text as HTML, plain text, or color-coded JavaScript. For script steps, the text viewer highlights code lines containing errors.

![Sample script](../images/execution-details-embedded-editors.png "Sample text view of a script step")

## Viewing results for each item in flow logic

Workflow Studio displays a selector control to view the configuration and runtime results for each item processed by flow logic. Select a record number to see its configuration and runtime details.

![For Each flow logic](../images/example-flow-logic-for-each.png "Sample flow statistics for each item in the flow logic")

## Subflow execution details

Process analysts can view subflow execution details from multiple locations.

-   **Parent flow**

    A parent flow lists the flow execution details of each subflow that it calls as inline elements. Expand the subflow step to see the subflow execution details.

-   **Subflow**

    The system generates flow execution details for each subflow run. View subflow execution details directly from the list of flow executions.


## User role support

You can control access to flow execution details by granting user roles. For more information about available Workflow Studio user roles, see [User access to Workflow Studio flows](user-access-flow-designer.md).

<table id="table_utq_v2r_nnb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

flow\_operator

</td><td>

Enables you to view flow execution details, dashboards, and logs. Administrators can grant this role to users that want to be able to view execution results but not create, change, or test them.

</td><td>

none

</td></tr><tr><td>

fd\_read\_operations

</td><td>

Enables you to view basic flow and action execution details. When reporting is enabled, users with this role can only see basic execution details such as the runtime state and duration. If the reporting level generates additional details, users with this role cannot see them. Administrators can grant this role to users that only need to view basic execution results but not create, change, or test flows and actions.**Note:** Read only roles are incompatible with roles that provide write access. Avoid granting the same user both a read only and a write access role.

</td><td>

none

</td></tr><tr><td>

fd\_read\_operations\_all

</td><td>

Enables you to view all generated flow and action execution details. When reporting is enabled, users with this role can view all available execution details. The user can only see as much detail as defined by the reporting level system property. Administrators can grant this role to users that need to view all flow results but not create, change, or test flows and actions.**Note:** Read only roles are incompatible with roles that provide write access. Avoid granting the same user both a read only and a write access role.

</td><td>

fd\_read\_operations

</td></tr></tbody>
</table>## Run with roles support

When a flow runs with one or more privileged roles, a user must also have these privileged roles to see the flow execution details. For example, if a flow runs as System, then a user must have the admin role to view its flow execution details. In addition, if a flow runs with a role that can access an encryption context, then a user must also have that role in order to view its flow execution details. For more information about encryption contexts and roles, see [Column Level Encryption](https://www.servicenow.com/docs/access?context=column-level-encryption-landing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

**Parent Topic:**[Exploring flows](../../workflow-studio/concept/exploring-flows.md)

