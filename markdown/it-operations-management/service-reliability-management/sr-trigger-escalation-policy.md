---
title: Create an escalation trigger for an SRM team
description: To address issues promptly, define the conditions that trigger a team's escalation policy in Service Reliability Management \(SRM\).
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up escalation policies for your team in SRM, Working with SRM teams, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Create an escalation trigger for an SRM team

To address issues promptly, define the conditions that trigger a team's escalation policy in Service Reliability Management \(SRM\).

## Before you begin

If your team needs trigger fields other than Assignment group, confirm that an admin has already configured them. For more information, see [Configure fields for escalation triggers](srm-configure-trigger-fields.md).

Role required: srm\_manager or srm\_admin

## About this task

This procedure shows how to create escalation triggers in SRM. If your organization manages on-call scheduling using IT Service Management \(ITSM\), you can also use ITSM On-Call Scheduling to define escalation triggers. See [Create an escalation trigger rule](https://www.servicenow.com/docs/access?context=create-trigger-rule-oncall&version=australia&pubname=australia-it-service-management&ft:locale=en-US) for more information. While that procedure lists ITSM roles, SRM users only need the srm\_manager or srm\_admin role.

For a broader overview of escalation processes in ITSM, see [Designing an escalation process](https://www.servicenow.com/docs/access?context=designing-escalation-process-oncall&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the primary navigation, select **Teams** \(![Teams.](../image/icon-sr-teams.png)\).

3.  Select your team, and then select the **Escalation triggers and policies** tab.

4.  In the **Escalation triggers** panel, select **Create trigger**, and fill in the Escalation trigger form.

<table id="table_escalation_trigger"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Escalation trigger name

</td><td>

Name of the trigger. Example: `P1 incidents`.

</td></tr><tr><td>

Order

</td><td>

Order of execution for the trigger.When a team has multiple escalation triggers, the triggers with lower values are evaluated first.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the trigger.

</td></tr><tr><td>

Conditions

</td><td>

Choose the table \(**Alert** or **Incident**\) and set the conditions for the trigger. When conditions are met, the system triggers an escalation for the relevant team.Example: `Priority is 1 - Critical`.

</td></tr><tr><td>

Advanced options

</td><td>

Define what happens when the trigger conditions are met and when the trigger runs.For **Trigger action**, select **Workflow**, **Subflow** or **Script**, then choose the specific item. Example: Select **Workflow**, and **On-Call: Assign by Acknowledgment** to auto-assign the incident to the person who acknowledges it.

Select **Run trigger rule every time the selected field changes** to run the trigger when one of the chosen fields updates. If not selected, the trigger runs only when the Assignment group changes.

</td></tr></tbody>
</table>5.  Select **Save**.

    The UI displays `The Escalation trigger has been added successfully`. The trigger is now active and runs when the defined conditions are met.


**Parent Topic:**[Set up escalation policies for your team in SRM](sr-create-escalation-policies.md)

