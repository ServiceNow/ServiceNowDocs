---
title: Event type extension points in Workforce Optimization for HR
description: Use extension points to call scripts for event categories such as meeting, time off, or work time.
locale: en-US
release: australia
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Scheduling for Workforce Optimization for HR, Configuring Workforce Optimization for HR, Workforce Optimization overview, HR Service Delivery, Employee Service Management]
---

# Event type extension points in Workforce Optimization for HR

Use extension points to call scripts for event categories such as meeting, time off, or work time.

To see a list of extension points that you can use for Workforce Optimization for HR, navigate to **System Extension Points** &gt; **Scripted Extension Points**. In the Extension Points list, open the sn\_shift\_planning.EventManagerextension point.

Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

|Extension points|Description|
|----------------|-----------|
|sn\_shift\_planning.EventManager|Implement this extension point to customize the logic for the event categories that you create.|

You can use extension points to create events such as meeting, training, and time-off requests. For example extension point implementations, see the following extension instances in the Implementations related list:

|Category|Extension Script|
|--------|----------------|
|Meeting|AgentScheduleMeetingEventManager|
|Break|AgentScheduleBreakEventManager|
|Training|AgentScheduleTrainingEventManager|
|Time off|AgentScheduleTimeOffEventManager|
|Work|AgentScheduleWorkEventManager|
|On call|AgentScheduleOnCallEventManager|
|On Call Time Off|AgentScheduleOnCallTimeOffEventManager|
|Actual Work|AgentScheduleActualWorkEventManager|

**Parent Topic:**[Setting up Scheduling for Workforce Optimization for HR](../task/setup-scheduling-wfo-hr.md)

