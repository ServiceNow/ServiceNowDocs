---
title: Activity executions
description: Activity execution records provide runtime information about activities in a playbook, such as the activity's current state and associated record.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Activity executions

Activity execution records provide runtime information about activities in a playbook, such as the activity's current state and associated record.

An activity execution represents a runtime execution of your activity. Each time one of your playbooks triggers, records are automatically created for each activity that runs within the triggered playbook.

To access the activity execution records for an In Progress playbook execution, navigate to **Process Automation** &gt; **Process Automation Administration** &gt; **Active Processes**. Alternatively, you can see the activity executions for all playbooks that ran today by navigating to **Process Automation** &gt; **Process Automation Administration** &gt; **Today's Executions**. Select a playbook execution record from the list. Then, you can view the associated activity execution records in the Activity Executions related list.

## Fields

By default, each record in the Activity Executions related list contains the following fields:

|Field|Description|
|-----|-----------|
|Label|Name of the activity|
|Stage|Stage in which the activity runs|
|State|Execution status for the activity. See [Activity execution states](activity-executions.md).|
|Activity Type|Experience type for the activity. See [Experience types](experience-types.md).|
|Associated Record|Record whose data renders within the playbook card.|
|Execution index|Sequential order in which the activity runs, starting with 1 \(one\).|

## Activity execution states

Activity execution states indicate the status of an activity in a triggered playbook. Activities that render in a playbook card can display this state to agents. An activity execution record can have one of the following states:

|State|Description|
|-----|-----------|
|Pending|The playbook triggered, but the activity execution is waiting on preceding activities to complete before it can start running.|
|Ready|The playbook triggered, and the activity will start running soon.|
|In Progress|The playbook triggered, and the activity execution is running.|
|Complete|The playbook triggered, and the activity execution is done running.|
|Skipped|The playbook triggered, but a user chose to skip this activity execution and move on to the next activity. Also, if the activity contains a condition that evaluates to false, the system skips the activity.|
|Error|The playbook triggered, but an error with the activity's automation plan or activity experience occurred. Errors can occur when the underlying action or subflow in the activity's automation plan fails to run.|
|Cancelled|A user with the admin, flow\_designer, or action\_designer role explicitly canceled the underlying action or subflow in the activity's automation plan.|

**Parent Topic:**[Playbooks reference](../reference/process-automation-designer-reference.md)

