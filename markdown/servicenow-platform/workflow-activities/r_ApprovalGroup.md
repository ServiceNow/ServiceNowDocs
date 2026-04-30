---
title: Approval - Group workflow activity
description: The Approval - Group activity creates approval records for each member of a specified group.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Approval and rollback workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Approval - Group workflow activity

The **Approval - Group** activity creates approval records for each member of a specified group.

**Note:** This activity is only available when the workflow runs on a table that extends Task.

The group approval is approved or rejected based on the user approvals, according to the logic specified in the **Wait For** field.

## Results

The workflow designer can assign a result value using activity.result from within a script field of the activity. By default, the result value is the final approval disposition. This disposition depends on the approval actions take by the approvers and the approval conditions specified in the **Wait for** or **When Anyone Rejects** fields. Possible result values are:

-   Approved
-   Rejected
-   Deleted
-   Cancelled

## Input variables

Input variables determine the initial behavior of the activity.

<table id="table_xql_rnw_w4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="subhead" colspan="2">

Approval - Group When Specify when this activity generates a group approval record.

</td></tr><tr><td>

Condition

</td><td>

Conditions which, if met, cause the group approval to be generated. If the conditions are not met, the approval is skipped.

</td></tr><tr><td class="subhead" colspan="2">

Approval - Group Approvers Specify the groups whose approval will be requested.

</td></tr><tr><td>

Groups

</td><td>

The groups whose approval will be requested.To edit this field, click the lock icon. To select specific groups by name, use the lookup list. To select groups from field values on the current record at runtime, click the tree icon.

 Each member of the group will be assigned an individual approval record.

 If no group is selected, the activity automatically sets the approval to **Approved**.

</td></tr><tr><td class="subhead" colspan="2">

Approval - Group Condition Specify how the activity decides to approve or reject the group approval, based on the responses from individual members of the group.

</td></tr><tr><td>

Wait for

</td><td>

A choice between different approval logics to determine which individual approvals or rejections result in approval or rejection of the activity's approval. Options are:

-   **An approval from each group:** Any user from each group can approve and the first approval from each group causes the activity to complete with a result of **approved** \(see below for how a rejection is handled\).
-   **An approval from any group:** Any user from any group can approve and the first approval from any group causes the activity to complete with a result of **approved**.
-   **An approval from everyone from all groups:** All users from all groups must approve to cause the activity to complete with a result of **approved** \(see below for how a rejection is handled\).
-   **First response from each group:** The first approval or rejection from any user in each group is used to indicate the state of the group approval \(see below for how a rejection is handled\).

Indicate what happens when any user rejects their approval request. Options are:

-   **Reject the approval:** Immediately complete the activity with a result of **rejected**.
-   **First response from any group:** The first approval or rejection from any user in any group causes the activity to complete with a result of **approved** or **rejected**.
-   **Condition based on script:** Each time a user approves or rejects, the **Approval script** is called to determine if the activity should complete.

</td></tr><tr><td>

Approval scriptOnly appears when **Wait for** is set to `Condition based on script`.

</td><td>

If the **Wait for** variable is set to **Condition based on script** this script is called to determine how to handle an approval or rejection. The script needs to set the variable *answer* to approved or rejected to indicate the overall status for this approval.

 This script is responsible for setting the approval state for each group that is part of this approval activity before returning the overall approval state for all of the groups.

 When called, the following variables are available to the script for all the groups that are part of this approval activity:

 ```
counts.total = total number of groups that are part of this approval
                  counts.approved = # of groups that approved so far
                  counts.rejected = # of groups that rejected so far
                  counts.requested = # of groups that are pending approval
                  counts.not_requested = # of groups that are not pending approval
                  counts.not_required = # of groups that approval is not required
```

 And for each group:

```
groups[group_id].total = total number of users that are part of this group's approval
                    groups[group_id].approved = # of users that approved so far
                    groups[group_id].rejected = # of users that rejected so far
                    groups[group_id].requested = # of users that are pending approval
                    groups[group_id].not_requested = # of users that are not pending approval
                    groups[group_id].not_required = # of users that approval is not required
                    groups[group_id].approvalIDs[state] = array of user ids that are at the specified approval state
```

 Note: Iterate the groups using:

```
for (var id in groups) {
                    var group = groups[id];
                    ... group.total ...
                    }
```

 Note: Get group object using the following code \(to get things like the group name being iterated on\):

```
var objGroup = fncGetGroupObj(id);
                    var strGroupName = objGroup.name;
                    
                    function fncGetGroupObj(sidGroupApproval)
                    {
                    var objGroupApproval = new GlideRecord('sysapproval_group');
                    objGroupApproval.get(sidGroupApproval);
                    
                    var objGroup = new GlideRecord('sys_user_group');
                    objGroup.get(objGroupApproval.assignment_group.sys_id);
                    
                    return objGroup;
                    }
```

 Approval scripts also allow computations. For example, if only half of the approvals are required:

