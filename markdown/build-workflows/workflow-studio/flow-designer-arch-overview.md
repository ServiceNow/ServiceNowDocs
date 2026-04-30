---
title: Architecture Overview
description: Understand how Workflow Studio works within the ServiceNow AI Platform to activate, trigger, and process flows and actions.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Flows, Explore, Workflow Studio, Build workflows]
---

# Architecture Overview

Understand how Workflow Studio works within the ServiceNow AI Platform to activate, trigger, and process flows and actions.

A flow consists of a trigger and one or more actions. The trigger specifies when to start the flow, which can be record-based, schedule-based, or application-based. Record-based triggers run a flow after a record has been created, updated, or deleted. The flow can use the triggering record as input for actions. Schedule-based triggers run a flow at the specified date and time. The flow can use the execution time as input for actions. Application triggers are added when the associated application is activated. For example, the MetricBase trigger is present when the MetricBase application is active.

## Flow processing

Flow processing occurs in this sequence.

1.  When the flow trigger conditions occur or an API directly calls the flow, the system creates an entry in the event queue to start the flow.
2.  The scheduler processes the event and starts the flow in the background.
3.  The system builds a process plan from the flow.
4.  The system runs the process plan using the record that triggered the flow.
5.  The system stores the execution details in a context record.

![Flow processing diagram](../images/build-process-plan.png)

