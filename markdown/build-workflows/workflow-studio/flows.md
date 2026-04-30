---
title: Building flows
description: Workflow Studio is the default ServiceNow AI Platform process automation builder used to create flows. Workflow Studio replaces the Workflow Editor.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Use, Workflow Studio, Build workflows]
---

# Building flows

Workflow Studio is the default ServiceNow AI Platform process automation builder used to create flows. Workflow Studio replaces the Workflow Editor.

Flows consist of a trigger and a sequence of actions and flow logic. When you add actions and flow logic to a flow, the data collected or created appears in the data panel, which you can use in other actions and flow logic.

Building and managing flows requires that you have some familiarity with the ServiceNow AI Platform tables and fields that the application or process uses. Process analysts can create flows using available actions and flow logic, or they can copy an existing flow to use it as a template.

## Action limit

By default, flows can have no more than 50 actions. To change the default behavior, increase the value of the **sn\_flow\_designer.max\_actions** system property. However, consider the performance impact that a large flow may have on your instance.

## Missing actions

If an administrator added your flow from an update set, you might have some missing actions in your flow. This normally happens when your instance doesn't have the appropriate Integration Hub spokes installed. For more information on how to install the spokes you need to get these actions to appear, see [spokes](spokes.md).

## More Actions menu

Select the **More Actions** icon \(![More Actions icon](../images/MoreActionsIcon.png)\) to access additional options for your flow.

-   **Stages**

    Access the stages for a flow.

-   **Manage flow catalog variables**

    Manage the catalog variables available to Service Catalog-triggered-flows.

-   **Flow Variables**

    Create flow variables to set and retrieve data throughout a flow.

-   **Copy flow**

    Create a copy of the open flow in an application you specify.

-   **Flow preferences**

    Enable or disable the **Show draft actions**, **Show triggered flows**, **Show store spokes**, and **Show inline script toggle** options.

-   **Create code snippet**

    Generate a code snippet to call a specific flow, subflow, or action.

-   **Manage security**

    Enable or disable the **Callable by Client API** option.

-   **Change default flow title**

    Change the default title for your flow by adding styled or dynamic text. For more information, see [Create a natural language title](../task/manage-natural-language-title.md).


## Testing flows

You can test a flow directly from the Workflow Studio interface. Each test runs your flow as if the trigger conditions were met. If the flow has record trigger, you can specify the record to use for your test. After the flow runs, use the flow execution details to verify that your flow is running properly.

**Important:** Always run tests on a non-production instance where flow record changes cannot interfere with your production data.

## Flow execution details

Each time you test a flow, the system generates flow execution records, log messages, and reports. The flow context is a related record containing the current state and runtime values of the flow. The system generates a context record each time a flow is run.

