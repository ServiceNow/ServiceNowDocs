---
title: Setting up skill prediction in Workforce Optimization for ITSM
description: Collect skill data based on skills agents have used for incident resolution. Use supervised learning to recommend these skills for agents to resolve similar open incidents. You can also find patterns in how skills are used for incident resolution and use unsupervised learning to recommend skills for agents.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Skills Management, Workforce Optimization for ITSM, IT Service Management]
---

# Setting up skill prediction in Workforce Optimization for ITSM

Collect skill data based on skills agents have used for incident resolution. Use supervised learning to recommend these skills for agents to resolve similar open incidents. You can also find patterns in how skills are used for incident resolution and use unsupervised learning to recommend skills for agents.

## Before you begin

Predictive Intelligence must be set up and configured on your instance to train the models. For more information, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Activate the Skill Recommendation application plugin \(com.snc.sre\) to use predictive intelligence for recommending skills.

Role required: sn\_sre.admin

## Procedure

1.  Configure the [properties for the Skill Recommendation application](../reference/configurable-wfo-itsm-skill-recommendation-reference.md).

2.  Run the solution definition models to train the supervised and unsupervised solutions.

    For more information on training a solution, refer to [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

3.  Run the **Start skill prediction** scheduled job everyday to start predicting skills for incidents or agents.

    This scheduled job is inactive by default. When you activate it, the job runs daily at 1:00 AM on all incidents resolved the previous day. The job then adds the skills to the User Predicted Skill \[sn\_sre\_user\_predicted\_skill\] table and Task Predicted Skill \[sn\_sre\_task\_predicted\_skill\] table.


-   **[Use extension points for skill prediction](extension-points-skill-prediction-wfo-itsm.md)**  
Use scripted extension points to customize skill prediction for tasks.

**Parent Topic:**[Skills Management in Workforce Optimization for ITSM](../concept/skills-management-wfo-itsm.md)

