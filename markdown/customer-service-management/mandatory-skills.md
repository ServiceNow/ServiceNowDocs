---
title: Mandatory skills
description: Use the mandatory skills feature to identify any skills that are required for agents and technicians to work on customer service cases and field service work orders and tasks. Then assign cases and tasks to agents and technicians who have those required skills.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Skills Management, Configure case routing and assignment, Configure case management, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Mandatory skills

Use the mandatory skills feature to identify any skills that are required for agents and technicians to work on customer service cases and field service work orders and tasks. Then assign cases and tasks to agents and technicians who have those required skills.

When assigning cases, work orders, and work order tasks, the assignment tools consider the mandatory skills, filter out agents and technicians who don’t have these skills, and then rank the remaining agents.

-   If agents with the mandatory skills are available, the cases and tasks are assigned to these agents.
-   If agents with the mandatory skills aren’t available, then agents with any other, non-mandatory skills identified in the cases and tasks are ranked and assigned.

Field service dispatchers \(wm\_dispatcher\), field service technicians \(wm\_agent\), customer service managers \(sn\_customerservice\_manager\), and customer service agents \(sn\_customerservice\_agent\) can specify both skills and mandatory skills for cases and tasks.

Mandatory skills are an optional feature. Mandatory skills can be identified on the assignment workbench. In addition to the **Skills** list, the assignment workbench includes a **Mandatory Skills Added** list. Agents are ranked in the workbench based on the number of skills that match the skills identified in the Skills list. If the mandatory skills feature is being used, then the agents displayed are filtered by the skills listed in the Mandatory Skills Added list and then ranked by the other matching criteria.

**Related topics**  


[Use the assignment workbench](case-assignment-workbench.md)

