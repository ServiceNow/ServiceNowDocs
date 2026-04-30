---
title: Validate parts using the Parts Manager AI agent
description: Use the Parts Manager AI agent to track and validate parts usage when closing a work order task through the Now Assist panel.
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

# Validate parts using the Parts Manager AI agent

Use the Parts Manager AI agent to track and validate parts usage when closing a work order task through the Now Assist panel.

## Before you begin

Before validating parts, verify that comments or work notes describing the parts used during the task have been added to the work order task activity stream. The Parts Manager AI agent references these notes to identify and validate parts.

Role required: wm\_agent

## About this task

The Parts Manager AI agent analyzes your work notes to identify which parts were used during a service task. You can use the agent to swap, install, or decline required parts through a conversational AI interaction. After validation, the agent automatically updates inventory and parts statuses.

**Note:** Review the AI-generated parts summary before confirming. AI-generated results may not be accurate in all cases.

## Procedure

1.  Open a work order task and select the Now Assist panel icon ![](../image/now-assist-panel-icon.png).

2.  Ask Now Assist to validate parts for the work order task.

    ![The validate parts conversation in the Now Assist panel.](../image/now-assist-validate-parts.png)

    If the Parts Manager AI agent cannot determine the work order task, provide the work order task number when prompted.

    The Parts Manager AI agent analyzes the work notes and work order task details, then presents a summary of parts used, parts removed, and parts not used.

3.  Review the validated parts summary and confirm the results.

    The parts statuses and inventory are updated based on the validated results.


