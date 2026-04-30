---
title: Escalation triggers and policies
description: Create and edit trigger rules.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [On-Call Scheduling in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Escalation triggers and policies

Create and edit trigger rules.

## About this task

There are two ways to create and edit escalation triggers and policies. Navigate to **Workspaces** &gt; **Service Operation Workspace** and:

-   Schedules menu:
    -   Select the **Schedule** menu, select a shift card and click ![Edit shift](../image/mim-edit-icon.png) icon.
    -   Select **Escalation policies** tab and click **Open Team Record**.
-   Teams menu:
    -   Select the **Teams** menu, select **All Shifts** from the drop-down and select a shift card.
    -   Select **Escalation triggers and policies** tab.

## Before you begin

Role required: rota\_manager, rota\_admin

## Procedure

1.  Under **Escalation policies** in the left panel, select **Create policy**.

2.  On the form, fill in the fields.

    ![Escalation triggers and policies form.](../image/create_policy_teams_menu_sow.png)

    |Field|Description|
    |-----|-----------|
    |Active|Check the box to activate or deactivate the policy.|
    |Create from scratch or Create from template|Create your own policy or use a template created by your admin.|
    |Description|Enter text describing the policy.|
    |Active on shift|Select from the list menu. Set this as the default using the check box.|
    |Order|Select an order of execution. When there are multiple escalation triggers in a team, The one with smaller order number is checked first.|
    |Conditions|Set the conditions for the policy by selecting a table and condition set. These conditions are checked after the escalation is started by an escalation trigger. If the conditions are met, the policy is run.|
    |Escalation steps|Using the modal, add escalation steps. Select **Done** when you are finished.|
    |Escalation notifications|Set the notification conditions for the policy. Toggle user preference override, manual set or use a template.|
    |Add notification step|Select email, call, or SMS. You can add as many attempts as you like. Select **Done** when you are finished.|

3.  To add more escalation levels to the policy, select **Add an escalation level**.

4.  Select **Save changes**.

5.  To add another escalation policy to the team for another category of alert or incident, select **Add a policy**.

6.  To create trigger rules, select **Escalation triggers** in the left panel, select **Create trigger**.

7.  On the form, fill in the fields.

    ![Create trigger form](../image/create_trigger_sow.png)

    |Field|Description|
    |-----|-----------|
    |Escalation trigger name|Enter the name of the trigger.|
    |Active|Check the box to activate or deactivate the trigger.|
    |Order|Select an order of execution. When there are multiple escalation triggers in a team, The one with smaller order number is checked first.|
    |Conditions|Set the conditions for the trigger by selecting a table and condition set. When conditions are met, Escalation triggers are triggered for shifts in SRM team.|

8.  Select **Save changes**.


-   **[Create escalation trigger rules and policy from team record](edit-escalation-trigger-rules-and-policy-from-team-record.md)**  
Navigate to team record to create new policy and trigger rules

**Parent Topic:**[On-Call Scheduling in Service Operations Workspace](on-call-scheduling-in-sow.md)

