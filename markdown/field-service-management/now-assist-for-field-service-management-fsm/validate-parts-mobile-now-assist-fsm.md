---
title: Validate parts on ServiceNow Agent using the Parts Manager AI agent
description: Use the Parts Manager AI agent to track and validate parts usage when closing a work order task on the ServiceNow Agent mobile application.
locale: en-US
release: zurich
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-02-23"
reading_time_minutes: 1
keywords: [Parts Manager, validate parts, AI agent, generative AI for Field Service Management]
breadcrumb: [Use agentic AI in FSM, Now Assist for FSM]
---

# Validate parts on ServiceNow Agent using the Parts Manager AI agent

Use the Parts Manager AI agent to track and validate parts usage when closing a work order task on the ServiceNow Agent mobile application.

## Before you begin

Before validating parts, verify that comments or work notes describing the parts used during the task have been added to the work order task activity stream. The Parts Manager AI agent references these notes to identify and validate parts.

Role required: wm\_agent

## About this task

The Parts Manager AI agent analyzes your work notes to identify which parts were used during a service task. You can use the agent to swap, install, or decline required parts through a conversational AI interaction. After validation, the agent automatically updates inventory and parts statuses.

**Note:** Review the AI-generated parts summary before confirming. AI-generated results may not be accurate in all cases.

## Procedure

1.  Navigate to **My Work**.

2.  Tap a work order task under **My Tasks**.

3.  Tap the Now Assist icon ![](../image/now-assist-panel-icon.png) in the navigation bar to open Now Assist Virtual Agent.

4.  Ask Now Assist to validate parts for the work order task.

    ![The validate parts conversation in Now Assist Virtual Agent on the mobile app.](../image/now-assist-mobile-validate-parts.png)

    If the Parts Manager AI agent cannot determine the work order task, provide the work order task number when prompted.

    The Parts Manager AI agent analyzes the work notes and work order task details, then presents a summary of parts used, parts removed, and parts not used.

5.  Review the validated parts summary and confirm the results.

    The parts statuses and inventory are updated based on the validated results.


## What to do next

To verify the updated parts for the task, open the work order task and tap the more options icon next to **Related**, then tap **Parts**.

