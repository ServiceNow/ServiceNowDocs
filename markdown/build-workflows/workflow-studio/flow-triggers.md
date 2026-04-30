---
title: Workflow Studio flow trigger types
description: Each trigger type defines when a flow starts and the starting data available to it. There are triggers for record operations, dates, and application operations.​
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Workflow Studio flow trigger types

Each trigger type defines when a flow starts and the starting data available to it. There are triggers for record operations, dates, and application operations.​

## Record triggers

Use record triggers to start a flow when a record is created or updated.

<table id="table_rvf_njy_mbb"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Starts a flow when a record is created in a specific non-system table.**Note:** Some common record types such as requests have their own dedicated triggers. See the application trigger types for a list of application records that have dedicated triggers.

</td></tr><tr><td>

Updated

</td><td>

Starts a flow when a record is updated in a specific non-system table. Requires selecting when to run the flow.-   **For each unique change**: Triggers the flow for every unique update to a non-[system field](https://www.servicenow.com/docs/access?context=r_GlobalDefaultFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) even if the flow is currently running.

**Note:** The system stores a history of every change to a record and determines whether the change is unique. For example, if an incident record's **State** field changes from In Progress to On Hold, the flow can run. However, if the **State** field then changes back to In Progress, the flow can't run.

**Note:** Flows that have a record trigger that runs **For each unique change** can produce recursions when run in a non-interactive session. When this type of flow makes a change to the trigger record, the change meets the flow trigger conditions and causes a recursion.

-   **Once**: Triggers the flow once for the life of the record.
-   **Only if not currently running**: Triggers the flow for every unique record change if the flow is not currently running on this record. This behavior is the same as the **Always** option in previous releases.
-   **For every update**: Triggers the flow every time that the record is updated, regardless of whether there has already been or currently are any running contexts for the flow.

</td></tr><tr><td>

Created or Updated

</td><td>

Starts a flow when a record is either created or updated in a specific non-system table. Requires selecting when to run the flow.-   **For each unique change**: Triggers the flow for every unique update to a non-[system field](https://www.servicenow.com/docs/access?context=r_GlobalDefaultFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) even if the flow is currently running.

**Note:** The system stores a history of every change to a record and determines whether the change is unique. For example, if an incident record's **State** field changes from In Progress to On Hold, the flow can run. However, if the **State** field then changes back to In Progress, the flow can't run.

**Note:** Flows that have a record trigger that runs **For each unique change** can produce recursions when run in a non-interactive session. When this type of flow makes a change to the trigger record, the change meets the flow trigger conditions and causes a recursion.

-   **Once**: Triggers the flow once for the life of the record.
-   **Only if not currently running**: Triggers the flow for every unique record change if the flow is not currently running on this record. This behavior is the same as the **Always** option in previous releases.
-   **For every update**: Triggers the flow every time that the record is updated, regardless of whether there has already been or currently are any running contexts for the flow.

</td></tr></tbody>
</table>**Note:** Flows including approval actions should only run the trigger once. In cases where you need to update and resubmit an approval, consider using a [Go back to flow logic](go-back-to-flow-logic.md) to ask for approval again.

## REST triggers

Use REST triggers to start a flow after a specific REST API request.

**Note:** This feature requires an Integration Hub Enterprise subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

|Trigger|Description|
|-------|-----------|
|REST API - Asynchronous|Start a flow from an inbound API call or webhook from an external system. Configure the trigger start conditions without having to write or maintain custom code. For more information, see [REST API trigger](https://www.servicenow.com/docs/access?context=rest-trigger&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).|

## Scheduled triggers

Use scheduled triggers to start a flow after a specific date and time or repeatedly at scheduled intervals. Scheduled triggers use the instance timezone to determine when to start a flow.

**Note:** Because flows are processed asynchronously, a flow with a scheduled trigger may not run at the exact scheduled time its trigger conditions were met. For example, if a scheduled flow is triggered during core business hours, the system may have to process other events in the queue before it can run the scheduled flow.

|Trigger|Description|
|-------|-----------|
|Daily|Starts a flow at a specific time every day.|
|Weekly|Starts a flow at a specific time every week.|
|Monthly|Starts a flow at a specific time every month.|
|Run Once|Starts a flow once at a specific time but does not repeat. If you select a past date or time, the system schedules the flow to run as soon as possible.|
|Repeat|Starts a flow at regular intervals you define.|

## Application triggers

Use application triggers to start a flow when application-specific conditions are met.

<table id="table_gfx_xvl_ycb"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Kafka Message

</td><td>

Starts a flow when there's a message in a topic in your Kafka environment. For more information, see [Create a flow with a Kafka Message trigger](../task/create-flow-kafka.md).

</td></tr><tr><td>

MetricBase

</td><td>

Starts a flow when a MetricBase trigger is met. Requires the MetricBase application. For more information, see [Create a flow with a MetricBase trigger](../task/create-mb-flow.md).

</td></tr><tr><td>

Proactive Analytics

</td><td>

Starts a flow when Proactive Analytics KPI score or KPI threshold values are met. Requires a Performance Analytics subscription to Proactive Analytics. For more information, see [Create a flow with a Proactive Analytics trigger](../task/create-flow-proactive-analytics.md).

</td></tr><tr><td>

Service Catalog

</td><td>

Starts a flow from a Service Catalog item request. For more information, see [Create a flow with a Service Catalog trigger](../task/create-sc-flow.md).**Note:** Service Catalog triggers do not support catalog variables as part of the trigger condition. Instead, get or create catalog variables in the main body of the flow.

</td></tr><tr><td>

SLA Task

</td><td>

Starts a flow from an SLA Definition record. For more information, see [Create a flow with an SLA Task trigger](../task/create-sla-task-flow.md).

</td></tr></tbody>
</table>## Inbound email triggers

Start a flow when your instance receives an email.

Inbound email flows take priority over inbound email actions. If you create flows with inbound email triggers, emails are first processed by the inbound email triggers before they are processed by inbound email actions.

With inbound email actions, you don't have full control over email attachment handling or assigning the target record of an email. When you create a flow with an inbound email trigger, you can perform these actions with the [Move Email Attachments to Record action](move-email-attachments-action.md) and the [Associate Record to Email action](associate-to-email-action.md). For greater control over email attachments, you can also use the [Look up email attachments action](lookup-email-attachment.md) to access a specific attachment as a data pill.

Although you can process an inbound email with multiple inbound email actions, you can't process an inbound email with multiple flows by default. Additional configuration is required. For information on how to stop processing in inbound email actions, see [Specifying the inbound email processing order](https://www.servicenow.com/docs/access?context=r_OrderedEmailProcessingPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

For more information on running multiple flows on an inbound email, see [Allow multiple triggers to process an inbound email](../../notification/task/deactivate-stop-processing.md).

The following diagram shows how inbound emails are processed by inbound email triggers. After the email has been classified as a reply, forward, or new email, the system tries to match the email to an active inbound email trigger. If the email meets the conditions of an inbound email trigger, the flow runs. If the flow issues stop processing, the email is finished being processed. If the flow does not issue stop processing, the system evaluates the conditions of more inbound email triggers. If there are no more inbound email triggers to evaluate, the system tries to match the email with an active inbound email action instead.

![Processing emails in the Inbound Email trigger](../../notification/image/inbound-flow-processing.png "Processing emails with inbound email triggers")

**Important:** Inbound email flows use the email sender as the user who initiates the session. If the system doesn't recognize the sender, the inbound email flow runs as the Guest user. Setting the inbound email flow to run as the user who initiates the session ensures that the flow actions are limited by user access controls. If the initiating user needs elevated privileges for some reason, have the inbound email flow call a subflow that runs with the required roles. To test access controls for an inbound email flow, impersonate a typical inbound email user and manually trigger the flow.

## Spoke triggers

Spokes can have conditional and event-driven external triggers or webhooks that start from third-party applications. The webhooks act as the triggers that provide the data to a flow. For example, when you create a P1-level issue in a third-party issue-tracking application, it updates the incident database record in the ServiceNow instance. To implement this flow, follow these steps:

1.  [Set up a flow](https://www.servicenow.com/docs/access?context=set-up-flow-ihub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
2.  [Set up external trigger endpoints](https://www.servicenow.com/docs/access?context=set-up-external-webhook-endpoints&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

## Advanced options

Specify the user session requirements needed to start a flow in the **Advanced Options** section.

-   **When to run the flow**

    Determine the type of session that can trigger the flow, whether to run the flow when triggered by certain users, and which tables can trigger the flow.

    |Option|Description|
    |------|-----------|
    |Only Run for Non-Interactive Session|Flow that is triggered only in non-interactive sessions. See [Non-interactive sessions](https://www.servicenow.com/docs/access?context=c_NonInteractiveSessions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).|
    |Only Run for User Interactive Session|Flow that is triggered only in interactive sessions.|
    |Run for Both Interactive and Non-Interactive Sessions|Flow that is triggered in all sessions.|

    |Option|Description|
    |------|-----------|
    |Do not run if triggered by the following users|Flow that doesn't trigger for a selected list of users. Select the Add User icon \(![Add User Icon](../images/icon-select-users.png)\) to add users to the list.|
    |Only run if triggered by the following users|Flow that triggers only for a selected list of users. Select the Add User icon \(![Add User Icon](../images/icon-select-users.png)\) to add users to the list.|
    |Run for any user|Flow that runs for any user.|

    |Option|Description|
    |------|-----------|
    |Run only on current table|Flow that is triggered only for the selected table.|
    |Run on current and extended tables|Flow that is triggered for the selected table and any extended tables.|

-   **Where to run the flow**

    Determine whether to run the flow in the background or in the current session.

<table id="table_qhf_fh1_phb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run flow in background \(default\)

</td><td>

Flow that runs asynchronously in the background. Use this option for flows that don't require immediate updates and to allow other system processes to run at the same time.

</td></tr><tr><td>

Run flow in foreground

</td><td>

Flow that runs synchronously in the current session. Use this option to provide immediate updates to an end user. For example, if a flow opens a task after the previous task closes, use this option to open the next task immediately after a user closes one.**Note:** Running a flow in foreground may block the current session thread and prevent user input until the flow finishes. Avoid running flows in the foreground when they contain actions that cannot be interrupted, such as actions that run script. Actions or flow logic that pause a flow will not block a session.

</td></tr></tbody>
</table>
## Data pills available by trigger type

Flow designers have access to data pills from the trigger.

<table id="table_n55_2rb_2jb"><thead><tr><th>

Trigger Type

</th><th>

Data pills available

</th></tr></thead><tbody><tr><td>

Record

</td><td>

-   **\[Table Label\] Record**

An object containing the triggering record.

-   **Changed Fields**

An array of objects containing the field values that changed. This data pill is only available for the **Updated** or **Created or Updated** trigger types.

**Note:** To process the **Changed Fields** array data pill, you will need to use [For Each flow logic](../concept/flow-logic-for-each.md). For more information on working with array data pills, see [Complex data](../concept/complex-data.md).

-   **\[Table Label\] Table**

The Sys ID of the table containing the trigger record.

-   **Run Start Date/Time**

Date/Time object that stores when the flow started in the system's local timezone. Use this data pill to pass a Date/Time value to other actions and steps such as the Create record action or the Update record action.

-   **Run Start Time UTC**

Date/Time string that stores when the flow started in Coordinated Universal Time \(UTC\). Use this data pill to pass data to legacy flows that expect UTC date-time strings.


</td></tr><tr><td>

REST API - Asynchronous

</td><td>

-   **Path Parameters**

An object containing path parameters in the inbound request.

-   **Query Parameters**

An object containing query parameters in the inbound request.

-   **Request Headers**

An object containing headers in the inbound request.

-   **Request Body**

Complex data object that defines the body structure of the inbound request. For more information on complex objects, see [Complex data](../concept/complex-data.md).


</td></tr><tr><td>

Date

</td><td>

-   **Run Start Date/Time**

Date/Time object that stores when the flow started in the system's local timezone. Use this data pill to pass a Date/Time value to other actions and steps such as the Create record action or the Update record action.

-   **Run Start Time UTC**

Date/Time string that stores when the flow started in Coordinated Universal Time \(UTC\). Use this data pill to pass data to legacy flows that expect UTC date-time strings.


</td></tr><tr><td>

SLA Task

</td><td>

-   **Task SLA Record**

An object containing the triggering Task SLA record.

-   **sla\_flow\_inputs**

An Object containing Task SLA Definition values.


</td></tr><tr><td>

Inbound Email

</td><td>

-   **Email Record**

An object containing the triggering Email record.

-   **\[Table Label\] Table**

The Sys ID of the table associated with the target email.

-   **Body Text**

A String containing the body of the email message.

-   **Subject**

A String containing the subject of the email message.

-   **User Record**

An object containing the user who sent the triggering email. If the sender does not have an associated User record, the data pill lists the object for the Guest user.

-   **From address**

A String containing the sender email address.


</td></tr><tr><td>

Metric Base

</td><td>

-   **MetricBase Trigger Definition Record**

An object containing the triggering MetricBase Trigger Definition Record.

-   **Level**

The Integer value of the MetricBase trigger level.

-   **Time of Metric Event**

The Date/Time value of when the metric event occurred.

-   **Record**

An object containing the record for which metric events have been collected.


</td></tr><tr><td>

Service Catalog

</td><td>

-   **Requested Item Record**

An object containing the triggering Requested Item record.

-   **Run Start Date/Time**

Date/Time object that stores when the flow started in the system's local timezone. Use this data pill to pass a Date/Time value to other actions and steps such as the Create record action or the Update record action.

-   **Run Start Time UTC**

Date/Time string that stores when the flow started in Coordinated Universal Time \(UTC\). Use this data pill to pass data to legacy flows that expect UTC date-time strings.

-   **Table Name**

The table name containing the requested catalog item.


</td></tr><tr><td>

Kafka Message

</td><td>

-   **Messages**

An array of objects containing the messages received from the Kafka topic. Each message has the following data pills.

    -   Headers: An array of headers, with each header containing a Key and a Value. The Key-Value pair provides additional information about the message. Both the Key and the Value are strings.
    -   Payload: A string containing the text of the message.
    -   Key: A sting identifying the insertion order for the message. Messages with the same key are processed in order.

</td></tr></tbody>
</table>## General guidelines

Follow these general guidelines when creating record triggers.

-   **Determine whether your flow needs a trigger or variable input**

    Flows always run when their trigger conditions are met. Triggers always provide the same data as input for flows. If you need variable input to initiate a flow instead, create a [subflow](flow-triggers.md#subflows-design-considerations).

-   **Add conditions to specify what record values start your flow**

    Starting a flow only when needed consumes fewer system resources than starting a flow, pausing it, and waiting to resume the flow until a specific record condition applies. Instead of creating a flow that starts with a Wait for condition action, redesign the flow to include the wait condition as part of the record trigger.

-   **Create unique conditions for record triggers on the same table**

    To prevent flows from overwriting each other, create unique conditions for each flow running on the same table. If multiple flows on the same table have the same filter conditions, there is no way to know the order in which the flows run. Using conditions also helps to optimize flow performance by returning a more precise, smaller set of records.

-   **Ignore records added or updated by import and update sets**

    Record triggers ignore records added or updated by applying an update set or importing an XML file. These operations apply to the entire application or table rather than an individual record.

-   **Replace record triggers on Service Catalog tables with Service Catalog application triggers**

    Flow Designer no longer displays Service Catalog tables as options for record triggers. Instead, create flows that use the Service Catalog application trigger type.

-   **Verify that the users who trigger a flow have access to trigger condition data**

    Since flows typically run as the user who triggers them, verify that users have access to all of the data specified in the trigger conditions. Avoid creating trigger conditions to related tables that typical users don't have access to. If your flow trigger conditions require access to role-restricted data, run your flows with the role needed to access that data.


**Parent Topic:**[Flows, subflows, and actions reference](flow-designer-reference.md)

