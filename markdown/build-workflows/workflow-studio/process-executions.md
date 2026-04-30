---
title: Process executions
description: A process execution is a single, runtime instance of a playbook. Process execution records provide runtime information about playbooks, such as the current state and input record.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Process executions

A process execution is a single, runtime instance of a playbook. Process execution records provide runtime information about playbooks, such as the current state and input record.

A process execution represents a runtime execution of your playbook. Each time a playbook is triggered, a record is automatically in the Process Executions \[sys\_pd\_context\] table.

To access the records for an In Progress process execution, navigate to **Process Automation** &gt; **Process Automation Administration** &gt; **Active Processes**. Alternatively, you can see the process executions for all playbooks that ran today by navigating to **Process Automation** &gt; **Process Automation Administration** &gt; **Today's Executions**.

## Fields

By default, each process execution record contains the following information:

|Field|Description|
|-----|-----------|
|Name|Name of the playbook that triggered this process execution|
|Created|Date and time when the playbook triggered|
|Input Record|Table name and record number that triggered this process execution|
|State|Current status of the overall process execution. For more information, see [Process execution states](process-executions.md#process-execution-states).|

## Process execution states

A process execution record can have one of the following states:

|State|Description|
|-----|-----------|
|Queued|The playbook triggered, but the system hasn't started running the process execution yet.|
|In Progress|The playbook triggered, and the process execution is currently running. One or more activities in the playbook have a state of Ready or In Progress.|
|Complete|The playbook triggered, and the process execution is done running. All activities in the playbook have a state of Skipped or Complete.|
|Error|The playbook triggered, but an activity has an Error state. Errors can occur when the action, subflow, or flow specified in the activity definition's automation plan fails to run.|
|Cancelled|A user with the admin or playbook.admin role explicitly canceled the process execution, and the execution has stopped running.|

**Parent Topic:**[Playbooks reference](../reference/process-automation-designer-reference.md)

