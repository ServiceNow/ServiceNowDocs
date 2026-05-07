---
title: Validate parts on ServiceNow Agent using the Parts Manager AI agent
description: Use the Parts Manager AI agent to validate parts usage when closing work order tasks on the ServiceNow Agent mobile application using Now Assist for Field Service Management \(FSM\).
locale: en-US
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Parts Manager, AI agent, validate parts, mobile]
breadcrumb: [Use agentic AI in FSM, Now Assist for FSM]
---

# Validate parts on ServiceNow Agent using the Parts Manager AI agent

Use the Parts Manager AI agent to validate parts usage when closing work order tasks on the ServiceNow Agent mobile application using Now Assist for Field Service Management \(FSM\).

## Before you begin

Add comments or work notes describing the parts used during the task to the work order task activity stream before validating parts. The Parts Manager AI agent references these notes to identify and validate parts.

Role required: wm\_agent

## About this task

The Parts Manager AI agent analyzes your work notes to identify which parts were used during a service task. After validation, the agent automatically updates inventory and parts statuses.

**Note:** This feature uses AI to generate results. AI-generated content may not always be accurate or complete. Review the validated parts summary before confirming the results.

## Procedure

1.  Navigate to **My Work**.

2.  Tap a work order task under **My Tasks**.

3.  Tap **Now Assist** from the navigation bar to open Now Assist Virtual Agent.

4.  Ask Now Assist to validate parts for the work order task.

    The Parts Manager AI agent analyzes your work notes and the work order task details, then presents a summary of validated parts. The summary includes parts used, parts removed, and parts not used.

5.  Review the validated parts summary and select **Yes** or **No** when prompted to mark the validation as done.

6.  Tap **Submit**.

    The parts statuses and inventory are updated based on the validated results.


## What to do next

To verify the updated parts for the task, open the work order task and tap the more options icon next to **Related**, then tap **Parts**.

