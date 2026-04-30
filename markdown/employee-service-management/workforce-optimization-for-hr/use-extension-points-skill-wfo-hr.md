---
title: Use extension points for skill prediction in Workforce Optimization for HR
description: Use scripted extension points to customize skill prediction for tasks.
locale: en-US
release: yokohama
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up skill prediction in Workforce Optimization for HR, Setting up Coaching in Workforce Optimization for HR, Configuring Workforce Optimization for HR, Workforce Optimization for HR Overview, HR Service Delivery, Employee Service Management]
---

# Use extension points for skill prediction in Workforce Optimization for HR

Use scripted extension points to customize skill prediction for tasks.

## Before you begin

The Skill Recommendation extension point is included with the Skill Recommendation \(com.snc.sre\) plugin.

Role required: sn\_hr\_wfo.admin

## About this task

You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Client Extension Points**.

2.  From the Extension Points list, select **Skill Recommendation** \(sn\_sre.SkillPredictionAPI\).

3.  Do one of the following:

    -   To create a new skill recommendation implementation, click **Create Implementation**.
    -   To modify an existing implementation, from the **Implementations** related list, select a class.
4.  Modify the script as required.

5.  Click **Update**.


**Parent Topic:**[Setting up skill prediction in Workforce Optimization for HR](setup-skill-prediction-wfo-hr.md)

