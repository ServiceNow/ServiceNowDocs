---
title: Script actions
description: You can use script actions to create server-side scripts that perform a variety of tasks, such as modifying a configuration item \(CI\), or managing failed login attempts. Script actions are triggered by events only.
locale: en-US
release: yokohama
product: System Events
classification: system-events
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [System events reference, System Events, Build workflows]
---

# Script actions

You can use script actions to create server-side scripts that perform a variety of tasks, such as modifying a configuration item \(CI\), or managing failed login attempts. Script actions are triggered by events only.

## Configuration

To create a new script action, navigate to **System Policy** &gt; **Events** &gt; **Script Actions** and click **New**.

<table id="table_xc1_q3p_22c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for your script action.

</td></tr><tr><td>

Application

</td><td>

Application that contains the script.

</td></tr><tr><td>

Event name

</td><td>

Event to use for this script. If you do not find an event for your script action that suits your purpose, you can create a new one.

</td></tr><tr><td>

Active

</td><td>

Check box that enables or disables the script action. Select **true** to enable the script action.

</td></tr><tr><td>

Execution order

</td><td>

Order in which the script will be executed.

</td></tr><tr><td>

Condition script

</td><td>

Statement for a condition under which this script should execute. The system only parses the **script** field if the condition evaluates to true. If you decide to include the condition statement in the script, leave this field blank.

</td></tr><tr><td>

Script

</td><td>

Script that runs when the condition you define evaluates to true. Two additional objects are available in this script:-   event: a [GlideRecord](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)- the sysevent that caused this to be invoked. If you want this first parameter on the event, use **event.parm1** or **event.parm2** for the second parameter. For the date/time of the event, use **event.sys\_created\_on**. To get the user ID that created the event \(if there was a user associated\), use **event.user\_id**.
-   current: a GlideRecord- the event scheduled on behalf of \(incident for example\).

</td></tr></tbody>
</table>Sample of a script action that creates an email notification for Workflow activity:

![Script action workflow notification](../image/ScriptActionWorkflow.png "Script action workflow")

**Parent Topic:**[System events reference](system-events-reference.md)