-   **1. Process flow triggers and API calls**

    Each time trigger conditions are met or an API directly calls a flow, Workflow Studio creates an event entry. The system processes triggers after database operations. To learn more, see [Execution order of scripts and engines](https://www.servicenow.com/docs/access?context=r_ExecutionOrderScriptsAndEngines&version=zurich&pubname=zurich-api-reference&ft:locale=en-US). Typically, [How business rules work](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=zurich&pubname=zurich-api-reference&section=r_HowBusinessRulesWork&ft:locale=en-US) and [Workflow engine operation order](../../using-workflows/concept/c_WorkflowEngineOperationOrder.md#) that run synchronously run before a triggered flow.

-   **2. Process events in the queue**

    Each flow event contains a reference to the flow to start and a reference to either the triggering record or the execution time. The system processes these events using [Events](../../platform-events/concept/events.md) where a scheduler periodically works through the current items in the event queue in the order in which they were added. Depending on what other events are in the queue, the system may not immediately start a flow. Flow designers should expect some lag time between when the trigger conditions occur and when the flow actually starts.

-   **3. Build the process plan**

    When Workflow Studio pulls an event from the queue, it builds a process plan to actually run the flow. A process plan contains all the information necessary to execute a flow such as the sequence of published actions or subflows, the input values for each subflow or action, the action steps to run for each action, and the data provided by the trigger or subflow output.

    Workflow Studio uses a just-in-time compilation scheme to ensure that process plans contain the latest changes to flows, subflows, and actions. If no changes are detected, Workflow Studio uses a cached copy of the process plan. Otherwise, it builds a new process plan.

    By automatically checking for updated flows, subflows, and actions with process plans, Workflow Studio enables you to apply changes from update sets and upgrades without having to edit current flows. If you move published actions to a target instance, every flow that uses the published action will automatically update the next time it is executed.

    **Warning:** If changing subflows or actions used in activated flows, do not change the inputs and outputs used in the subflow or action. Changing inputs and outputs may cause errors when the activated flow is next triggered because it has not been configured to use the new inputs and outputs. Any currently running flows are unaffected by changes to inputs or outputs as the flow uses the compiled subflows and actions from the process plan.

-   **4. Run the process plan**

    Workflow Studio runs the process plan as the user specified in the flow properties and runs it within the flow application scope.

    When running a flow with a record-based trigger, Workflow Studio stores the triggering record in memory as an instance that is represented in the interface as a data pill.

    Each time you add an action to a flow, Flow Designer adds a data pill to store its results. The data pill name indicates its sequence in the flow and its data type. Flow designers use action result data pills to provide input for other flows, actions, or subflows. Flow designers can use the sequence value in the data pill name to ensure that they select the correct data pill as an input value. When a flow runs an action, it generates the data pill runtime value as it is used.

-   **5. Store flow execution details**

    Workflow Studio stores flow execution details in a flow context record, which contains this information.

    -   Flow outcome state
    -   Flow runtime duration
    -   Flow log messages
    -   Flow configuration and runtime values
    Each time a flow runs, Workflow Studio adds an entry to the **Flow Executions** list. Each entry has its own context record and matching execution details page.

    **Note:** A flow execution context runs in a single thread. However, there may be times when you want to run flows within separate contexts even though this may consume more of your instance's resources. To run subflows in separate flow contexts within the same flow, see [Dynamic flows](flow-logic-dynamic-flow.md).

    A flow can have one of these outcome states.

    |State|Description|
    |-----|-----------|
    |Complete|The flow completed successfully.|
    |In Progress|The flow is running. By default, a transaction quota rule prevents flows from running longer than an hour.|
    |Waiting|The flow is waiting for another event to occur. For example, a user must update a task or approval, or a record must reach a specific state. When in the waiting state, the flow is quiesced and serialized into a context record.|
    |Canceled|The flow was canceled by a user.|
    |Error|The flow encountered an error and has stopped running. For example, an action is missing an input value, or a quota transaction rule has stopped the flow.|


## Flow, subflow, and action life cycle

Workflow Studio uses the flow or action status to describe the current state of configuration changes.

-   **Flow and subflow status and activation state**

    The **Status** field indicates whether there is a process plan associated with the flow or subflow.

    |Flow status|Description|
    |-----------|-----------|
    |Modified|Indicates that there are unsaved changes to a flow or subflow. Modified flows or subflows have not been saved.|
    |Draft|Indicates that there are saved changes to a flow or subflow, which have not been stored in a process plan. Draft flows have been saved but not activated. Draft subflows have been saved but not published.|
    |Published|Indicates that there is a stored process plan for the flow or subflow. Published flows have either been activated or deactivated.|

    The **Active** field indicates whether the system runs a flow or subflow.

    |Active|Description|
    |------|-----------|
    |True|Indicates that the flow or subflow is active and runs when triggered or called. The flow has been activated or the subflow has been published. Active flows run when the trigger conditions are met or when called. Active subflows run when called.|
    |False|Indicates that the flow is inactive and does not run when triggered or called. An inactive flow has either never been activated or has been deactivated. An inactive subflow has never been published.|

    When working with flows, you can:

    -   **Save** a flow: Creates a draft of the flow.
    -   **Activate** a flow: Enables the flow trigger and transform the flow into a process plan.
    -   **Deactivate** a flow: Disables the flow trigger and prevents new flow executions. Currently running flows continue to run.
    When working with subflows, you can:

    -   **Save** a subflow: Creates a draft of the subflow. If the subflow is modified after being published, the subflow moves into a draft state. Any active flows that use the subflow only run the published subflow.
    -   **Publish** a subflow: Enables you to activate a flow containing the subflow. Publishing adds the subflow to the list of available subflows in a flow.
    ![Flow life cycle diagram](../images/flow-life-cycle.png)

-   **Action status**

    The Workflow Studio interface does not display the configuration status of actions. To view action status, navigate to the Action Types table \[sys\_hub\_action\_type\_definition\] and display the **Draft state** field.

    |Action Draft status|Description|
    |-------------------|-----------|
    |Draft|Indicates that there are changes to an action that have not been published. Draft actions are only available to flows when the **Show draft actions** option is enabled. You cannot activate a flow containing draft actions.|
    |Published|Indicates that the action has been published. Published actions are available to all flows and allow flows to be activated.|

    When working with actions, you can:

    -   **Save** an action: Creates a draft of the action that is only available to flows when **Show draft actions** is enabled. If the action is modified after being published, the action moves into a draft state. Any active flows that use the action only run the published action.
    -   **Publish** an action: Enables you to activate a flow containing the action. Publishing adds the action to the list of available actions in a flow. Only actions in a published state run during flow execution.
    ![Action life cycle diagram](../images/action-life-cycle.png)


## Application development

When designing an action or a flow, use these general guidelines.

Use standard ServiceNow AI Platform application development capabilities to create, manage, protect, and deploy Workflow Studio content. Flow and action designers typically perform the following application development tasks:

-   Create a custom application to store flows and actions.
-   Set application permissions to share or restrict access to application data.
-   Grant application developers access to Workflow Studio.
-   Publish custom applications to the application repository to deploy flows and actions on other instances.

## Collision avoidance

Workflow Studio supports collision avoidance. Collision avoidance prevents a user from modifying an object that is being modified in a different update set. For example, User A is editing a flow in a particular update set. User B, who is working in a different update set, attempts to open the same flow. In this situation, the system detects a collision and alerts User B. User B can then choose to either **Cancel** or **Continue**. Selecting **Cancel** takes User B back to the Workflow Studio homepage. Selecting **Continue** opens the flow in read-only mode.

For collision avoidance to work, both users must be in the same application scope, and it must be an application scope other than global. Additionally, the application being modified must be linked to source control. For more information, see [Collision avoidance](https://www.servicenow.com/docs/access?context=collision-avoidance&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Security

Control access to Workflow Studio processes and records.

-   Administrators can grant users access to Workflow Studio flows by creating an application and assigning users as developers with the [delegated development](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=zurich&pubname=zurich-application-development&ft:locale=en-US) permission. Delegated development allows administrators to control whether flow designers can access features normally restricted to admin users such as assigning user roles, creating access controls, or creating scripts. For more information, see [Developer permissions](https://www.servicenow.com/docs/access?context=developer-permissions&version=zurich&pubname=zurich-application-development&ft:locale=en-US).
-   Administrators can grant access to Workflow Studio flows by directly assigning users the flow\_designer user role, which includes the role to view flow execution details.

    **Warning:** Directly granting a user the flow\_designer role is equivalent to giving the user the admin role, because Workflow Studio can run flows as the System user, which has access to all tables and all database operations.

-   Flow and action designers can use standard [Application access settings](https://www.servicenow.com/docs/access?context=c_ApplicationAccessSettings&version=zurich&pubname=zurich-application-development&ft:locale=en-US) to manage how their content interacts with other applications.

## Action limit

By default, flows can have no more than 50 actions. To change the default behavior, increase the value of the **sn\_flow\_designer.max\_actions** system property. However, consider the performance impact that a large flow may have on your instance.

## Trigger options for record updates

Flow designers can specify how often a flow can update a particular record with the **Run Trigger** option. Use the **Once** option when you want a flow to run only once. The first time a record is updated, the flow runs, but any further record updates do not trigger the flow. Use the **Always** option when you want the flow to run every time a record is updated and there is not already an active flow running for it. For example, you might set a flow that assigns an incident record to run only once, and set a flow that notifies the incident watch list to always run. The **Run Trigger** field is only available for these trigger types.

-   Created or Updated
-   Updated

## Direct recursion prevention and indirect recursion limit

To prevent instance outages and consumption of system resources, Workflow Studio ignores any request to start a flow or subflow that is the result of direct recursion. Direct recursion occurs under these conditions.

-   An action calls the same flow that it is part of. For example, a script step makes an API call to a flow.
-   An action or subflow produces a result matching the flow trigger. For example, a flow that runs when an incident record is updated contains an update record action that updates an incident record.

Workflow Studio also limits the number of times a flow can be started from indirect recursion. Indirect recursion occurs under these conditions.

-   The same flow is called multiple times in a chain of subflow calls. For example, if subflow A calls subflow B, and subflow B calls subflow A, then calling either subflow produces indirect recursion.
-   The same flow is triggered multiple times in a chain of subflows. For example, suppose that there are two flows triggered by record creation. Suppose that creating record A triggers flow A and also creates record B. Furthermore, creating record B triggers flow B and creates record A. Creating either record type produces indirect recursion.

By default, the system stops triggering flow runs after the run count reaches the indirect recursion limit of three runs. Administrators can change the limit by setting the system property **com.glide.hub.flow\_engine.indirect\_recursion\_limit** to an integer value equal to or greater than one. The system ignores any property value less than one and instead uses a limit of one. Consider the performance impact that increasing the indirect recursion limit may have on your instance.

**Note:** By default, a transaction quota rule prevents flows from running longer than an hour.

## Flow and action testing

Testing a flow bypasses the trigger conditions and immediately runs it. Testing a flow with a record-based trigger requires selecting a specific record to act as the trigger. Flow designers should generate appropriate sample records prior to testing. For more information about testing a flow, see [Test a flow](../task/flow-test.md).

During the design phase, you can test unpublished actions by setting **Show draft actions** on the flow. If testing with draft actions, use these guidelines.

-   Design flows and actions on a non-production instance. Only deploy active, working flows to your production instance.
-   Leave **Show draft actions** set to true until your draft action is in a final state. Once final, publish each action, set **Show draft actions** to false, and activate the flow.

    **Warning:** Disabling **Show draft actions** before publishing your actions removes all draft actions from your flow.

-   Any change you make to an active flow or published action causes it to return to a draft state. If the flow is triggered, the system only runs the activated flow and published actions, and the flow execution details only display what was run. When there is a draft of an active flow, the trigger and actions listed in the flow execution details may be different than those listed in the draft flow.

**Parent Topic:**[Exploring flows](../../workflow-studio/concept/exploring-flows.md)

