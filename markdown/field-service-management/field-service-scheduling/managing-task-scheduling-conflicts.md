---
title: Managing task scheduling conflicts
description: Some updates to work order tasks \(WOTs\) can cause conflicts when they occur during a scheduled task run. You can use a table to track these scheduling conflicts as they arise. Tracking conflicts helps you monitor and resolve issues efficiently, ensuring that WOTs and agent schedules remain up-to-date and aligned.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Managing task scheduling conflicts

Some updates to work order tasks \(WOTs\) can cause conflicts when they occur during a scheduled task run. You can use a table to track these scheduling conflicts as they arise. Tracking conflicts helps you monitor and resolve issues efficiently, ensuring that WOTs and agent schedules remain up-to-date and aligned.

## Scheduling Methods Included

-   Schedule Optimization
-   Dynamic Scheduling
-   Manual Scheduling
-   Intelligent Task Recommendations
-   Route Optimization

## Conflict Prevention and Warnings Messages

While a WOT is being optimized or scheduled, users receive warning messages while making changes to fields that could impact the scheduling process. These fields include:

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

## Conflict Logging and Resolution

When a work order task \(WOT\) record is updated during a scheduling run, it can cause conflicts. To manage these conflicts effectively, the system logs and captures them in the Work Order Task Scheduling Conflict \[wm\_task\_scheduling\_conflict\] table, ensuring that any issues are documented and can be addressed promptly.

You determine whether the scheduling process must run again based on the new values that were changed while the process was running. For example, if the estimated work duration is changed during a scheduling run, you might decide that:

-   The system should return the WOT with the previous estimated work duration.
-   The scheduling process should be scheduled to run again in X minutes with the new estimated work duration.

