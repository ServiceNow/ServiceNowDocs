---
title: Create an activity definition
description: Specify the action or subflow you want an activity to run. Configure the inputs you want playbook designers to set when adding the activity to a playbook. Select the experience you want end users to have when the activity runs.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Activity definitions, Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Create an activity definition

Specify the action or subflow you want an activity to run. Configure the inputs you want playbook designers to set when adding the activity to a playbook. Select the experience you want end users to have when the activity runs.

## Before you begin

-   Create a Workflow Studio [subflow](../../flow-designer/task/create-subflow.md) or [action](../../flow-designer/task/create-action.md) that you want to use as the automation plan for your activity. For example, see [Create an action as an activity automation plan](create-automation-plan.md).
-   Make sure to set your current application to the application that you want your activity to run in. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).
-   Role required: admin, playbook.admin, or pd\_content\_author

## Procedure

1.  To start creating a new activity definition, do one of the following:

    -   Navigate to **Process Automation** &gt; **Process Automation Administration** &gt; **Activity Definitions**. Then in the context header, click **New**.
    -   Follow the steps to [Create a playbook](create-process-definition.md). Then in the Playbooks activity design space, click **Add an activity** &gt; **Create a new activity**.
    The Activity Definition form view appears.

2.  Fill in the Activity Definition form fields.

<table id="choicetable_ndc_pgy_5lb"><thead><tr><th align="left" id="d175240e170">

Field

</th><th align="left" id="d175240e173">

Action

</th></tr></thead><tbody><tr><td id="d175240e179">

**Label**

</td><td>

Enter a unique name for your activity.

 This name appears in the playbook in both the Workflow Studio Playbooks builder as well as during playbook runtime.

</td></tr><tr><td id="d175240e206">

**Table**

</td><td>

Select a table whose records the activity can access as inputs. When adding inputs to your activity in the Workflow Studio Playbooks builder, you can dot-walk to dynamic record data from this table. See [Dot-walking to data in related tables](https://www.servicenow.com/docs/access?context=c_DotWalking&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

 **Note:** The table specified for a playbook's triggering input record overrides the activity definition table at design time. See [Triggers](../concept/process-automation-designer-triggers.md)

</td></tr><tr><td id="d175240e250">

**Description**

</td><td>

Optionally, enter some descriptive details about your activity.

</td></tr><tr><td id="d175240e259">

**Accessible From**

</td><td>

Choose one of the following options:-   **All application scopes** - You can add this activity to a playbook in any application scope.
-   **This application scope only** - You can only add this activity to playbooks within the same application scope specified in the **Application** field.


</td></tr><tr><td id="d175240e288">

**Required Roles**

</td><td>

Add roles that are allowed to access activities that use this activity definition. ![Required roles field in an activity definition](../images/required-roles-activity-def.png)

**Note:** Users who can view the playbook but who do not have the required role to access activities with this activity definition will have a read-only view of these activities.

</td></tr></tbody>
</table>3.  Under the Automation Plan section next to the **Flow or Action** field, click the lookup documents using list icon \(![Lookup documents using list icon](../../flow-designer/images/lookup-using-list-icon.png)\).

    The Select the document screen appears.

4.  In the Table Name list, select one of the following options:

    -   To use a Workflow Studio subflow to automate your activity, select **Flow**.
    -   To use a Workflow Studio action to automate your activity, select **Action Type**.
    **Note:** You can only use published actions or subflows for an activity definition's automation plan.

5.  Next to the **Document** field, click the lookup documents using list icon \(![Lookup documents using list icon](../../flow-designer/images/lookup-using-list-icon.png)\).

    The Flows or Action Types screen appears.

6.  From the list, select the subflow or action that you want to use to automate your activity.

7.  Select **OK**.

8.  From the list, select an UI Layout for the properties and components that you want your activity to use when it renders in a user-facing view of your playbook.

    For more information, see [UI Layouts](../concept/experience-types.md).

9.  Click **Submit** to save and create your activity definition record.

    The Activity Definitions list view appears.

10. Under the **Label** column in the list, select your activity definition.

    The Activity Definition form view appears.

11. Select the Automation Plan section.

    The system displays the available variables for the action or subflow. The Workflow Studio Playbooks builder displays a variable for each action or subflow input.

12. For each variable, configure the default value you want each variable to have.

    Leave a variable blank when you want a playbook designer to configure the value when adding the activity to a playbook.

13. For each variable, select where it is visible.

    |Visibility|Description|
    |----------|-----------|
    |**Include in standard modal**|Only displays the variable as an input from the Advanced properties modal.|
    |**Include in standard modal and configuration panel**|Displays the variable as an input in the properties panel and the Advanced properties modal.|
    |**Admin visibility only**|Only displays the variable as an input from the Advanced properties modal to users that have the admin or playbook.admin roles.|

    Playbook designers can only set values for variables that they have access to.

14. Select the Activity Experience tab.

15. Next to the **UI Layout** field, select the list icon \(![Lookup documents using list icon](../../flow-designer/images/lookup-using-list-icon.png)\).

    The Activity UI Layouts list appears.

16. Select the UI Layout you want to use.

17. Right-click in the header of the activity definition, and select **Save**.

18. Under the Associated Record section, select values for the **Associated table** and **Associated record** fields.

    These values are typically Record and Table Name outputs for the Workflow Studio subflow or action specified in your activity's automation plan. For example, you can click the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon-01.png)\) next to the **Associated record** field and dot-walk to the Table Name output by selecting **VL** &gt; **Add Comment** &gt; **Outputs** &gt; **task** &gt; **Approval**.

    The system associates a record with your activity so that, when the activity runs, it knows which record's data to output.

    ![Use the data pill picker to add an associated table and record to your activity definition.](../images/add-associated-table-activity-def-demo.gif)

19. If you want to set up the default activity data that renders in your playbook during runtime, enter the values for that data in the other sections under Activity Experience.

    The sections and fields that appear under Activity Experience vary depending on the UI Layout that you select. For more information, see [UI Layouts](../concept/experience-types.md).

20. Click **Update** to finish creating your activity definition.


## Result

You can now select your custom activity from the activity picker in the Workflow Studio Playbooks design environment. Select the appropriate application scope for your activity to view it in the picker.

**Parent Topic:**[Activity definitions](../concept/activity-definitions.md)

**Related topics**  


[Create an action as an activity automation plan](create-automation-plan.md)

[UI Layouts](../concept/experience-types.md)

