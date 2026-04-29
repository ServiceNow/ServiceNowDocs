---
title: Configuring Multi-day scheduling
description: Field Service Multi-day task scheduling helps dispatchers manage tasks that require more than a single workday to complete.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configuring Multi-day scheduling

Field Service Multi-day task scheduling helps dispatchers manage tasks that require more than a single workday to complete.

## Configuration overview

As an administrator, you can install the Field Service Multi-Day Task Scheduling application to enable scheduling of work order tasks across multiple days. You can activate the Field Service Multi-Day Task Scheduling plugin \(com.snc.fsm\_multiday\_tasks\) for Field Service.

## Multi-day task scheduling

This system is adept at handling complex tasks that need extended time, verifying that everything is organized and efficient.

-   Agent availability and scheduling: The system checks the availability of agents, their work hours, and even their break times to assign tasks in the most efficient way possible. It supports both manual and dynamic scheduling options along with Schedule Optimization, providing flexibility in how tasks are assigned.
-   Locking in agents for Multi-day tasks: Once an agent is assigned a task that spans multiple days, the system locks the agent's schedule for that duration and no other tasks are assigned to the agent during this time. Even if a higher priority task comes up, the agent remains committed to the multi-day task. This ensures that the multi-day tasks aren’t interrupted, helping to maintain continuity and efficiency until completion.

## Multi-day Task Scheduling

In disaster recovery operations, a cleanup task may require a 20-hour commitment. With multi-day scheduling, the task can be distributed across three days, ensuring that agents aren't overworked or idle, which in turn maximizes productivity and well-being. The agents who are involved in this task are locked and aren't available for other assignments during these three days.

