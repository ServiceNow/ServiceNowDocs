---
title: Agent auto assignment using schedules
description: Agents can be auto assigned based on the agent or the task schedule.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent auto assignment using time-based criteria, Agent auto assignment, Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Agent auto assignment using schedules

Agents can be auto assigned based on the agent or the task schedule.

Auto assignment by schedule can be performed only in a [task-driven processing](c_TaskVsRequestDrivenProcessing.md) environment, and the **Auto-selection of agents will consider agent or task schedules** configuration option must be enabled for the application. If this option is turned off, only the [agent ratings](c_AgentAutoAssignUseRatBaseCrit.md) are used for auto-assignment.

When a task is qualified or marked as **Ready for Work**, agents ratings are evaluated, and the schedules of qualified agents are compared against the schedule of the task to determine the agent with the best matching schedule.

**Note:** If the task includes specific time entries in the **Window start** and **Window end** fields, and no schedule of an agent falls within that task window, no agents are assigned. Also if the customer wants a task to be performed at or near a specific time, the **Window start** time should be set as close to that time as possible. For example, the **Window start** and **Window end** fields are set to 1:00 pm and 8:00 pm respectively. The customer prefers the job to be started at 4:00 pm. It is possible that an agent is dispatched at 13:00. So, setting the **Window start** closer to 4:00 can help ensure that the work is performed when the customer prefers it to be done.

If the application is configured to use other selection criteria, such as skills or time zone, the ratings of all selection criteria are averaged, and the agent with the highest overall rating is auto-selected for the task. See [Agent auto assignment using multiple selection criteria](c_AgAtAssgmtMlt.md) for details.

**Parent Topic:**[Agent auto assignment using time-based criteria](c_AgAtAssgnTime.md)

