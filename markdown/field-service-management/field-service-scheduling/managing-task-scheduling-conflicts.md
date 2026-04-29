---
title: Managing task scheduling conflicts
description: Some updates to work order tasks \(WOTs\) can cause conflicts when they occur during a scheduled task run. You can use a table to track these scheduling conflicts as they arise. Tracking conflicts helps you monitor and resolve issues efficiently, ensuring that WOTs and agent schedules remain up-to-date and aligned.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Managing task scheduling conflicts

Some updates to work order tasks \(WOTs\) can cause conflicts when they occur during a scheduled task run. You can use a table to track these scheduling conflicts as they arise. Tracking conflicts helps you monitor and resolve issues efficiently, ensuring that WOTs and agent schedules remain up-to-date and aligned.

## Conflict Logging and Resolution

When a WOT record is updated during a scheduling run, the update can cause a conflict. The system logs and captures conflicts in the Work Order Task Scheduling Conflict \[wm\_task\_scheduling\_conflict\] table so that issues are documented and can be addressed promptly.

You determine whether the scheduling process must run again based on the values that changed while the process was running. For example, if the estimated work duration changes during a scheduling run, you might decide that:

-   The system should return the WOT with the previous estimated work duration.
-   The scheduling process should run again in X minutes with the new estimated work duration.

## Scheduling Methods Included

-   Schedule Optimization
-   Dynamic Scheduling
-   Manual Scheduling
-   Intelligent Task Recommendations
-   Route Optimization

## Conflict field configuration

The fields considered for conflict capture are configured using the Application Common Field Set. For each field in the field set, the Always Show attribute determines whether that field is included in conflict tracking. When Always Show is set to true, the field is considered during conflict capture. When set to false, it is not. To configure which fields are considered in conflict tracking, see [Configure task scheduling conflict triggers](../task/task-scheduling-conflict-triggers.md).

## Conflict Prevention and Warnings Messages

While a WOT is being optimized or scheduled, users receive warning messages while making changes to fields that can impact the scheduling process. These fields include:

-   Estimated work duration: The expected time required to complete the task.
-   Task skills: The specific skills required to perform the task.
-   Priority: The urgency or importance of the task.
-   Location: The physical location where the task must be performed.
-   Value: The importance or value of the task.
-   Penalty: The penalty associated with not completing the task on time.
-   Preferred/Secondary/Excluded Technician: The technicians who are preferred, secondary, or are excluded for the task.
-   Agent shift: The shift during which the agent is available.
-   Agent skills: The skills possessed by the agent.
-   Agent skill levels: The proficiency levels of the agent's skills.
-   Agent location: The physical location of the agent.

