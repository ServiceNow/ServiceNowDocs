---
title: Create an activity definition
description: Specify the action or subflow you want an activity to run. Configure the inputs you want playbook designers to set when adding the activity to a playbook. Select the experience you want end users to have when the activity runs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/create-activity-definition.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 6
breadcrumb: [Activity definitions, Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Create an activity definition

Specify the action or subflow you want an activity to run. Configure the inputs you want playbook designers to set when adding the activity to a playbook. Select the experience you want end users to have when the activity runs.

## Before you begin

-   Create a Workflow Studio [subflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-subflow.md) or [action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-action.md) that you want to use as the automation plan for your activity. For example, see [Create an action as an activity automation plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-automation-plan.md).
-   Make sure to set your current application to the application that you want your activity to run in. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).
-   Role required: admin, playbook.admin, or pd\_content\_author

## Procedure

1.  To start creating a new activity definition, do one of the following:

    -   Navigate to **Process Automation** &gt; **Process Automation Administration** &gt; **Activity Definitions**. Then in the context header, click **New**.
    -   Follow the steps to [Create a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-process-definition.md). Then in the Playbooks activity design space, click **Add an activity** &gt; **Create a new activity**.
    The Activity Definition form view appears.

2.  Fill in the Activity Definition form fields.

<table id="choicetable_ndc_pgy_5lb"><thead><tr><th align="left" id="d182499e162">

Field

</th><th align="left" id="d182499e165">

Action

</th></tr></thead><tbody><tr><td id="d182499e171">

**Label**

</td><td>

Enter a unique name for your activity.

 This name appears in the playbook in both the Workflow Studio Playbooks builder as well as during playbook runtime.

</td></tr><tr><td id="d182499e198">

**Table**

</td><td>

Select a table whose records the activity can access as inputs. When adding inputs to your activity in the Workflow Studio Playbooks builder, you can dot-walk to dynamic record data from this table. See [Dot-walking to data in related tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_DotWalking.md).

 **Note:** The table specified for a playbook's triggering input record overrides the activity definition table at design time. See [Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-triggers.md)

</td></tr><tr><td id="d182499e242">

**Description**

</td><td>

Optionally, enter some descriptive details about your activity.

</td></tr><tr><td id="d182499e251">

**Accessible From**

</td><td>

Choose one of the following options:-   **All application scopes** - You can add this activity to a playbook in any application scope.
-   **This application scope only** - You can only add this activity to playbooks within the same application scope specified in the **Application** field.


</td></tr><tr><td id="d182499e280">

**Required Roles**

</td><td>

Add roles that are allowed to access activities that use this activity definition. \[Omitted image "required-roles-activity-def.png"\] Alt text: Required roles field in an activity definition

**Note:** Users who can view the playbook but who do not have the required role to access activities with this activity definition will have a read-only view of these activities.

</td></tr></tbody>
</table>3.  Configure the **Automation Plan**.

    1.  Next to the **Flow or Action** field, click the lookup documents using list icon \(\[Omitted image "lookup-using-list-icon.png"\] Alt text: Lookup documents using list icon\).

        The Select the document screen appears.

    2.  In the Table Name list, select one of the following options:

        -   To use a Workflow Studio subflow to automate your activity, select **Flow**.
        -   To use a Workflow Studio action to automate your activity, select **Action Type**.
        **Note:** You can only use published actions or subflows for an activity definition's automation plan.

    3.  Next to the **Document** field, select the lookup documents using list icon \(\[Omitted image "lookup-using-list-icon.png"\] Alt text: Lookup documents using list icon\).

        The Flows or Action Types screen appears.

    4.  From the list, select the subflow or action that you want to use to automate your activity.

    5.  Select **OK**.

    6.  Right-click in the header of the activity definition, and select **Save**.

        The system displays the available variables for the action or subflow. The Workflow Studio Playbooks builder displays a variable for each action or subflow input.

    7.  For each variable, configure the default value you want each variable to have.

        Leave a variable blank when you want a playbook designer to configure the value when adding the activity to a playbook.

