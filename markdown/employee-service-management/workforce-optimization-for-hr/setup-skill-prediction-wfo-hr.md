---
title: Setting up skill prediction in Workforce Optimization for HR
description: Collect skill data based on skills agents have used for case resolution. Use supervised learning to recommend these skills for agents to resolve similar open case. You can also find patterns in how skills are used for case resolution and use unsupervised learning to recommend skills for agents.
locale: en-US
release: australia
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Coaching in Workforce Optimization for HR, Configuring Workforce Optimization for HR, Workforce Optimization overview, HR Service Delivery, Employee Service Management]
---

# Setting up skill prediction in Workforce Optimization for HR

Collect skill data based on skills agents have used for case resolution. Use supervised learning to recommend these skills for agents to resolve similar open case. You can also find patterns in how skills are used for case resolution and use unsupervised learning to recommend skills for agents.

## Before you begin

Set up skills. For more information, see Skills Management.

Predictive Intelligence must be set up and configured on your instance to train the models. For more information, see Predictive Intelligence.

Activate the Skill Recommendation application plugin \(com.snc.sre\) to use predictive intelligence for recommending skills.

Role required: sn\_hr\_wfo.admin

## Procedure

1.  Configure the skill prediction property.

2.  Run the solution definition models such as **Recommend similar skills for cases** or **Recommend skills from similar cases** to train the supervised and unsupervised solutions.

    For more information on training a solution, refer to Create and train a similarity solution.

3.  Run the **Start skill prediction** scheduled job everyday to start predicting skills for cases or agents.

    This scheduled job is inactive by default. When you activate it, the job runs daily at 1:00 AM on all cases resolved the previous day. The job then adds the skills to the User Predicted Skill \[sn\_sre\_user\_predicted\_skill\] table and Task Predicted Skill \[sn\_sre\_task\_predicted\_skill\] table.

    **Note:** Recommended skills will start appearing once the number of records in \[sn\_sre\_task\_predicted\_skill\] table exceeds the value defined in the \[sn\_sre.user\_predicted\_skill\_threshold\] .


-   **[Use extension points for skill prediction in Workforce Optimization for HR](use-extension-points-skill-wfo-hr.md)**  
Use scripted extension points to customize skill prediction for tasks.

**Parent Topic:**[Setting up Coaching in Workforce Optimization for HR](../concept/setup-coaching-wfo-hr.md)

