---
title: Service Level Agreement \(SLA\) processing
description: The SLA engine performs two passes to evaluate SLA definitions and their conditions based on a task.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Service Level Management, IT Service Management]
---

# Service Level Agreement \(SLA\) processing

The SLA engine performs two passes to evaluate SLA definitions and their conditions based on a task.

The SLA engine performs the following passes:

1.  Checks the SLA definitions that do not have an active SLA record associated to the task. The SLA engine determines if the SLA definition applies to the task and if it needs to create a SLA record. The following condition checks are performed:
    1.  If the Start condition is true and the Stop condition is true, do nothing. No SLA record is created, because the Stop condition overrides the Start condition.
    2.  If the Start condition is true and the Stop condition is false, a new SLA record is created for this task using the SLA definition. The SLA record is then set to the In Progress stage.
2.  Checks all active SLA records associated to the task. The engine determines if the SLA records are changing stage. The condition checks are performed in the following order:
    1.  If the Stop condition is true, the SLA changes to **Completed** and becomes inactive.
    2.  If both the Reset and Start conditions are true, the SLA changes to **Completed** and a new task SLA is created.
    3.  If the Start condition is false, the SLA changes to **Cancelled** and becomes inactive.
    4.  If the SLA is active, the Pause condition is true, and the SLA stage is **In Progress**, the SLA is paused.
    5.  If the SLA is active, the Pause condition is false, and the SLA stage is **Paused**, the SLA changes back to **In Progress**.

-   **[Actual and business elapsed times](../reference/r_ElapsedTimeCounting.md)**  
Task SLA records contain two sets of timing information: **Actual elapsed** and **Business elapsed**.

**Parent Topic:**[Exploring Service Level Management](exploring-slm.md)

