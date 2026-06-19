---
title: Create extension points for Work scheduler
description: Create extension points to customize your implementation in Work scheduler. For example, if you want your team members to work on an on-site task, you can configure the location of your team members to the work items assigned to them so that they can get to the tasks quickly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/create-work-sched-ext-points-wfo-cs.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up Work scheduler, Optimize workforce operations, Extend capabilities, Configure, Customer Service Management]
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


**Parent Topic:**[Setting up Work scheduler in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/setting-up-work-scheduler-wfo-cs.md)

