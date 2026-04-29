---
title: Optimizing technician schedules at set intervals throughout the day
description: Efficiently reassign tasks and maximize productivity by continuously running schedule optimization at selected intervals throughout the day.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Optimizing technician schedules at set intervals throughout the day

Efficiently reassign tasks and maximize productivity by continuously running schedule optimization at selected intervals throughout the day.

## About intraday optimization

Intraday is an event-based mode of Schedule Optimization that runs on a set interval to optimize schedules in response to canceled tasks and other events such as a technician running late, a technician calling in sick, an agent using PTO, or a new high priority task being added.

Create a policy, a grouping of optimization features that run in combination, to define the rules for optimization. Policy objectives prioritize technician task assignment. Policy constraints determine the criteria that must be met for an assignment group or territory to be assigned a task.

The basic intra-day flow runs every 60 minutes by default, with a minimum option of every 15 minutes. When a trigger condition is met, an intraday event is created. When the next intraday flow runs, an intra-day job is created for each of the groups or territories that have intraday events and those qualifiers are optimized. When a group or territory is selected for optimization, all tasks within the group are considered for optimization, except for schedule-locked tasks. When optimization is complete and the tasks are updated, the intraday job shows a status of Assignment Complete.

Prioritized event optimization responds immediately to critical events instead of waiting for the next scheduled intraday run. When a high-priority event occurs, prioritized optimization triggers shortly after and targets only the specific technicians and tasks affected by the event. This focused approach ensures urgent scheduling changes are handled quickly without reoptimizing all tasks in the group or territory.

Dispatchers can manually trigger optimization to run from the Dispatcher Workspace when the intraday on demand optimization configuration is enabled and an on demand applicable policy has been added to the scheduling attribute. See [Create a scheduling attribute for Schedule Optimization](configure-scheduling-attributes.md) to add an on demand applicable policy to the configuration.

Note that agent schedules can't be manually updated until intraday optimization is complete.

