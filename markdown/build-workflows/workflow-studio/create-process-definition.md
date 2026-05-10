---
title: Create a playbook
description: Enable playbook owners to configure and organize multiple instances of Workflow Studio content into an automated business process on the ServiceNow AI Platform.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Create a playbook

Enable playbook owners to configure and organize multiple instances of Workflow Studio content into an automated business process on the ServiceNow AI Platform®.

## Before you begin

-   [Activate Playbooks](../concept/activate-process-automation-designer.md) for your appropriate application.
-   Familiarize yourself with the tables and relationships that your application uses for the playbook that you want to create.
-   Make sure to familiarize yourself with any features that your business uses to automate operations on the ServiceNow AI Platform, such as [flows](../../workflow-studio/concept/exploring-flows.md), [subflows](../../workflow-studio/reference/exploring-subflows.md), and [actions](../../workflow-studio/concept/exploring-actions.md).
-   Learn how to [get started with ServiceNow® Process Automation](../concept/getting-started-process-automation.md).
-   Role required: admin, playbook.admin, or playbook.write. To learn more about playbook authoring access in Workflow Studio, see [User access to Playbooks in Workflow Studio](../concept/user-access-playbooks.md).

## About this task

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

    The Workflow Studio landing page appears. Playbooks are shown by default, but you can toggle to flows, subflows, actions, and decisions.

2.  In the upper right corner, click **New** and select **Playbook** from the drop-down menu.

    The Playbooks builder details screen for a new playbook opens in a new tab.

3.  Fill in the following fields.

    |Field|Action|
    |-----|------|
    |**Playbook name**|Enter a unique, user-facing name for your playbook. This name appears to agents and fulfillers during runtime of your playbook.|
    |**Description**|Optionally, enter some descriptive details about your playbook.|
    |**Application**|Choose an application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationScope.md).|

    The builder displays in **Diagram view** by default, but you can select **Board view** to switch views. Switch between views anytime as you build your playbook.

    ![Diagram and Board view toggle](../images/board-view.png)

4.  Select the **Start** node.

    The **Playbook properties** side panel opens.

5.  Under the **Details** tab, update or fill in the following fields.

<table id="choicetable_vdx_qhw_bgc"><thead><tr><th align="left" id="d107149e332">

Field

</th><th align="left" id="d107149e335">

Action

</th></tr></thead><tbody><tr><td id="d107149e341">

**Playbook name**

</td><td>

Enter a unique, user-facing name for your playbook. This name appears to agents and fulfillers during runtime of your playbook.

</td></tr><tr><td id="d107149e356">

**Parent table**

</td><td>

Select the table that you want your trigger records and other playbook inputs to come from.**Note:** This field is required for Knowledge and Email activities.

</td></tr><tr><td id="d107149e367">

**Description**

</td><td>

Optionally, enter some descriptive details about your playbook.

</td></tr><tr><td id="d107149e379">

**Limit playbook executions for each parent record to**

</td><td>

Limit the number of times a playbook can run for a single parent record.

</td></tr><tr><td id="d107149e389">

**Allow this playbook to be restarted during runtime**

</td><td>

Allow runtime users to restart the entire playbook during a run.

</td></tr></tbody>
</table>6.  Under the **Inputs** tab, add inputs for a playbook to launch with.

    Inputs defined here are accessible throughout the playbook via dot-walking and dot notation \(e.g. inputs.inputName\) and can be used in activity fields, conditions, and UI elements.

    **Tip:** Use this to trigger a playbook with API inputs instead of trigger records.

7.  Under the **Runtime permissions** tab, add sets of users, user groups, user criteria and roles, and define whether they can add optional activities to the playbook, restart the playbook or its stages and activities, or cancel the playbook during runtime.

8.  [Configure your trigger.](add-configure-trigger.md)

    **Note:** You can create a playbook with no trigger, a single trigger, or multiple triggers.

9.  [Add a stage.](add-configure-stage.md)

10. [Add a decision stage.](create-decision-stage.md)

11. [Add an activity.](add-configure-activity.md)

12. Keep adding stages and activities according to your manual playbook.

    For an example of how to design an entire digitized process with Playbooks, see [Create a sample playbook](design-automated-process.md).

13. If you don't see the activity you need to add in the activity picker, [create an activity definition](create-activity-definition.md).

14. [Add a decision activity.](create-a-decision-activity.md)

15. [Add parallel activities.](create-parallel-activity.md)

16. [Add optional activities.](../concept/optional-activities.md#)

17. After you've added all appropriate stages and activities to your playbook, select **Activate** in the header.

    Activating your playbook publishes it so that it runs when triggered.

    **Note:** If you change your playbook after activating it, the system saves your changes but deactivates your playbook. You must click **Activate** again to publish any new changes to your playbook. For more information, see [Playbook statuses and activation states](../reference/process-status-activation-state.md).


## Result

When your playbook's trigger conditions are met, your playbook runs. As a result, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process that renders as a playbook, see [Create a sample playbook](design-automated-process.md).

## What to do next

Set up the Playbook Experience for your agents and fulfillers.

**Parent Topic:**[Creating and managing Playbooks](../concept/creating-managing-playbooks.md)

