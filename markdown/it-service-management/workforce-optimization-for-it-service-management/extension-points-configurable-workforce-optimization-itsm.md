---
title: Event type extension points in Workforce Optimization for ITSM
description: Use extension points to call scripts for event categories such as a meeting, time off, or work time.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Event type extension points in Workforce Optimization for ITSM

Use extension points to call scripts for event categories such as a meeting, time off, or work time.

## Creating custom event types using extension points

When you create extension points for custom events, consider the following:

-   Which users can create an event?
-   Does the event have to go through an approval process?
-   Is it a work-type or a non-work type event?

Here are some examples that provide guidance on some of the considerations you may want to take into account when you create a new custom event using extension points:

-   When you create an event for monthly staff meetings, take the following into consideration:
    -   Only managers can create this type of event.
    -   This is a non-work type event.
    -   The event does not have to go through an approval process.
-   When you create an event for time-off requests, take the following into consideration:
    -   Any employee can create this event.
    -   The is a non-work type event.
    -   The event has to go through a manager approval process.

To see a list of extension points that you can use for Workforce Optimization for ITSM, navigate to **System Extension Points** &gt; **Scripted Extension Points**. In the Extension Points list, open the sn\_shift\_planning.EventManager extension point.

Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

|Extension point name|Description|
|--------------------|-----------|
|sn\_shift\_planning.EventManager|Implement this extension point to customize the logic for the event categories that you create.|

You can use extension points to create events such as meeting, training, and time-off requests. For example extension point implementations, see the following extension instances in the Implementations related list:

|Category|Extension script|
|--------|----------------|
|Meeting|AgentScheduleMeetingEventManager|
|Break|AgentScheduleBreakEventManager|
|Training|AgentScheduleTrainingEventManager|
|Time off|AgentScheduleTimeOffEventManager|
|Work|AgentScheduleWorkEventManager|

**Parent Topic:**[Setting up Scheduling in Workforce Optimization for ITSM](../concept/setup-scheduling-configurable-workforce-optimization-itsm.md)

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

