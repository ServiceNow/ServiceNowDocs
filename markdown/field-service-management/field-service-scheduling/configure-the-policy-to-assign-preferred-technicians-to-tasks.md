---
title: Configure the policy to assign preferred technicians to tasks
description: Add optimization features to the policy, enabling dispatchers to assign preferred Field Service agents to specific work order tasks, ensuring the right technician handles each task efficiently. Additionally, dispatchers can exclude agents who are not well-suited for certain tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/configure-the-policy-to-assign-preferred-technicians-to-tasks.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create policies, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure the policy to assign preferred technicians to tasks

Add optimization features to the policy, enabling dispatchers to assign preferred Field Service agents to specific work order tasks, ensuring the right technician handles each task efficiently. Additionally, dispatchers can exclude agents who are not well-suited for certain tasks.

## Before you begin

Role required: wm\_admin

## About this task

Dispatchers can designate preferred, secondary, or excluded technicians on the work order task record. To activate this capability, an admin must incorporate specific optimization features into the policy.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Policies**.

2.  Select the policy.

3.  Select the **Objective** or **Constraint** tab.

4.  Select **New**.

5.  In the **Optimization Features** field, select the Lookup icon \(\[Omitted image "List\_SearchIcon.png"\] Alt text: Lookup icon.\) and add the following objectives and constraints:

6.  1.  Maximize preferred agent assignment
2.  Enable assignments based on technician assignment preference
3.  Block excluded agents from assignment
7.  Select **Submit**.


## Result

The policy is configured to assign preferred technicians to tasks. When the optimization run is complete, check the [Run Summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/viewing-task-assignments-from-so-runs.md) to view assignment outcomes for tasks with required, preferred, or secondary technician preferences. Tasks that could not be assigned to a required technician are listed in the run summary.

**Related topics**  


[Objectives and constraints used with Schedule Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/hard-soft-constraints.md)

[Set technician preferences for tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/assign-preferred-agents-tasks.md)