```
if (counts.approved/counts.total > .49) {
                    answer = 'approved';
                    }
                    else if (counts.rejected/counts.total > .50) {
                    answer = 'rejected';
                    }
```

</td></tr><tr><td>

When anyone rejects

</td><td>

A choice between different approval logics to determine which individual rejections result in rejection of the activity's approval. Options are:

-   **Reject the approval:** Immediately complete the activity with a result of **rejected**.
-   **Wait for other responses before deciding:** Wait until we get other responses before making an approval or rejection decision. This allows users to change their mind until a decision is made.

**Note:** If **Wait for** is set to **Anyone to approve**, then a single approval causes the activity to complete with a result of **approved**, even if one or more users reject.

</td></tr><tr><td class="subhead" colspan="2">

Approval - Group Schedule Specify how workflow calculates the approval record's expected start date and due date. Once you've made a selection for 'Due date based on', and 'Schedule based on', the appropriate fields will display.

</td></tr><tr><td>

Due date based on

</td><td>

Select how workflow determines the task's duration, due date, and schedule. -   **A user specified duration:** The duration is based on a user specified value.
-   **A relative duration:** The duration is calculated from a relative duration \(such as End of Next Business Day\).
-   **A date/time or duration field:** The duration is based on the value of a field on the current record.
-   **Script:** The duration is returned by a script.

</td></tr><tr><td>

Duration Only appears when **Due date based on** is set to `A user specified duration`

</td><td>

The specific number of days and hours.

</td></tr><tr><td>

Relative durationOnly appears when **Due date based on** is set to `A relative duration`

</td><td>

The general number and length of business days.

</td></tr><tr><td>

Due date fieldOnly appears when **Due date based on** is set to `A date/time or duration field`

</td><td>

The date/time or duration field.

</td></tr><tr><td>

Due date scriptOnly appears when **Due date based on** is set to `Script`

</td><td>

The script that sets 'answer' to the number of seconds for the duration.

</td></tr><tr><td>

Schedule based on

</td><td>

The basic schedule the timer uses to count working hours. If a schedule is specified, the duration will only be considered for times that are specified on the schedule. For example, if the duration is 2 hours and the workflow begins at 4:00pm on a schedule that is 8am - 5pm, then it ends at 9:00am the next day. The options are: -   **This workflow's schedule:** The schedule uses workflow context date, time, and an optional **Time zone based on** value.
-   **A specific schedule:** The schedule uses a pre-defined **Schedule** and an optional **Time zone based on** value.
-   **A schedule field:** The schedule uses a value from a table and an optional **Time zone based on** value.

</td></tr><tr><td>

ScheduleOnly appears when **Schedule based on** is set to `A specific schedule`

</td><td>

The predefined **Schedule** from a list.

</td></tr><tr><td>

Schedule fieldOnly appears when **Schedule based on** is set to `A schedule field`.

</td><td>

A date and time or duration field for the schedule, that is associated with the table. Valid fields appear in blue on the Select the element from a tree dialog.

</td></tr><tr><td>

Time zone based on

</td><td>

The time zone for calculating the duration. The time zone may be based on:-   **No time zone:** Default. Workflow uses the GMT time zone.
-   **A specific time zone:** A specific **Time zone** that you choose from a choice list.
-   **A time zone field:** A **Time zone field** to track time duration from a field on the form.

</td></tr><tr><td>

Time zoneOnly appears when **Time zone based on** is set to `A specific time zone`

.

</td><td>

Select the time zone you want from the choice list.

</td></tr><tr><td>

Time zone fieldOnly appears when **Time zone based on** is set to `A time zone field.`

</td><td>

A date and time or duration field for the schedule, that is associated with the table. Valid fields appear in blue on the Select the element from a tree dialog.

</td></tr><tr><td class="subhead" colspan="2">

Approval - Advanced If desired, write a script for determining additional users to request approvals from.

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to write a script for determining additional users to request approvals from. Use the **Additional groups script** to customize group approvals.

</td></tr><tr><td>

Additional groups script

</td><td>

If the **Advanced** check box is selected, this script is called to determine any additional group approvals to be created. The script needs to set the variable *answer* to a comma-separated list of group ids or an array of group ids to add as approver groups. For example:

```
answer = [];
       answer.push('id1');
       answer.push('id2');
```

</td></tr></tbody>
</table>## Conditions

The following conditions determine which transition runs after this activity.

**Note:** Approval activities run as the user whose actions match the approve or reject conditions the workflow was waiting for and advances the workflow.

|Condition|Description|
|---------|-----------|
|Approved|The users from the groups have approved the request based on the **Wait for** rules.|
|Rejected|The users from the groups have rejected the request based on the **Wait for** rules.|
|Error|The event or condition that generates an error.|
|Skipped|The event or condition that allows a skipped approval.|

## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine starts the execute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

**Parent Topic:**[Approval and rollback workflow activities](../concept/c_ApprovalAndRollbackActivities.md)

