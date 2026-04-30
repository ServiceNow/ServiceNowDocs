---
title: Optimizing technician schedules at set intervals throughout the day
description: Efficiently reassign tasks and maximize productivity by continuously running schedule optimization at selected intervals throughout the day.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Schedule Optimization, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Optimizing technician schedules at set intervals throughout the day

Efficiently reassign tasks and maximize productivity by continuously running schedule optimization at selected intervals throughout the day.

## About intra-day optimization

Intraday is an event-based mode of Schedule Optimization that runs on a set interval to optimize schedules in response to canceled tasks and other events such as an agent running late, an agent calling in sick, an agent using PTO, or a new high priority task being added.

Create a policy, a grouping of optimization features that run in combination, to define the rules for optimization. Policy objectives prioritize agent task assignment. Policy constraints determine the criteria that need to be met for an assignment group or territory to be assigned a task.

The basic intra-day flow runs every 60 minutes by default, with a minimum option of every 15 minutes. When a trigger condition is met, an intraday event is created. When the next intraday flow runs, an intra-day job is created for each of the groups or territories that have intraday events and those qualifiers are optimized. When optimization is complete and the tasks are updated, the intraday job shows a status of Assignment Complete.

Dispatchers can manually trigger optimization to run from the Dispatcher Workspace when the intraday on demand optimization configuration is enabled and an on demand applicable policy has been added to the scheduling attribute. See [Create a scheduling attribute for Schedule Optimization](configure-scheduling-attributes.md) to add an on demand applicable policy to the configuration.

Note that agent schedules can't be manually updated until intraday optimization is complete.

