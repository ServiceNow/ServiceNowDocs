---
title: Agent auto assignment using location
description: Agents can be auto assigned based on the location defined in their user record and the location of the tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent auto assignment using rating-based criteria, Agent auto assignment, Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Agent auto assignment using location

Agents can be auto assigned based on the location defined in their user record and the location of the tasks.

Auto assignment by location can be performed in a [task- or request-driven processing](c_TaskVsRequestDrivenProcessing.md) environment when the **Auto-selection of agents will consider location of agents** configuration is enabled.

When a task is created, agent locations are compared to the following ranges to determine a location rating for each agent.

|Distance \(mi.\) from agent to task|Rating|
|-----------------------------------|------|
|0–0.1|1|
|0.11–0.5|0.9|
|0.51–5|0.7|
|5.1–10|0.5|
|10.1–20|0.4|
|20.1–30|0.3|
|30.1–40|0.2|
|40.1–100|0.1|
|&gt;100|0|

When a task is qualified or marked as **Ready for Work**, the agent closest to the task location is considered for the task. If the application is configured so that only location is considered, the closest agent is auto-assigned to the task.

If the application is configured to use other selection criteria—such as skills, time zone, or schedule—the ratings of all selection criteria are averaged, and the agent with the highest overall rating is auto-assigned for the task. See [Agent auto assignment using multiple selection criteria](c_AgAtAssgmtMlt.md) for details.

**Parent Topic:**[Agent auto assignment using rating-based criteria](c_AgentAutoAssignUseRatBaseCrit.md)

