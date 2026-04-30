---
title: Use extension points for skill prediction
description: Use scripted extension points to customize skill prediction for tasks.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up skill prediction in Workforce Optimization for ITSM, Skills Management in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Use extension points for skill prediction

Use scripted extension points to customize skill prediction for tasks.

## Before you begin

The Skill Recommendation extension point is included with the Skill Recommendation \(com.snc.sre\) plugin.

Role required: admin

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


**Parent Topic:**[Setting up skill prediction in Workforce Optimization for ITSM](setup-skill-prediction-configurable-wfo-itsm.md)

