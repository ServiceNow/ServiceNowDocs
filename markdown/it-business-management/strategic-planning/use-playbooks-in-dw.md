---
title: Use playbook for a demand
description: Use the demand workflow default playbook on a demand to complete the activities in each stage and move the demand through its life cycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/strategic-planning/use-playbooks-in-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 4
breadcrumb: [Playbooks in Next Experience for Demand Management, Manage demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Use playbook for a demand

Use the demand workflow default playbook on a demand to complete the activities in each stage and move the demand through its life cycle.

## Before you begin

Role required: it\_demand\_user or it\_demand\_manager

## About this task

The demand workflow playbook guides you through the stages of a demand, such as creating a demand brief, defining demand alignment, and estimating demand cost and effort. Each stage includes activities that you complete before you move to the next stage. For the stages and activities in the default playbook, see [Demand workflow playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/demand-default-playbook-stages.md).

Using the default demand playbook, you can create customized playbooks or create new ones for your governance processes. If your playbooks use the same demand-specific custom activities and playbook experience, follow the steps in this task to complete them. However, some steps might differ based on your customizations. For detailed information on how to use playbooks, see [Workflow Studio playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio-playbooks-landing.md).

**Note:** To find out how to update demand information on the Details page of the demand record, see [Update demand details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/update-the-demand-details-from-dw.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select the **Playbook** tab.

    The **Playbook** tab appears only if a playbook applies to the demand.

    **Note:** Playbooks aren't available for existing demands that were created before the playbook experience was active in the instance.

5.  Select a stage to view its activities.

    Each activity displays its status, such as In Progress, Skipped, or Complete.

6.  Select an activity and enter the required information.

    -   In a form activity, enter or update the fields that the activity displays.

        \[Omitted image "demand-playbook-form.png"\] Alt text: Form activity in a stage.

    -   In a related list activity, you can add an entry or remove one. To view the details of an entry, select it in the list.

        \[Omitted image "demand-playbook-related-list.png"\] Alt text: Related list activity in a stage.

    -   In an activity that creates a record, such as a benefit plan, fill in the form and select **Save**. The record is created and linked to the demand, and the playbook moves to the next activity.
    -   In an instruction activity, follow the message, for example to create resource assignments on the **Resources** tab of the demand. Then return to the playbook and select **Mark Complete**. The **Resources** tab displays resourcing only after both the planned start date and the planned end date of the demand are set.
    For example, in the Define demand details activity of the Create demand brief stage, enter the name, description, and business case of the demand. In the Add stakeholders activity of the Define demand alignment stage, select **New** to add a stakeholder.

7.  Select an action for the activity.

    \[Omitted image "demand-playbook-activities.png"\] Alt text: Actions on an activity.

<table id="choicetable_pb_actions"><thead><tr><th align="left" id="d138458e232">

Action

</th><th align="left" id="d138458e235">

Result

</th></tr></thead><tbody><tr><td id="d138458e241">

**__Mark Complete__**

</td><td>

Saves your changes, marks the activity as complete, and opens the next activity automatically. Use this action when you finish all the work for the activity. If the activity contains mandatory fields, fill them before you mark the activity as complete. Otherwise, an error message asks you to fill the required fields.

</td></tr><tr><td id="d138458e251">

**__Save__**

</td><td>

Saves your changes without completing the activity. The activity stays in progress so that you can return to it later. In an activity that creates a record, **Save** creates the record and completes the activity.

</td></tr><tr><td id="d138458e264">

**__Skip__**

</td><td>

Bypasses the activity and moves you to the next one. Use this action when the activity does not apply to the demand. A skipped activity counts toward finishing the stage. If you skip an activity in a stage that ends with an automated state change, the state is also moved along with the stage.

</td></tr><tr><td id="d138458e274">

**__Restart__**

</td><td>

Reopens a completed or skipped activity so that you can edit it. Completed and skipped activities are read-only. To restart one, select the More options icon on the activity and then select **Restart**. If **Restart** is not available, the activity is configured not to run again. Restarting an activity also reopens the activities after it, but does not change the state of the demand.\[Omitted image "demand-playbook-restart-activity.png"\] Alt text: More actions menu with restart activity.

</td></tr></tbody>
</table>    For example, if the demand doesn't need any tasks yet, select **Skip** on the Add demand tasks activity. If you later need to add a task, select **Restart** on the skipped activity, add the task, and select **Mark Complete**.

    **Note:** At the end of some stages, the playbook moves the demand to the next state automatically, for example from Draft to Submitted. The state changes only if the conditions for the state change are met. For more information, see [Transition checker to move a demand to the next state automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/playbooks-in-demand-workspace.md).

8.  Repeat the previous steps for each activity and stage until the playbook is complete.

9.  Restart a playbook.

    \[Omitted image "demand-playbook-6.png"\] Alt text: The Playbook actions available for a playbook.

    **Note:** Restarting a playbook results in loss of information for all stages and activities. You have to start with the first stage again.

    1.  Select the Playbook Actions icon.

    2.  Select **Restart Playbook**.

    3.  Select **Restart**.


## Result

The demand moves through its life cycle and is converted to the selected work entity, such as a project.

**Related topics**  


[Running Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-agents-and-fulfillers.md)

[Playbooks reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer-reference.md)

[Playbooks in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/playbooks-in-demand-workspace.md)

[Demand workflow playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/demand-default-playbook-stages.md)

