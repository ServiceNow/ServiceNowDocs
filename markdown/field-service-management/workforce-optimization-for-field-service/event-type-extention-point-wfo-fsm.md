---
title: Event type extension point in Workforce Optimization for Field Service
description: Use extension points to call scripts for event categories such as meeting, time off, or work time.
locale: en-US
release: zurich
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up scheduling, Workforce Optimization, Set up workforce, Configure, Field Service Management]
---

# Event type extension point in Workforce Optimization for Field Service

Use extension points to call scripts for event categories such as meeting, time off, or work time.

Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

You can use extension points to create events such as meeting, training, and time-off requests. For example extension point implementations, see the following extension instances in the Implementations related list:

|Category|Extension Script|
|--------|----------------|
|Meeting|AgentScheduleMeetingEventManager|
|Break|AgentScheduleBreakEventManager|
|Training|AgentScheduleBreakEventManager|
|Time off|AgentScheduleBreakEventManager|
|Work|AgentScheduleWorkEventManager|
|Actual Work|AgentScheduleActualWorkEventManager|
|Personal|AgentSchedulePersonalEventManager|

