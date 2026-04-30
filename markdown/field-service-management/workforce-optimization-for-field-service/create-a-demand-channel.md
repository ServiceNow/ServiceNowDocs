---
title: Create a demand channel
description: Demand channels help organize and manage work by efficiently distributing resources. When creating a reservation rule, you can allocate a specific percentage of capacity to a particular demand channel. By tagging work orders or tasks with demand channels, you ensure they are routed correctly, improving resource allocation and scheduling accuracy.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Capacity and Reservations Management, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create a demand channel

Demand channels help organize and manage work by efficiently distributing resources. When creating a reservation rule, you can allocate a specific percentage of capacity to a particular demand channel. By tagging work orders or tasks with demand channels, you ensure they are routed correctly, improving resource allocation and scheduling accuracy.

## Before you begin

Role required: wm\_admin, wm\_manager, sn\_fsm\_tp.fsm\_territory\_manager, sn\_fsm\_tp.fsm\_territory\_planner

Ensure the Field Service Territory Planning \(com.snc.fsm\_territory\_planning\) plugin is installed.

## About this task

The scheduling system uses demand channel attributes \(conditions and order\) for capacity reservation rules based on demand channels. For more information, see [Create a reservation rule](../concept/capacity-reservations.md#)

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Capacity Management** &gt; **Demand Channel**.

2.  Click **New**.

3.  On the form, fill the fields.

4.  |Field|Description|
|-----|-----------|
|Name|Name of the demand channel. For example, "Install" for installation-related tasks.|
|Active|Select this option to activate the demand channel.|
|Order|Order of preference of the demand channel.|
|Default|If selected, this demand channel becomes the default one. For instance, if the total capacity is 100, and specific channels like "Install" and "Breakfix" take up 30 and 50 respectively, the remaining 20 will be allocated to this default channel.|
|Table|Select the table used to categorize demand channel. By default, this is set to `wm_task`.|
|Condition|Conditions to filter the data. For example, setting the work type as "Installation" ensures the system checks the reservation rule for capacity usage when a task is received.|

5.  Click **Submit**.

    The demand channel is created. You can use the demand channel in the reservation rules.


## Create demand channel for installation related task assignments

Let's create a demand channel named "Install":

1.  Name: Install
2.  Active: Yes
3.  Order: 1
4.  Default: False
5.  Table: wm\_task
6.  Condition: `work_type = Installation`

By defining these fields, the "Install" demand channel in the reservation rule will help route installation related tasks correctly and ensure proper capacity allocation.

**Related topics**  


[Field Service Territory Capacity Analytics dashboard](../../../use/dashboards/application-content-packs/capacity-dashboard.md)

