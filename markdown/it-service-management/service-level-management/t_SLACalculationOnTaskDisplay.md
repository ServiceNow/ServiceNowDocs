---
title: Recalculate SLA times automatically
description: By default when a user opens a task, the SLA timing information for that task is not automatically recalculated.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SLA calculation, Using Service Level Management, Service Level Management, IT Service Management]
---

# Recalculate SLA times automatically

By default when a user opens a task, the SLA timing information for that task is not automatically recalculated.

## Before you begin

Role required: admin

## About this task

You can enable this information to be automatically recalculated each time the task is opened, to provide current information rather than information from the last scheduled job.

## Procedure

1.  Go to **Service Level Management** &gt; **Properties** &gt; **SLA Engine**.

2.  For the **Recalculate Task SLA records when a task's form is displayed** property, select the **Yes** check box.

    **Note:** This property is disabled by default because there is a potential performance impact when several users concurrently open tasks.

3.  Click **Save**.


**Parent Topic:**[SLA calculation](../reference/r_SLAAutomation.md)

