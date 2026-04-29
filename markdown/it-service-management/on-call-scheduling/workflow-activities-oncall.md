---
title: Workflow Activities for On-Call Scheduling
description: Workflow activities in On-Call Scheduling workflows.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [On-Call Scheduling workflows, Reference for on-call scheduling, On-Call Scheduling, IT Service Management]
---

# Workflow Activities for On-Call Scheduling

Workflow activities in On-Call Scheduling workflows.

## Escalation workflow activities

-   **On-Call: Log Escalation Start**

    Creates an escalation record based on group, task, and workflow details.

    **Note:**

    The escalation that the workflow creates the `workflow.scratchpad.escalationSysId` sys\_id. Use the sys\_id in any of the other workflow activities.

    |Setting|Description|
    |-------|-----------|
    |Group|sys\_id of the group that the escalation belongs to.|
    |Table|Table name of the task record of the incident.|
    |Source|sys\_id of the task record on which the escalation happened.|
    |WorkflowDefinition|sys\_id of the workflow definition that is used to escalate.|
    |WorkflowContext|sys\_id of the workflow context.|
    |ParentEscalationLevelId|sys\_id of the parent escalation in the case that the escalation was triggered from another escalation.|
    |Category|Category of the escalation. One of: \[assign\_by\_acknowledgement, auto\_assignment, notify\_manual\_assignmen,conferencing\].|
    |Channels|Comma-separated list of the channels used to communicate during the escalation. Any or all of: \[email, sms, voice, slack\]. For example, sms,email,voice|
    |IgnoreDefReminders|If true, the workflow sends notification reminders as specified by the workflow, rather than as specified in On-Call Escalation settings. For example, in Conference On-Call escalations, the workflow might to dial the on-call members at one-minute intervals instead of the standard 15-minute intervals.|

-   **On-Call: Log Escalation Level**

    Creates an escalation level record given escalation and level details.

    |Setting|Description|
    |-------|-----------|
    |EscalationId|sys\_id of the escalation to which the level belongs.|
    |RotaId|sys\_id of the shift for which the escalation is happening.|
    |Level|Current escalation level. For example, 2.|
    |Escalatee|Escalatee object at current escalation level. For example, getEscalationPlan\(\)\[1\].|
    |CatchAll|True if the escalation level belongs to a catch-all.|

-   **On-Call: Log Escalation Attempt**

    Creates a Contact attempt record given an escalation, level, and attempt details.

    |Setting|Description|
    |-------|-----------|
    |EscalationId|sys\_id of the escalation to which the contact attempt belongs.|
    |RotaId|sys\_id of the shift for which the escalation is happening.|
    |Level|Current escalation level. For example, 2.|
    |ContactAttempt|Contact attempt number within the escalation level. For example, 1.|
    | | |

-   **On-Call: Log Escalation Communication**

    Creates a communication record given escalation, level, attempt, and communication details.

    |Setting|Description|
    |-------|-----------|
    |EscalationId|sys\_id of the escalation to which the communication belongs.|
    |RotaId|sys\_id of the shift for which escalation is happening.|
    |Level|Current escalation level. For example, 2.|
    |ContactAttempt|Contact attempt number within the escalation level. For example, 1.|
    |EscalateeType|Type of escalatee to whom the communication is sent. One of: \[user,device\]|
    |EscalateeId|sys\_id of the user or device, depending on escalatee type.|
    |CommType|Type of communication. One of: \[sms, voice, email, slack\]|
    |CommValue|Phone number or email address, depending on communication type. For example, `abel.tuter@servicenow.com`|
    |Status|Status of the communication. One of: \[sent, failed\].|
    |Escalatee|Escalatee object at current escalation level. For example, getEscalationPlan\(\)\[1\].|
    |CatchAll|True if the escalation level belongs to a catch-all.|

-   **On-Call: Log Escalation End**

    Completes the escalation by setting active flag to false.

    |Setting|Description|
    |-------|-----------|
    |EscalationId|sys\_id of the escalation.|

-   **On-Call: Send Notification**

    Sends notification to the current escalatee via voice, SMS, Slack, Microsoft Teams, or mobile push.

<table id="table_knb_ngv_mlb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notification type

</td><td>

Type of notification. One of: \[sms, voice, slack\].

</td></tr><tr><td>

Message

</td><td>

Text of message to send to current escalatee if notification type is sms.

</td></tr><tr><td>

Notification detail

</td><td>

List of parameters that are required for a notification:-   SMS: notify\_number, users, groups, numbers
-   Voice: numberToCallFrom, numberToCall, user
-   Slack: slack user, taskId, catchAllOption, wFContextId
-   Microsoft Teams: user, taskId, catchAllOption, wFContextId
-   Mobile push: userSysId, tablename, recordSysId


</td></tr></tbody>
</table>-   **On-Call: Manage Escalation Response**

    Manage an escalation response record \(insert escalation record, clean escalation records, update response to an escalation\). An escalation response record keeps track of a response received for an escalation through the SMS, voice, email, or Slack notification channels. An escalation response record is used to resume the **On-Call: Assign by Acknowledgement** workflow upon rejection of an escalation.

    |Setting|Description|
    |-------|-----------|
    |Workflow Context|Workflow context ID.|
    |Escalatee Id|UserID of the current escalatee.|
    |Table Name|Table name of the task record. For example, `incident`.|
    |Current Record Id|sys\_id of the task record.|
    |Action Type|Type of action. One of: \[add,clean,update\]|
    |Response|Response by escalatee to an escalation. One of: \[accepted,rejected\]|

    Example uses:

    -   Insert \(add\) - Workflow Context, Escalatee ID, Table Name, Current Record ID
    -   Clean - Workflow Context
    -   Update - Escalatee ID, Table Name, Current Record ID, Response

**Parent Topic:**[On-Call Scheduling workflows](workflows-oncall.md)

