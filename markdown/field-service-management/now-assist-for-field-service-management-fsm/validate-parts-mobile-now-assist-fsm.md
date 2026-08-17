---
title: Validate parts on ServiceNow Agent using the Parts Manager AI agent
description: Use the Parts Manager AI agent to validate parts usage when closing work order tasks on the ServiceNow Agent mobile application using ServiceNow Otto for Field Service Management \(FSM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/validate-parts-mobile-now-assist-fsm.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Parts Manager, AI agent, validate parts, mobile]
breadcrumb: [Use agentic AI in FSM, ServiceNow Otto for FSM]
---

# Validate parts on ServiceNow Agent using the Parts Manager AI agent

Use the Parts Manager AI agent to validate parts usage when closing work order tasks on the ServiceNow Agent mobile application using ServiceNow Otto for Field Service Management \(FSM\).

## Before you begin

Add comments or work notes describing the parts used during the task to the work order task activity stream before validating parts. The Parts Manager AI agent references these notes to identify and validate parts.

Role required: wm\_agent

## About this task

The Parts Manager AI agent analyzes your work notes to identify which parts were used during a service task. After validation, the agent automatically updates inventory and parts statuses.

**Note:** This feature uses AI to generate results. AI-generated content may not be accurate or complete. Review the validated parts summary before confirming the results.

## Procedure

1.  Log in to the ServiceNow Agent mobile application.

2.  Tap **My Work**.

3.  Tap a work order task under **My Tasks**.

4.  Tap **ServiceNow Otto** on the navigation bar to open ServiceNow Otto Virtual Agent.

5.  Ask AI to validate parts for the work order task.

    The Parts Manager AI agent analyzes your work notes and the work order task details, then presents a summary of validated parts. The summary includes parts used, parts removed, and parts not used.

6.  Review the validated parts summary and select **Yes** or **No** when prompted to mark the validation as done.

7.  Tap **Submit**.

    The parts statuses and inventory are updated based on the validated results.


## What to do next

To verify the updated parts for the task, open the work order task and tap the more options icon next to **Related**, then tap **Parts**.

