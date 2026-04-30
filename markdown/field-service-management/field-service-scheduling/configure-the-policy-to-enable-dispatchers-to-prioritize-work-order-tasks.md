---
title: Configure the policy to enable dispatchers to prioritize work order tasks
description: Incorporate optimization features into the policy to allow dispatchers to prioritize work orders, establishing the importance of each task.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a policy for Schedule Optimization, Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configure the policy to enable dispatchers to prioritize work order tasks

Incorporate optimization features into the policy to allow dispatchers to prioritize work orders, establishing the importance of each task.

## Before you begin

Role required: wm\_admin

## About this task

By completing this task, you are allowing dispatchers to add importance to a work order task. You must incorporate three specific optimization features into the relevant policy: Maximize higher value task assignments, Minimize task time penalties \(fixed\), and Minimize task time penalties \(hourly\). This allows Schedule Optimization to take these values and penalties into account during processing.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Policies**.

2.  Select the policy.

3.  Select the **Objective** or **Constraint** tab.

4.  Select **New**.

5.  In the **Optimization Features** field, select the Lookup icon \(![Lookup icon.](../../../common/image/List_SearchIcon.png)\) and add the following objectives and constraints:

6.  1.  Maximize higher value task assignments
2.  Minimize task time penalties \(fixed\)
3.  Minimize task time penalties \(hourly\)
7.  Select **Submit**.


