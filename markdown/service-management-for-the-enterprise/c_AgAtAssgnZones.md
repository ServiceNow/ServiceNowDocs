---
title: Agent auto assignment using time zones
description: Agents can be auto assigned based on the time zone defined in their user records and the time zone of the tasks.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent auto assignment using rating-based criteria, Agent auto assignment, Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Agent auto assignment using time zones

Agents can be auto assigned based on the time zone defined in their user records and the time zone of the tasks.

Auto assignment by time zone can be performed in either a [task- or request-driven processing](c_TaskVsRequestDrivenProcessing.md) environment when the **Auto-selection of agents will consider time zone for the task** configuration option must be enabled for the application.

When a task is qualified or marked as **Ready for Work**, agents in the time zone closest to the task time zone are considered for the task. If the application is configured so that only time zone is considered, an agent in the same time zone is auto-assigned the task.

**Note:** It is important that the time zones for the agent and the task are set correctly.

When a task is created, agents are rated based on the time zones of both task and agent using the following formula:

`1 - [abs(Task_tz – Agent_tz) ÷ 12]`

Where:

-   `abs` is the mathematical function to compute the absolute value.
-   `Task_tz` is the offset between the time zone of the task and GMT.
-   `Agent_tz` is the offset between the time zone of the agent and GMT.

For example, a task is created in New York City \(GMT-4\), and two agents are available to perform the task, one in Los Angeles \(GMT-7\) and one in Paris, France \(GMT+1\).

The rating of the agent in Los Angeles is calculated as:

`1 - abs((-4) - (-7)) ÷ 12 or 0.75`

The rating of the agent in Paris is calculated as:

`1 - abs((-4) - (+1)) ÷ 12 or 0.58`

So if the auto assignment of the task is based on the time zone alone, it is assigned to the agent from Los Angeles.

If the application is configured to use other selection criteria, such as skills or location, the ratings of all selection criteria are averaged, and the agent with the highest overall rating is auto-selected for the task. See [Agent auto assignment using multiple selection criteria](c_AgAtAssgmtMlt.md) for details.

**Parent Topic:**[Agent auto assignment using rating-based criteria](c_AgentAutoAssignUseRatBaseCrit.md)

