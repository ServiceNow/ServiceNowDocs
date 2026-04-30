---
title: Configure the policy to assign preferred technicians to tasks
description: Add optimization features to the policy, enabling dispatchers to assign preferred Field Service agents to specific work order tasks, ensuring the right technician handles each task efficiently. Additionally, dispatchers can exclude agents who aren’t well suited for certain tasks.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a policy for Schedule Optimization, Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configure the policy to assign preferred technicians to tasks

Add optimization features to the policy, enabling dispatchers to assign preferred Field Service agents to specific work order tasks, ensuring the right technician handles each task efficiently. Additionally, dispatchers can exclude agents who aren’t well suited for certain tasks.

## Before you begin

Role required: wm\_admin

## About this task

Dispatchers can designate preferred, secondary, or excluded technicians on the work order task record. To activate this capability, an admin must incorporate specific optimization features into the policy.

## Procedure

1.  Navigate to **All** &gt; **Schedule Optimization** &gt; **Administration** &gt; **Policies**.

2.  Select the policy.

3.  Select the **Objective** or **Constraint** tab.

4.  Select **New**.

5.  In the **Optimization Features** field, select the Lookup icon \(![Lookup icon.](../../../common/image/List_SearchIcon.png)\) and add the following objectives and constraints:

6.  1.  Maximize preferred agent assignment
2.  Enable assignments only with preferred or secondary agents
3.  Block excluded agents from assignment
7.  Select **Submit**.


