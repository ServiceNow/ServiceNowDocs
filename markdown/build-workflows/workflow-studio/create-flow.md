---
title: Create a flow in Workflow Studio
description: Run a sequence of actions and flow logic when the trigger conditions occur.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a flow in Workflow Studio

Run a sequence of actions and flow logic when the trigger conditions occur.

Create a flow with Workflow Studio 

## Before you begin

-   Create or select an application to store your Workflow Studio content.
-   Role required: flow\_designer or admin

## About this task

Users with the flow\_designer or admin role should know the application table structure and be aware of any existing business logic associated with the target tables of a flow or subflow. Be sure to disable any conflicting business rules or workflows before creating a flow or subflow.

Creating a custom application to contain your Workflow Studio content enables you to [deploy](https://www.servicenow.com/docs/access?context=c_SharingApplications&version=australia&pubname=australia-application-development&ft:locale=en-US) the application using the application repository or the ServiceNow Store.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **New** &gt; **Flow**.

3.  Select whether to build the flow with Now Assist or to build the flow from scratch.

    To build a flow with Now Assist, see [Create a flow with Now Assist](create-flow-now-assist.md).

    To build a flow from scratch, continue to the next step.

4.  Select the **Build from scratch** tab.

5.  On the Flow Properties screen, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Flow name|Name to uniquely identify your flow. The system converts the flow name into an internal name by replacing space characters with underscore characters.|
    |Description|Description of your flow.|
    |Application|Application scope to create your flow in. Global is the default. The application scope determines what data your flow can access and what data it can share.|
    |Domain|Domain scope of the flow. For more information about domain separation, see [Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=australia&pubname=australia-platform-security&ft:locale=en-US).|

<table id="table_ltx_mlf_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Protection

</td><td>

Selection to specify if the flow is read-only. You can only select a value when you create the flow in an application scope that you own.

</td></tr><tr><td>

Run as

</td><td>

Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows.

 **Note:** By default, flows run as the user who initiates the session.

 To create a flow that can run with a personal OAuth token, select the user who initiates the session option. If the user who is running the flow has a personal OAuth token, the flow runs with that token. For more information about creating a personal OAuth token, see [OAuth 2.0 credentials](https://www.servicenow.com/docs/access?context=oauth-2-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

 When flows run as the user who initiates the session, the system limits flow actions by user ACL restrictions. Ensure that security restrictions don't prevent users who trigger the flow from performing flow actions. Flows run by the initiating user also respect user-specific settings such as date/time formats.

 **Note:** Inbound email flows ignore this setting and always run as the user who initiates the session. To test access controls for an inbound email flow, impersonate a typical inbound email user and manually trigger the flow.

</td></tr><tr><td>

Run with roles

</td><td>

Roles that the flow runs with. This option is only available when **Run as** is set to **user who initiates the session**.

</td></tr><tr><td>

Flow Priority Default

</td><td>

Priority level at which you want the system to run this flow by default. Options include:

-   Low
-   Medium \(Default\)
-   High
 To learn about flow priority levels, see [Flow priority](../concept/flow-priority.md).

</td></tr></tbody>
</table>6.  Select **Submit**.

    **Note:** If this is your first time in Workflow Studio, a welcome screen appears. You can choose to either take the welcome tour or skip the tour for now.

    The system displays the Workflow Studio design environment.

7.  Create a trigger for the flow.

    **Tip:** You can either create a trigger for the flow or use a saved trigger. To use a saved trigger, proceed to the next step.To learn more about saved triggers, see [Building triggers](../concept/building-triggers.md)

    1.  Under the TRIGGER section, select **Add a trigger**.

    2.  From the Trigger list, select a trigger that will start running your flow.

        For more information on trigger types, see [Workflow Studio flow trigger types](../reference/flow-triggers.md).

        The system displays a set of fields depending on the type of trigger that you've selected.

    3.  Set up your trigger by filling in the fields.

        For a record-based trigger, for example, select a table and set field conditions that, when met, will start running your flow.

    4.  Click **Done**.

8.  Select a saved trigger for the flow.

    Skip this step if you have already created a trigger in the previous step.

    1.  Under the TRIGGER section, select **Add a trigger**.

    2.  From the Trigger list, under INSTALLED SPOKES, select the application under which the trigger was created.

        For example, Global.

        Workflow Studio displays a list of triggers that are in the selected application.

    3.  Select the trigger.

        Depending on how the trigger is configured, you may be able to view the trigger properties or add additional conditions to the trigger.

    4.  Select **Done**.

9.  To add actions, flows, subflows, or flow logic, select **Add an Action, Flow Logic, or Subflow**.

    1.  Select an option.

<table id="table_smq_3ys_tcb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Select the desired action. Workflow Studio includes [Workflow Studio actions](../concept/flow-actions.md) that are available to flows and subflows. Alternatively, a user with the action\_designer role can create additional actions to add to flows. The [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [Spokes](../concept/spokes.md) plugins install additional actions.

 To add draft actions from the More Actions menu, set **Show draft actions** to **true**.

 To view spokes that are available in the ServiceNow Store, set **Show store spokes** to **true** from the More Actions menu.

**Note:** Under **Not Installed Spokes**, the system displays spokes that are available in the ServiceNow Store based on compatibility with the ServiceNow version and application dependency on Workflow Studio.

</td></tr><tr><td>

Flow Logic

</td><td>

Select an option to specify conditional or repeated operations.

</td></tr><tr><td>

Subflow

</td><td>

Select a published subflow and define the input values. In addition to adding a subflow as a flow action, you can enable the **Show triggered flows** option from the More Actions menu to select an activated flow and define the required inputs. Running a triggered flow ignores its trigger conditions and runs all actions.

</td></tr></tbody>
</table>        To change the order of an action in a flow, drag the handle on the left side of the action to the desired location.

        The system displays a set of fields depending on the option that you selected.

    2.  To configure the action, flow logic, or subflow, fill in the fields.

    3.  Select **Done**.

    4.  Repeat adding actions until complete.

10. Select **Save**.

    Workflow Studio saves a draft of the flow, trigger, and actions.


## What to do next

-   Test your flow until you're ready to activate it.

    **Note:** The system only triggers activated flows.

-   Deploy or transfer your flow to another instance.
    -   [Deploy](https://www.servicenow.com/docs/access?context=c_SharingApplications&version=australia&pubname=australia-application-development&ft:locale=en-US) your flow from the application repository when your application is complete and ready for release.
    -   [Transfer](https://www.servicenow.com/docs/access?context=update-set-transfers&version=australia&pubname=australia-application-development&ft:locale=en-US) your flow from an update set XML file when you want to test the flow on another instance. When you save a flow, Workflow Studio generates a single update set file containing its subflows and actions.

-   **[Create a flow with Now Assist](create-flow-now-assist.md)**  
Use generative AI to create a flow from text directionsand images.
-   **[Create a flow with an inbound email trigger](create-inbound-email-flow.md)**  
Start a flow when your instance receives an email.
-   **[Create a flow with a Kafka Message trigger](create-flow-kafka.md)**  
Build a flow that processes events from a Kafka stream. Start the flow when an event is available in the specified topic.
-   **[Create a flow with a MetricBase trigger](create-mb-flow.md)**  
Start a flow when a MetricBase trigger is met. MetricBase triggers track time series data and can monitor when a threshold is reached, when a trend is detected, or when a system stops reporting data.
-   **[Create a flow with a Proactive Analytics trigger](create-flow-proactive-analytics.md)**  
Use Performance Analytics indicators to start a flow. Define the flow start conditions as a set of Proactive Analytics KPI scores and KPI threshold values.
-   **[Create a flow with a Service Catalog trigger](create-sc-flow.md)**  
Start a flow when a Service Catalog item is requested to automate the fulfillment process.
-   **[Create a flow with an SLA Task trigger](create-sla-task-flow.md)**  
Configure your Service Level Agreement \(SLA\) definition to run a flow as the action plan.
-   **[Create a flow with an external trigger](../../integrationhub/tasks/create-a-flow-with-an-external-trigger-definition.md)**  
Set up a flow with a base system external trigger definition. The flow responds to an event-driven external trigger from a third-party system. For example, run a flow when an issue is created in a third-party issue-tracking system.
-   **[Create a flow with roles](create-flow-roles.md)**  
Create a flow or subflow that runs with assigned roles. Assigning roles enables you to create a user-initiated flow that runs with its own roles rather than the user's roles.
-   **[Create flow Service Catalog variables](create-flow-catalog-variables.md)**  
Create Service Catalog variables that are only available to a specific Service Catalog flow. Flow-specific variables are available to catalog tasks and actions in the flow.
-   **[Create a decision table in a flow](create-decision-table-flow.md)**  
Create the structure for a decision table while you author your flow in Workflow Studio. Use data from the flow to create inputs, conditions, and results for the decision table, all in a convenient modal. For example: You can store the logic for incident assignments in a Decision Table, and then use that Decision Table within a flow.
-   **[Copy a flow](copy-flow.md)**  
Copy a flow to give it a new name and move it to another application scope.
-   **[Duplicate an action or subflow](duplicate-action-subflow.md)**  
Duplicate an action or subflow within a flow.
-   **[Test a flow](flow-test.md)**  
Before activating a flow so other users can access it, test to make certain it works the way you expect.
-   **[Activate a flow](flow-activate.md)**  
Activate a flow to make it available to run.
-   **[Change a flow or action's default title](manage-natural-language-title.md)**  
Change the default title for a flow, subflow, or action by adding styled and dynamic text.
-   **[Edit a flow](flow-edit.md)**  
Edit an existing flow.
-   **[Delete a flow](flow-delete.md)**  
Delete a flow that you no longer need.
-   **[View activated flows for a table](view-activated-flows.md)**  
View flows with record-based triggers that run on a specific table.

**Parent Topic:**[Building flows](../concept/flows.md)

