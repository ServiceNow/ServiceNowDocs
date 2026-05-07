---
title: Validate parts using the Parts Manager AI agent
description: Use the Parts Manager AI agent to validate parts usage when closing work order tasks in Now Assist for Field Service Management \(FSM\).
locale: en-US
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Parts Manager, AI agent, validate parts]
breadcrumb: [Use agentic AI in FSM, Now Assist for FSM]
---

# Validate parts using the Parts Manager AI agent

Use the Parts Manager AI agent to validate parts usage when closing work order tasks in Now Assist for Field Service Management \(FSM\).

## Before you begin

Add comments or work notes describing the parts used during the task to the work order task activity stream before validating parts. The Parts Manager AI agent references these notes to identify and validate parts.

Role required: wm\_agent

## About this task

The Parts Manager AI agent analyzes your work notes to identify which parts were used during a service task. After validation, the agent automatically updates inventory and parts statuses.

**Note:** This feature uses AI to generate results. AI-generated content may not always be accurate or complete. Review the validated parts summary before confirming the results.

## Procedure

1.  Open a work order task and select the Now Assist panel icon ![](../image/now-assist-panel-icon.png).

2.  Ask Now Assist to validate parts for the work order task.

    If the Parts Manager AI agent cannot determine the work order task, provide the work order task number when prompted.

    The Parts Manager AI agent analyzes the work notes and work order task details, then presents a summary of parts used, parts removed, and parts not used.

3.  Review the validated parts summary and confirm the results.

    The parts statuses and inventory are updated based on the validated results.


