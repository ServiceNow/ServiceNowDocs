---
title: Workflow activities reference
description: Workflow activity reference, organized by category.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow activities reference

Workflow activity reference, organized by category.

Each activity performs a different task, such as running a script, sending notifications, or requesting approvals.

Workflow runs activities as the user session that starts or advances them. Workflows started from record operations will run activities as the user session that performed the record operation. Workflows started from schedules or restarted from timers run activities as the System user. Workflows started from script calls run activities as the user session that started the script.

## Approval and rollback activities

Approval and rollback activities generate and manage approvals. Not all workflows can include approval activities. For more information, read [Approval and rollback workflow activities](c_ApprovalAndRollbackActivities.md).

**Note:** Approval activities run as the user whose actions match the approve or reject conditions the workflow was waiting for and advances the workflow.

|Activity|Description|
|--------|-----------|
|[Approval Action workflow activity](../reference/r_ApprovalAction.md)|The **Approval Action** activity performs an approval action on the current task.|
|[Approval Coordinator workflow activity](../reference/r_ApprovalCoordinator.md)|The **Approval Coordinator** activity creates an approval whose outcome depends on the outcome of one or more child activities, including one or more **Approval - User**, **Approval - Group**, and/or **Manual Approval** activities.|
|[Approval - Group workflow activity](../reference/r_ApprovalGroup.md)|The **Approval - Group** activity creates approval records for each member of a specified group.|
|[Approval - User workflow activity](../reference/r_ApprovalUser.md)|The **Approval - User** activity creates one or more individual user approvals.|
|[Generate workflow activity](../reference/r_Generate.md)|The **Generate** activity immediately creates task or approval records from any task or approval activities placed after the **Generate** activity in the workflow path. These pre-generated tasks and approvals start when the task and approval activities are reached during flow execution. This allows a task to have a set of associated pre-generated sequential tasks or approvals, but still require them to be completed in order.|
|[Manual Approvals workflow activity](../reference/r_ManualApprovals.md)|The **Manual Approvals** activity watches and manages any approvals that users add manually outside of the workflow process. This activity only selects approvals that are in the Not requested state.|
|[Rollback To workflow activity](../reference/r_RollbackTo.md#)|The **Rollback To** activity transitions directly to the activity specified by the outgoing transition line arrow.|

## Condition activities

Condition activities provide conditional branching and logical operation functionality for workflows.

**Note:** Condition activities run as the user whose actions match the conditions the workflow was waiting for and advances the workflow.

|Activity|Description|
|--------|-----------|
|[If workflow activity](../reference/r_If.md)|The **If** activity checks a condition or script to determine if a **Yes** or **No** transition should be taken.|
|[Switch workflow activity](../reference/r_Switch.md)|The **Switch** activity checks if the value of a passed field or variable is equivalent to one of several case values.|
|[Wait for condition workflow activity](../reference/r_WaitForCondition.md)|The **Wait for condition** activity causes the workflow to wait at this activity until the current record matches the specified condition.|
|[Wait for WF Event workflow activity](../reference/r_WaitForWFEvent.md)|The **Wait for WF Event** activity causes the workflow to wait at this activity until the specified event is fired.|

## Notify activities

Notify workflow activities manage calls and SMS messages in Notify.

|Activity|Description|
|--------|-----------|
|[Forward call workflow activity](../reference/r_WorkflowActivityForwardCall.md)|The **Forward Call** activity forwards a Notify call to an E.164-compliant phone number.|
|[Input workflow activity](../reference/r_WorkflowActivityGather.md)|The **Input** activity creates a phone menu by presenting a list of options on a Notify call.|
|[Hangup workflow activity](../reference/r_WorkflowActivityHangUp.md)|The **Hangup** activity disconnects an active Notify phone call.|
|[Play workflow activity](../reference/r_WorkflowActivityPlay.md)|The **Play** activity plays a sound file on a Notify call.|
|[Record workflow activity](../reference/r_WorkflowActivityRecord.md)|The **Record** workflow activity records audio from a user on a Notify call.|
|[Reject workflow](../reference/r_WorkflowActivityRejectCall.md)|The **Reject** workflow activity rejects an incoming Notify call.|
|[Say workflow activity](../reference/r_WorkflowActivitySay.md)|The **say** workflow activity allows you to play a message, using text to speech, on a Notify call.|
|[Forward to notify client workflow activity](../reference/r_WflowActivConnNotifClient.md)|The **forward to notify client** workflow activity connects a phone call to a Notify WebRTC client.|
|[Call workflow activity](../reference/r_WorkflowActivityCall.md)|The **Call** activity makes outbound phone calls using a Notify workflow. This workflow activity can be added to any table.|
|[Join conference call workflow activity](../reference/r_WflowActivJoinConfCall.md)|The **Join Conference Call** activity connects an incoming or outgoing call to a Notify conference call.|
|[Send SMS workflow activity](../reference/r_WorkflowActivitySendSMS.md)|The **send SMS** workflow activity to send short text messages using Notify to users' phones. This workflow activity can be added to any table.|
|[Queue workflow activity](../reference/r_WorkflowActivityQueue.md)|The **Queue** activity places an active Notify call in a queue.|

## Notification activities

Notification workflow activities notify users of events that occur during the workflow.

|Activity|Description|
|--------|-----------|
|[Create Event workflow activity](../reference/r_CreateEvent.md)|The **Create Event** activity adds an event to the event queue, but does not immediately fire the event.|
|[Notification workflow activity](../reference/r_NotificationActivity.md)|The **Notification** activity sends an email or SMS message to specified users or groups.|

## Subflow activities

Subflow activities run and manage workflows from a parent workflow.

|Activity|Description|
|--------|-----------|
|[Parallel Flow Launcher workflow activity](../reference/r_ParallelFlowLauncher.md)|The **Parallel Flow Launcher** activity launches multiple subflows in parallel.|

## Task activities

Task activities create and modify workflow tasks.

**Note:** Task activities run as the user whose actions complete the task the workflow was waiting for and advances the workflow.

|Activity|Description|
|--------|-----------|
|[Add Worknote workflow activity](../reference/r_AddWorknote.md)|The **Add Worknote** activity adds text to the Worknotes field of the current incident record.|
|[Attachment Note workflow activity](../reference/r_AttachmentNote.md)|The **Attachment Note** activity adds an attachment to the current record.|
|[Catalog Task workflow activity](../reference/r_CatalogTask.md)|The **Catalog Task** activity creates a service catalog task record.|
|[Create Task workflow activity](../reference/r_CreateTask.md)|The **Create Task** activity generates a record on any of the tables that extend Task \[task\].|

## Timer activities

Timer activities pause workflows for set periods of time.

**Note:** Timer activities run as the System user because the system scheduler advances the workflow.

|Activity|Description|
|--------|-----------|
|[SLA Percentage Timer workflow activity](../reference/r_SLAPercentageTimer.md)|The **SLA Percentage Timer** activity pauses the workflow for a duration equal to a percentage of an SLA.|
|[Timer workflow activity](../reference/r_Timer.md)|The **Timer** activity pauses the workflow for a specified period of time.|

## Utility activities

Utility activities provide controls over the path of the workflow, and other useful tools.

|Activity|Description|
|--------|-----------|
|[Branch workflow activity](../reference/r_BranchActivity.md)|The **Branch** activity splits the workflow into multiple transition paths from a single activity.|
|[Join workflow activity](../reference/r_JoinActivity.md)|The **Join** activity unites multiple execution paths into one transition.|
|[Lock workflow activity](../reference/r_LockActivity.md)|The **Lock** activity prevents other instances of this workflow from continuing past this activity until the lock is released.|
|[Log Message workflow activity](../reference/r_LogMessageActivity.md)|The **Log Message** activity writes a message to the workflow log.|
|[Log Trace Message workflow activity](c_LogTraceMessage.md)|The **Log Trace Message** activity writes a trace message to the workflow log.|
|[REST Message legacy workflow activity](../reference/r_RESTMessageActivity.md)|The legacy **REST Message** activity enables an administrator to override the REST endpoint or supply the variables configured in the REST Message module.|
|[Return Value workflow activity](../reference/r_ReturnValueActivity.md)|The **Return Value** activity returns a value to a parent workflow, when run from a subflow.|
|[Run Script workflow activity](../reference/r_RunScriptActivity.md)|The **Run Script** activity runs the specified script in the scope of the workflow version.|
|[Set Values workflow activity](../reference/r_SetValuesActivity.md)|The **Set Values** activity sets values on the current record when the workflow quiesces or ends.|
|[SOAP Message legacy workflow activity](../reference/r_SOAPMessageActivity_1.md)|The legacy **SOAP Message** activity uses SOAP messages defined in the System Web Services plugin and can call the messages using a MID Server.|
|[Turnstile workflow activity](../reference/r_TurnstileActivity.md)|The **Turnstile** activity limits how many times a workflow can pass through the same point.|
|[Unlock workflow activity](../reference/r_UnlockActivity.md)|The **Unlock** activity releases a lock that was previously placed by the **Lock** activity.|

## Activities provided with Orchestration

The following activities are included with Orchestration.

-   Active Directory activity pack
-   Orchestration activities
-   PowerShell activities
-   Puppet activities

## Templates provided for creating custom activities

If Orchestration is active on your system, users with the proper roles can create custom activities using the ServiceNow Orchestration activity designer. For information about the templates Orchestration provides for creating custom activities that you can upload to the ServiceNow Store, see Orchestration custom activity templates

