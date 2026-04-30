---
title: Create extension points for Work scheduler
description: Create extension points to customize your implementation in Work scheduler. For example, if you want your team members to work on an on-site task, you can configure the location of your team members to the work items assigned to them so that they can get to the tasks quickly.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Work scheduler in Workforce Optimization for ITSM, Work scheduler in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Create extension points for Work scheduler

Create extension points to customize your implementation in Work scheduler. For example, if you want your team members to work on an on-site task, you can configure the location of your team members to the work items assigned to them so that they can get to the tasks quickly.

## Before you begin

Role required: admin

You must set the application scope to Work scheduler \(sn\_wfo\_work\_sched\).

## About this task

The **WorkItemSkillsRecommendationManager** extension point is available by default.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Open the **sn\_wfo\_work\_sched.WorkItemRecommendationManager** extension point.

3.  In the Related Links section, select **Create Implementation**.

4.  Define the functions based on your needs to customize your implementation.


**Parent Topic:**[Setting up Work scheduler in Workforce Optimization for ITSM](../concept/setting-up-work-scheduler.md)

