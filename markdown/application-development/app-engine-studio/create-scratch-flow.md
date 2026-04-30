---
title: Add a flow from scratch
description: If an existing automation template doesn't fit your application goal, define custom automation in App Engine Studio \(AES\) by building a new flow.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Add logic and automation, Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add a flow from scratch

If an existing automation template doesn't fit your application goal, define custom automation in App Engine Studio \(AES\) by building a new flow.

## Before you begin

Role required: sn\_app\_eng\_studio.user or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

If a pre-built flow already exists, you can easily add its template to your app and then customize it. For more information, see [Add a pre-built flow using a template](use-flow-template.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, in the Logic and Automation section, select **Add**.

4.  Select the card for **Flow**.

5.  Select **Build from scratch**.

    ![Select to build the flow from scratch](../image/aes-automation-scratch-purple.png "Build from scratch")

6.  On the form, fill in the fields and then select **Continue**.

<table id="table_qf3_nxp_b4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify your flow.

</td></tr><tr><td>

Description

</td><td>

Description of your flow.

</td></tr><tr><td>

Protection

</td><td>

Access settings for the flow. You can select one of the following options:-   **-- None --**

Option to enable other users to edit the flow.

-   **Read-only**

Option to enable other users to view the flow but not edit it.

</td></tr><tr><td>

Run as

</td><td>

Selection to specify if the flow runs as a system user or the user who initiates the session. If updates should come from the user who triggered the flow, select **User who initiates session**. For example, when you want incident record comments to come from the current user, or approval emails to originate from the approver.

</td></tr><tr><td>

Run with roles

</td><td>

Roles that the flow runs with. This option is available only when **Run as** is set to **User who initiates session**.

 To use a custom role for your flow, you must create one in **Security** first. For more information, see [Add application security](../concept/add-security.md).

</td></tr></tbody>
</table>7.  On the summary screen, select **Edit this flow** to open your flow.

    ![Create the flow](../image/fd-aes-2.png "Flow Designer")

    For an example of how to build a flow, see [Build your first flow in Flow Designer](https://www.servicenow.com/docs/access?context=build-your-first-flow&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

8.  Add a trigger to your flow.

    1.  Under the TRIGGER section, select **Add a trigger**.

    2.  From the Trigger list, select a trigger that will start running your flow.

        For more information on trigger types, see [Workflow Studio flow trigger types](https://www.servicenow.com/docs/access?context=flow-triggers&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

        The system displays a set of fields depending on the type of trigger that you've selected.

    3.  Set up your trigger by filling in the fields.

        For a record-based trigger, for example, select a table and set field conditions that, when met, will start running your flow.

    4.  Click **Done**.

9.  To add actions, flows, subflows, or flow logic, select **Add an Action, Flow Logic, or Subflow**.

    1.  Select an option.

<table id="table_smq_3ys_tcb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Select the desired action. Workflow Studio includes [Workflow Studio actions](https://www.servicenow.com/docs/access?context=flow-actions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) that are available to flows and subflows. Alternatively, a user with the action\_designer role can create additional actions to add to flows. The [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) and [Spokes](https://www.servicenow.com/docs/access?context=spokes&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) plugins install additional actions.

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

10. To specify how the app will handle errors, enable the **ERROR HANDLER** switch and fill in the fields.

    For more information on configuring how errors are handled in flows, see [Flow error handler](https://www.servicenow.com/docs/access?context=flow-error-handler&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

11. Select **Save**.

    The ServiceNow AI Platform saves a draft of the flow, trigger, and actions.


## What to do next

Test your flow until you're ready to activate it. For more information on testing and editing flows, see [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Note:** Your application can trigger only activated flows.

-   **[Modify a flow](edit-flow.md)**  
To update or change an existing flow for an app you built in App Engine Studio \(AES\), edit it.

**Parent Topic:**[Add logic and automation](../concept/add-automation.md)