Optionally, you can configure the system to generate execution details anytime a flow is run, not just during testing. For more information, see [Activate flow reporting](../task/enable-flow-reporting.md#).

## Flow properties

The flow properties contain information about your flow. In the main header, select **Properties** to view or edit your flow's properties.

<table id="table_qpc_hyv_5fb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the flow

</td></tr><tr><td>

Protection

</td><td>

Choose whether the flow is read only by choosing from **None** or **Read-only**

</td></tr><tr><td>

Application

</td><td>

Select an application for the flow. This property is set when creating the flow and cannot be changed afterwards.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the flow.

</td></tr><tr><td>

Run As

</td><td>

Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows.

 To create a flow that can run with a personal OAuth token, select the user who initiates the session option. If the user who is running the flow has a personal OAuth token, the flow runs with that token. For more information about creating a personal OAuth token, see [OAuth 2.0 credentials](https://www.servicenow.com/docs/access?context=oauth-2-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Run with role\(s\)

</td><td>

Roles that the flow runs with. This option is only available when **Run as** is set to **user who initiates the session**.

</td></tr></tbody>
</table>## Printing flows

Workflow Studio supports multipage printing for flows, subflows, actions, and flow execution details. For a list of supported browsers, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

## Roles

To access Flows, a user must have the flow\_designer or admin roles.

## General guidelines

Flows should be short, modular, reusable collections of work. If they take more than an hour to execute, they’re probably too long and can be more efficient.

Any general guidelines that apply to flows also apply to [subflows](flows.md#subflows-design-considerations).

-   **Prevent conflicting or duplicate business logic**

    Automations can be created with Flow Designer, business rules, workflows, and Integration Hub. Before you start using Workflow Studio, make sure you understand how existing ServiceNow AI Platform automations work. Deactivate automations before replacing them with Workflow Studio flows and actions. See the [Architecture Overview](flow-designer-arch-overview.md) to learn how Workflow Studio works within the ServiceNow AI Platform.

    Review [Flows](flows.md), [Sub-flows](subflows.md), and [Actions](actions.md) documentation, if necessary.

-   **Determine whether your flow needs a trigger or variable input**

    Flows always run when their trigger conditions are met. Triggers always provide the same data as input for flows. If you need variable input to initiate a flow instead, create a [subflow](flows.md#subflows-design-considerations).

-   **Reuse business logic**

    Create a set of reusable operations as a subflow that can then be used in multiple flows.

-   **Grant flow roles to access role-protected data and preserve user information**

    Flow roles help keep permissions for your flows simple. Use flow roles to preserve user information and grant access to data, instead of running a flow as the system user. Adding flow roles also gives access to additional data that a user-initiated flow does not usually have. The roles granted only apply to the flow. They do not apply to the user who initiated the flow.

-   **Use flow logic or a schedule-based trigger to control flow timing**

    Flow logic or schedule-based triggers help to optimize the performance of your flows. Do not use the gs.sleep\(\) method to wait within a flow. The gs.sleep\(\) method prevents the thread from performing other work. To run a flow at a specific time, use a schedule-based trigger. To pause a flow for a specific duration, use the [Wait for a duration](flow-logic-wait-for-a-duration.md) or [wait for condition](../reference/wait-for-condition-flow-designer.md) flow logic.

-   **Avoid dependencies**

    Parallel branches that depend on each other stall a flow when a branch has to wait for output from another branch.

-   **Scope loop counters**

    Script loops don't have a maximum number of iterations, so loops execute infinitely when there is not a valid exit condition.

    To make sure that there is a valid exit condition, use scope loop counters in inline scripts or in script steps within an action. Add `var` to`for (i=0; i< length; i++)` and get `for (var i=0; i< length; i++)`

-   **Limit For Each and Do Until loops to 1000 iterations**

    Iterations with 1000 or more loops can lead to memory issues.

    -   Set max records on Look Up Records to 1000.
    -   Avoid changing property sn\_flow\_designer.max\_iterations, which defaults to 1000.
    -   For large amounts of data processing, consider batching into smaller batches.
    -   For bulk imports, consider [concurrent imports](https://www.servicenow.com/docs/access?context=concurrent-imports&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).
-   **Use QuickAPI for faster executions \(business rule alternative\)**
    -   [QuickAPI](https://www.servicenow.com/docs/access?context=ScriptableFlowRunnerScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) executions are much faster, but there is less debugging capability.
    -   Foreground QuickAPI executions run in the user session as the user who called the flow.
    -   Background QuickAPI executions run in a background thread and are run in the ‘system’ user session.
-   **Use Do Until loops instead of calling flows from themselves**

    A flow calling itself is not allowed and errors out. But if flow A is calling flow B, then flow B can call flow A up to three times.

-   **Execute flows in the background**

    Executing flows in the background enables UI threads to be released rather than keeping users waiting for flow executions.

-   **Avoid flow logic that waits after collecting a large output**

    Using a large payload immediately after it is retrieved can help prevent memory issues.

-   **Minimize switching between environments**

    Constantly switching back and forth between instance and MID Server steps in a flow can lead to delays in processing. To minimize the risk of delays, limit switching between instance and MID to only one time.

-   **Include sys\_complex\_object records generated by the flow in update sets**

    Missing [complex data](complex-data.md) schemas can cause execution issues. Make sure you include sys\_complex\_object records generated by the flow in update sets.

-   **Calling flows from a script**

    Start flows with a custom trigger by calling from a script.

-   **Avoid deploying newer release flows to instances on older releases**

    Workflow Studio does not support deploying newer release flows to instances running on earlier releases.

    **Danger**

    The flow data model can change between releases, which can prevent newer flows from running or produce unexpected results when running on earlier release instances. Upgrade your instances to be on the same release versions before deploying them.

-   **Turn flow reporting off in production**

    Minimize the amount of memory required to run flows by disabling [Flow reporting](../task/enable-flow-reporting.md#). Flow reporting stores configuration and runtime information for the Execution Details page. These reports are good for troubleshooting, but requires a large amount of data to be retained both in memory and in the database. By default, flow reporting is disabled, and the system only generates execution details when you manually test a flow or action. Instead you can use log files, which are still available when reporting is turned off.

-   **Reduce the amount of memory consumed in flows with nested looping**

    When reporting is activated, set com.snc.process\_flow.reporting.iteration.lastn to a value of "1" to reduce the amounts of the amounts of memory that previous loop iterations consume. The more iterations you report on, the more memory is required.


-   **[Create a flow in Workflow Studio](../task/create-flow.md)**  
Run a sequence of actions and flow logic when the trigger conditions occur.
-   **[Flow and subflow stages](flow-designer-stages.md)**  
Communicate the current stage of a request, flow, or subflow with an end user.
-   **[Flow error handler](flow-error-handler.md)**  
Enable flows to catch errors. Run a sequence of actions and subflows to identify and correct issues. For example, have flows log output values, send notifications, and run corrective subflows when they produce an error.
-   **[Flow history](flow-history.md)**  
View and manage the history of a flow. See past configurations of a flow to copy, restore, or remove them.
-   **[Flow Template Builder](flow-template.md#)**  
Enable citizen developers to create their own flow templates. Flow Templates guide flow authors to create flows for common use cases. Use the flow template builder to define flows, actions, and flow template variables.
-   **[Inline scripts](inline-scripts.md)**  
Enable users with coding experience to write inline scripts that set and modify input values during the configuration of an action or flow. Use inline scripts to modify input values that require small format conversions, data transformations, or math operations.
-   **[Summarize a flow](../task/summarize-a-flow.md)**  
Generate a summary of a flow with Now Assist for Creator.
-   **[Flow variables](flow-variables.md)**  
Similar to Workflow scratchpad variables, create variables that you can use and modify directly in your flow. Access flow variables as data pills directly in the Data panel.

**Parent Topic:**[Using Workflow Studio](../../workflow-studio/reference/building-workflow-studio-components.md)

