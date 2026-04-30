---
title: Set up skill prediction to resolve similar tasks in Workforce Optimization for Field Service
description: Collect skill data based on the skills agents have used for task completion. Use supervised learning to recommend these skills for agents to resolve similar work order tasks. You can also find patterns in how skills are used to complete the task and use unsupervised learning to recommend skills for agents.Use scripted extension points to customize skill prediction for tasks.
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Coaching, Workforce Optimization, Set up workforce, Configure, Field Service Management]
---

# Set up skill prediction to resolve similar tasks in Workforce Optimization for Field Service

Collect skill data based on the skills agents have used for task completion. Use supervised learning to recommend these skills for agents to resolve similar work order tasks. You can also find patterns in how skills are used to complete the task and use unsupervised learning to recommend skills for agents.

## Before you begin

-   Set up skills. For more information, see [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

-   Predictive Intelligence must be set up and configured on your instance to train the models. For more information, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

    Activate the Skill Recommendation application plugin \(com.snc.sre\) to use predictive intelligence for recommending skills.


Role required: sn\_sre.admin

## Procedure

1.  Configure the properties for the Skill recommendation application.

    For more information, see [properties for the Skill Recommendation application](../reference/components-wfo-fsm.md).

2.  Run the solution definition models such as **Recommend similar skills for cases** or **Recommend skills from similar cases** to train the supervised and unsupervised solutions.

    For more information on training a solution, refer to [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

3.  Run the **Start skill prediction** scheduled job every day to start predicting skills for cases or agents.

    This scheduled job is inactive by default. When you activate it, the job runs daily at 1:00 a.m. on all cases resolved the previous day. The job then adds the skills to the User Predicted Skill \[sn\_sre\_user\_predicted\_skill\] and Task Predicted Skill \[sn\_sre\_task\_predicted\_skill\] tables.

    **Note:** Recommended skills will start appearing once the number of records in the User Predicted Skill \[sn\_sre\_task\_predicted\_skill\] table exceeds the value defined in the **sn\_sre.user\_predicted\_skill\_threshold** property. For more information, see [Workforce Optimization for Field Service components](../reference/components-wfo-fsm.md).


## Use extension points for skill prediction

Use scripted extension points to customize skill prediction for tasks.

### Before you begin

Role required: admin

### About this task

You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed.

Note that the Skill Recommendation extension point is included with the Skill Recommendation \(com.snc.sre\) plugin.

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Client Extension Points**.

2.  From the Extension Points list, select **Skill Recommendation** \(sn\_sre.SkillPredictionAPI\).

3.  Either create a new skill recommendation implementation or modify an existing one.

    -   To create a new skill recommendation implementation, click **Create Implementation**.
    -   To modify an existing implementation, from the Implementations related list, select a class.
4.  Modify the script as required.

5.  Click **Update**.


