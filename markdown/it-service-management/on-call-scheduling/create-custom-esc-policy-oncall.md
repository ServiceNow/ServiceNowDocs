---
title: Create an escalation policy
description: An escalation policy includes the policy type that defines the order in which rosters and roster members receive escalation notifications. You can create a custom escalation policy for a shift by overriding settings in a default escalation type, for example, by configuring custom delays between escalation steps.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Designing an escalation process, Escalations in On-Call Scheduling, Defining On-Call Scheduling escalation process, On-Call Scheduling, IT Service Management]
---

# Create an escalation policy

An escalation policy includes the policy type that defines the order in which rosters and roster members receive escalation notifications. You can create a custom escalation policy for a shift by overriding settings in a default escalation type, for example, by configuring custom delays between escalation steps.

## Before you begin

Role required: rota\_admin, rota\_manager, or admin

## About this task

Users with rota\_manager role can edit policies only for their groups. Users with rota\_admin and admin role can edit policies for all the groups.

The escalation type determines the order in which members of a user group are notified about the escalation. The escalation type depends on the number of rosters.

-   If a shift has only one roster, the escalation type is automatically set to **Rotate through members** and the escalation path goes through the member list of a roster \(primary, secondary, tertiary\) to determine whom to notify.
-   If the shift has multiple rosters, the escalation type is automatically set to **Rotate through rosters** and the escalation path goes through all rosters to determine whom to notify.
-   If the shift has a customized escalation hierarchy, the escalation type is set to **Custom** and the escalation path goes through members as defined in the escalation hierarchy. See [Create an escalation policy](create-custom-esc-policy-oncall.md) for details.

On-Call Scheduling supports multiple escalation policies per shift; for example, policies based on the priority of the incident or type of task record.

## Procedure

1.  Create a custom escalation policy using the escalation designer.

<table id="choicetable_xjj_bsh_cgb"><tbody><tr><td id="d142494e93">

**Access the designer from the On-Call Schedules module**

</td><td>

1.  Navigate to **On-Call Scheduling** &gt; **On-Call Schedules**.
2.  Click the required shift card.
3.  In the **Shifts** tab, click the actions icon for the shift.
4.  Click **Override escalation** and click **OK** in the confirmation window.


</td></tr><tr><td id="d142494e135">

**Access the designer from the My Group Schedules module**

</td><td>

1.  Navigate to **On-Call Scheduling** &gt; **My Group Schedules**.
2.  Open the required shift.
3.  Click **Override Escalation Policy** and then click **Yes** in the confirmation dialog box.


</td></tr></tbody>
</table>2.  Click the Add Escalation Step icon and then fill in the Add Escalation Step form.

<table id="table_xrx_th1_cgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the escalation step.

</td></tr><tr><td>

Escalation level

</td><td>

Hierarchy level of the step.

</td></tr><tr><td>

Time to next step

</td><td>

Wait time from the last reminder to run the next step.

</td></tr><tr><td>

Escalation set

</td><td>

Escalation set for the step.

</td></tr><tr><td>

Number of reminders

</td><td>

Number of reminders to send in this step.

</td></tr><tr><td>

Time between reminders

</td><td>

Time between each reminder of this step.

</td></tr><tr><td class="sub-head" colspan="2">

Escalation audience

</td></tr><tr><td>

Roster

</td><td>

Rosters to which escalation notifications and reminders are sent.

</td></tr><tr><td>

Groups

</td><td>

User groups to which escalation notifications and reminders are sent.

</td></tr><tr><td>

Users

</td><td>

Users to whom escalation notifications and reminders are sent.

</td></tr><tr><td>

Devices

</td><td>

Devices to which escalation notifications and reminders are sent. For example, a mobile phone that is rotated between group members.

</td></tr><tr><td>

Group manager

</td><td>

Option to send escalation notifications and reminders to the group manager.

</td></tr><tr><td>

Group manager field

</td><td>

Option to select group managers hierarchically to send escalation notifications and reminders.This field is available only when the **Group manager** check box is selected.

</td></tr></tbody>
</table>    | | |
    |---|---|
    |Name|Name the escalation policy.|
    |Shift|The shift to which the escalation policy applies.|
    |Default|Select the check box to mark the escalation policy as default. The default escalation policy is used for all on-call escalations in the case that none of the specified **Conditions** are met.|
    |Table|Choose the table for which you want to set the escalation policy.|
    |Condition|Use the condition section to add filters to the escalation criteria.|
    |Description|Short description of the escalation policy.|
    |Active|Select the check box to enable the escalation policy.|
    |Override user preference|Select the check box to override the user's contact preferences.|
    |Order|When there are multiple escalation policies defined for a shift, the order in which to apply this policy. Smaller numbers first.|

3.  To edit an escalation step, click the edit escalation step icon and perform the edits.

4.  Add multiple escalation steps if required.

5.  To edit the escalation hierarchy for the shift, click the actions icon and click **Edit escalation**.

6.  To reset to the default escalation type for the shift, click the actions icon and click **Reset escalation**.


**Parent Topic:**[Designing an escalation process](../concept/designing-escalation-process-oncall.md)

