---
title: Qualify and rank users based on skills and skill levels
description: Rank users so that you can select the right users based on skills needed to complete tasks. Qualify users to work on tasks such as case, work order task, or chat interaction based on the number of skills and skill levels required to work on those tasks.
locale: en-US
release: australia
product: Skills Management
classification: skills-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Routing work items to agents based on skills, Using Skills Management, Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Qualify and rank users based on skills and skill levels

Rank users so that you can select the right users based on skills needed to complete tasks. Qualify users to work on tasks such as case, work order task, or chat interaction based on the number of skills and skill levels required to work on those tasks.

## Before you begin

Role required: skill\_admin

## About this task

Use the [UserSkillAnalyzer API](https://www.servicenow.com/docs/access?context=UserSkillAnalyzerAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) to analyze the skills and skill levels of users and the [UserSkillRanking API](https://www.servicenow.com/docs/access?context=UserSkillRankingAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) to rank and assign them to tasks. For example, when you use the Field Service Management application to assign agents to tasks, you can analyze and rank them based on their skills and skill levels using these APIs and use dynamic scheduling to assign them to tasks.

**Note:** You must add the Matching Skill Level Gap for Dynamic Scheduling criterion to the task filter to rank agents assessed based on skill gaps. For more information on adding this criterion, see [Create a task filter](https://www.servicenow.com/docs/access?context=create-dynamic-scheduling-config&version=australia&pubname=australia-field-service-management&section=create-task-filter&ft:locale=en-US).

## Procedure

1.  Analyze the skills and skill levels users have to complete work items using the UserSkillAnalyzer API.

    The API performs the following verification to check if users are qualified to be assigned to the work items:

    1.  If the user has all mandatory skills required to complete the work item, but does not have the skill level, the agent is not qualified to work on the task if the skill level is mandatory to work on the task.
    2.  If the user does not have all mandatory skills required to complete the task, the agent is not qualified to work on the task.
    3.  If the user has all skills and the skill levels required to complete the task, the agent is qualified to work on the task.
    4.  If the user has all skills required, but not mandatory to complete the task, the agent is qualified to work on the task.
    If the user is qualified to work on the task, the API performs the following verification to analyze gaps in skill level and the total number of skills the users have to execute tasks based on the skill requirements for the work item:

    1.  Verifies if a work item requires a skill that does not have a level type defined.
    2.  Verifies if a work item requires a skill that has a level type defined but does not have the skill level defined.
    3.  Verifies if a work item requires a skill that has the skill level defined, but the agent does not have the skill level defined. If the skill level is mandatory to complete the task, the user who does not have those skill levels will not be assigned to those tasks.
    4.  Verifies whether a user has all skill levels that are mandatory, but not optional, to perform a task.
2.  Rank users qualified to complete work items using [UserSkillRanking API](https://www.servicenow.com/docs/access?context=UserSkillRankingAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

    The API retrieves a list of qualified users based on matching and mandatory skills and skill levels.


**Parent Topic:**[Routing work items to agents based on skills](../concept/skill-based-routing.md)

**Related topics**  


[Dynamic scheduling](https://www.servicenow.com/docs/access?context=dynamic-scheduling&version=australia&pubname=australia-field-service-management&ft:locale=en-US)

