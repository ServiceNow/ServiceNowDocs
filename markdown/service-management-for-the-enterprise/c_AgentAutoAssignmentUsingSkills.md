---
title: Agent auto assignment using skills
description: Agents can be auto assigned based on the skills of an agent, and the skills required to perform the task. Assign skills to an agent user records using Skills Users .
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent auto assignment using rating-based criteria, Agent auto assignment, Agent assignment methods, Request Management in a Service Management application, Service Management]
---

# Agent auto assignment using skills

Agents can be auto assigned based on the skills of an agent, and the skills required to perform the task. Assign skills to an agent user records using **Skills** &gt; **Users**.

Auto assignment by skills can be performed in either a [task- or request-driven processing](c_TaskVsRequestDrivenProcessing.md) environment when the **Auto-selection of agents for tasks requires them to have skills** configuration option must be set to **all** or **some** for the application.

When a task that includes skills is qualified or marked as **Ready for Work**, skills of each agent are compared with the skills required to perform the task, and a rating is calculated based on the skills configuration option. If the option is set to **some**, the agent with the closest skills match is auto-assigned the task. If the option is set to **all**, only agents who possess all the required skills are considered. If no agents possess all the skills required to perform the task, none are auto-assigned.

Skills rating of an agent is calculated as:

`Skills_agent/Skills_task`

When:

-   `Skills_agent` is the number of skills possessed by the agent that match the skills required for the task.
-   `Skills_task` is the total number of skills required for the task.

For example, if a task requires four skills, and Agent A possesses three of them and Agent B possesses two of them:

-   Skill rating of Agent A = 3/4 or 0.75
-   Skill rating of Agent B = 2/4 or 0.5

If the application is configured to use other selection criteria, such as location or time zone, the ratings of all selection criteria are averaged, and the agent with the highest overall rating is auto-selected for the task. See [Agent auto assignment using multiple selection criteria](c_AgAtAssgmtMlt.md) for details.

**Parent Topic:**[Agent auto assignment using rating-based criteria](c_AgentAutoAssignUseRatBaseCrit.md)

