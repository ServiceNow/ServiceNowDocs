---
title: Approve or reject recommended skills in Workforce Optimization for ITSM
description: Approve predicted skills if the skill is necessary for the agent to complete assigned tasks. If the skill doesn't apply to the agent, you can reject a skill.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Adding skills to agents' skill set, Skills Management, Workforce Optimization for ITSM, IT Service Management]
---

# Approve or reject recommended skills in Workforce Optimization for ITSM

Approve predicted skills if the skill is necessary for the agent to complete assigned tasks. If the skill doesn't apply to the agent, you can reject a skill.

## Before you begin

Role required: skill\_manager

## About this task

The Predictive Intelligence application for skills displays the recommended skills on each agent's profile. The application uses sample incidents that the agent has worked on to recommend skills for an agent.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Select the coaching icon.

3.  Select the **Skills** tab.

4.  Approve or reject a skill that is recommended by Predictive Intelligence.

    1.  In the skill matrix, select **Recommended** to approve and recommend a skill for the user.
    2.  In the **Details** tab, review the request for skill approval, the sample incident resolutions that were used to predict the skill, and the activity stream.
        -   To approve a skill, select **Approve**. The skill is added to the agent and the lowest level for the skill is automatically associated with the added skill. The state for the request changes to **Approved** and the skill is added to the agent.
        -   To reject a skill, select **Reject**. The state for the request changes to **Rejected**. Predictive Intelligence doesn’t recommend the skill for the user again and the field changes to **Add**.
    3.  Select the more options \(![More options icon](../image/ellipsis_icon.png)\) icon and select **Save**.
    The application assigns the skill to the user. If the assigned skill doesn’t have a skill level, the application adds the basic skill level to the user.


**Parent Topic:**[Adding skills to agents' skill set in Workforce Optimization for ITSM](../concept/adding-skills-agents-skillset-wfo-itsm.md)

