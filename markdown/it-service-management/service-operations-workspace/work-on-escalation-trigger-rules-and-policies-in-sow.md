---
title: Escalation triggers and policies
description: Configure the user, notification and on-call escalation preferences by creating escalation trigger rules and policies.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring On-Call Scheduling in Service Operations Workspace, On-Call Scheduling in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Escalation triggers and policies

Configure the user, notification and on-call escalation preferences by creating escalation trigger rules and policies.

## About this task

## Before you begin

Role required: rota\_manager, rota\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operation Workspace** and use any of the following options.

    -   Schedules menu:
        -   Select the **Schedule** menu, select a shift card and click ![Edit shift](../image/mim-edit-icon.png) icon.
        -   Select **Escalation policies** tab and click **Open Team Record**.
    -   Teams menu:
        -   Select the **Teams** menu, select **All Shifts** from the drop-down and select a shift card.
        -   Select **Escalation triggers and policies** tab.
2.  Under **Escalation policies** in the left panel, select **Create policy**.

3.  On the form, fill in the fields.

    ![Escalation triggers and policies form.](../image/create_policy_teams_menu_sow.png)

    |Field|Description|
    |-----|-----------|
    |Active|Option to activate or deactivate the policy.|
    |Create from scratch or Create from template|Option to create your own policy or use a template created by your admin.|
    |Description|Text that describes the policy.|
    |Active on shift|Shift on which the escalation policy is applicable. Select from the list menu. Set this as the default using the check box.|
    |Use as default|Option to set the shift as default for the escalation policy.|
    |Order|Order in which the escalation policy is executed. When there are multiple escalation triggers in a team, The one with smaller order number is checked first.|
    |Conditions|Conditions for the policy. You select a table and condition set. These conditions are checked after the escalation is started by an escalation trigger. If the conditions are met, the policy is run.|
    |Escalation steps|Escalation steps that you can add using the modal. Select **Done** when you are finished.|
    |Escalation notifications|Set the notification conditions for the policy. Toggle user preference override, manual set or use a template.|
    |Add notification step|Notification step such as email, call, or SMS that you can add. You can add as many attempts as you like. Select **Done** when you are finished.|

4.  To add more escalation levels to the policy, select **Add an escalation level**.

5.  Select **Save changes**.

6.  To add another escalation policy to the team for another category of alert or incident, select **Add a policy**.

7.  To create trigger rules, select **Escalation triggers** in the left panel, select **Create trigger**.

8.  On the form, fill in the fields.

    ![Create trigger form](../image/create_trigger_sow.png)

<table id="table_escalation_trigger"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Escalation trigger name

</td><td>

Name of the trigger.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the trigger.

</td></tr><tr><td>

Order

</td><td>

Order in which the trigger rule is executed. When there are multiple escalation triggers in a team, The one with smaller order number is checked first.

</td></tr><tr><td>

Conditions

</td><td>

Set the conditions for the trigger by selecting a table and condition set. When conditions are met, escalation triggers are triggered for shifts in SRM team.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced options

</td></tr><tr><td>

Trigger action

</td><td>

Action that is triggered when the **Match conditions** and **Conditions** are met. Possible values:-   Subflow
-   Workflow
-   Script \(server-side JavaScript\)


</td></tr><tr><td>

Trigger workflow

</td><td>

Workflow to run. Available only if **Trigger action** is set to **Workflow**.

</td></tr><tr><td>

Trigger subflow

</td><td>

Subflow to run. Available only if **Trigger action** is set to **Subflow**.**Note:** The following subflows under the On-Call Escalation Triggers category can be configured using the trigger rules:

-   On-Call: Assign
-   On-Call: Assign and Notify
-   On-Call: Assign By Acknowledgement
-   On-Call: Escalations by Email


</td></tr><tr><td>

Trigger script

</td><td>

Script \(server-side JavaScript\) to run. Available only if the **Trigger action** field is set to **Script**.**Note:** This action is available only for users with the rota\_admin and admin roles.

</td></tr><tr><td>

Run trigger rule every time the selected field changes

</td><td>

Option to re-run the trigger rule when the field value of the specified **Trigger fields** is changed.

</td></tr><tr><td>

Trigger fields

</td><td>

List of fields for a specific table which when changed causes the trigger rule to re-run. For example, with table as incident, you can select fields such as assignment group, priority and state.**Note:**

-   This field is visible only if the **Run Trigger** field is set to **Every time trigger field changes**.
-   You can use the Trigger Rule Table Configs table to configure which fields to be displayed for a specific table. You can access the table from the SOW Admin Center. For more information, see [Manage configurations in Service Operations Workspace for ITSM](../task/manage-admin-console-sow-itsm.md) and [Configure a table for escalation trigger rules](../../../administer/on-call-scheduling/task/configure-tables-for-escalation-trigger-rule.md).


</td></tr></tbody>
</table>9.  Select **Save changes**.


-   **[Create escalation trigger rules and policy from team record](edit-escalation-trigger-rules-and-policy-from-team-record.md)**  
Navigate to team record to create new policy and trigger rules

**Parent Topic:**[Configuring On-Call Scheduling in Service Operations Workspace](configuring-oncall-scheduling-sow.md)

