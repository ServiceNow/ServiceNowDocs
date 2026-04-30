---
title: Intra-day schedule automation flows and subflows
description: The flows and subflows for configuring intra-day schedule automation.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field Service Management reference, Field Service Management]
---

# Intra-day schedule automation flows and subflows

The flows and subflows for configuring intra-day schedule automation.

## Intra-day scheduling flows

-   Agent time off created – The agent records time off, blocking availability.
-   FSM agent not take action – The agent fails to act as expected-for example, not marking travel start- triggering a dispatcher alert.
-   Work order task progressed – A task progresses, but the agent is early or late, affecting schedule timing.
-   Canceled task-A task is canceled. Schedule Optimization fills the gap.
-   High priority task- A high-priority task is added. Schedule Optimization reschedules to minimize disruption.

## Intra-day scheduling subflows

|Subflow|Description|
|-------|-----------|
|Agent tasks left adjustment|The agent was early to a task, so tasks shift to the left to accommodate for the early schedule.|
|Agent tasks right adjustment|The agent was late to a task, so the task shifts to the right to accommodate for the later schedule.|
|Auto-assign unassigned tasks|Unassigned tasks that are in the queue are automatically assigned to available agents.|
|Flag work order tasks|Work order tasks are flagged for review.|
|FSM send notification and flag the task|Work order tasks are flagged for review and the dispatcher is notified.|
|FSM wait for travel start|Checks whether the agent started to travel at the specified time.|
|FSM wait for work complete|Checks that the agent completed work at the specified time.|
|FSM wait for work start|Checks that the agent started work at the specified time.|
|Run task recommendation|Recommends tasks for an agent with free time. For example, the task recommendation runs if the agent has canceled tasks or ended a task early.|

**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