4.  For each variable, select where it is visible.

    |Visibility|Description|
    |----------|-----------|
    |**Always show**|Displays the input in the properties panel.|
    |**Show as additional property**|Displays the input in the properties panel only when playbook authors select **Show additional options**.|
    |**Show as additional property for Playbook admins only**|Displays the input in the properties panel when users with the playbook.admin role select **Show additional option**. The input is hidden for any other users.|

    Playbook designers can only set values for variables that they have access to.

5.  Configure the **Activity Experience**.

    1.  In the Activity Experience tab, next to the **UI Layout** field, select the list icon \(\[Omitted image "lookup-using-list-icon.png"\] Alt text: Lookup documents using list icon\).

        The Activity UI Layouts list appears.

    2.  Select the UI Layout you want to use.

    3.  Right-click in the header of the activity definition, and select **Save**.

    4.  Under the Associated Record section, select values for the **Associated table** and **Associated record** fields.

        These values are typically Record and Table Name outputs for the Workflow Studio subflow or action specified in your activity's automation plan. For example, you can click the data pill picker icon \(\[Omitted image "data-pill-picker-icon-01.png"\] Alt text: Data pill picker icon\) next to the **Associated record** field and dot-walk to the Table Name output by selecting **VL** &gt; **Add Comment** &gt; **Outputs** &gt; **task** &gt; **Approval**.

        The system associates a record with your activity so that, when the activity runs, it knows which record's data to output.

        \[Omitted image "add-associated-table-activity-def-demo.gif"\] Alt text: Use the data pill picker to add an associated table and record to your activity definition.

    5.  To set up the default activity data that renders in your playbook during runtime, enter the values for that data in the other sections under Activity Experience.

        The sections and fields that appear under Activity Experience vary depending on the UI Layout that you select. For more information, see [UI Layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/experience-types.md).

6.  In the **AI Agents** tab, select **On** to enable AI agents for the activity.

    AI Agents are supported for form-based activities. If you enable AI Agents for an activity, complete the following fields to configure the AI Agents.

    \[Omitted image "activity-definition-ai-agents.png"\] Alt text: Configure AI agents for the activity.

<table id="table_bzc_n2f_zjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Child Agents

</td><td>

Provides the option to add custom agents to the activity.To add custom agents to your activity, select the lock icon \[Omitted image "icon-lock.png"\] Alt text:.

</td></tr><tr><td>

Run as

</td><td>

Lets you select the user on whose behalf the activity runs - the user that triggered the playbook or the user who completed a previous activity.

</td></tr><tr><td>

AI agent instructions

</td><td>

Adds default instructions for the AI Agents in the activity. The playbook author can update these instructions.

</td></tr><tr><td>

Autonomous support

</td><td>

Enables you to configure the AI Agents to complete actions autonomously, without human intervention. Use the **Supported actions** field to define the autonomous actions.

</td></tr><tr><td>

Supported actions

</td><td>

Specifies the actions that the AI Agents can perform autonomously in the activity.Select the lock icon \[Omitted image "icon-lock.png"\] Alt text: and choose the actions to enable for autonomous support.

-   Update Record: The AI Agents can update records autonomously.
-   Create Record: The AI Agents can create records autonomously.
-   Mark Complete: The AI Agents can autonomously mark the record complete. The playbook then proceeds to the next activity.


</td></tr><tr><td>

AI agent autonomous instructions

</td><td>

Adds default instructions for the autonomous AI Agents in the activity. The playbook author can update these instructions.

</td></tr></tbody>
</table>7.  Select **Submit** to finish creating your activity definition.


## Result

You can now select your custom activity from the activity picker in the Workflow Studio Playbooks design environment. Select the appropriate application scope for your activity to view it in the picker.

**Parent Topic:**[Activity definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/activity-definitions.md)

**Related topics**  


[Create an action as an activity automation plan]()

[UI Layouts]()

