---
title: Periodically run an event forwarding job
description: Schedule an event forwarding job to periodically send events to all target instances with active event forwarding configurations when the monitoring source can't send events to multiple target instances.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event forwarding, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Periodically run an event forwarding job

Schedule an event forwarding job to periodically send events to all target instances with active event forwarding configurations when the monitoring source can't send events to multiple target instances.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can customize the **event-forwarding** job behavior through related system properties. For more information, see [Event forwarding properties](../reference/event-forwarding-properties-em.md).

**Note:** To minimize the performance impact, the scheduled job sends events not older than the latest hour when it ran for the first time after setting up event forwarding.

## Procedure

1.  Navigate to **All** &gt; **Scheduled jobs** &gt; **Event Management - Event Forwarding Job**.

2.  On the **Scheduled Script Execution** page, select the **Active** check box.

3.  In the **Repeat Interval** field, set the appropriate time interval for the job to run periodically.

    The default value is for the job to run every minute.

4.  Select **Update**.


## Result

The event forwarding job runs periodically based on the repeat interval that you set. Events are sent to all target ServiceNow instances that have active event forwarding configuration records.

If the admin account is disabled, configure the user of the scheduled job. By default, it’s admin, but in this case, it must be changed.

**Note:**

If the event forwarding to the instance failed due to any reason, the **Last Event Forwarding status** field displays `Failed` with a corresponding error message displayed in the **Last Event Forwarding error** field. The target instance generates a self-health monitoring event during the next successful event forwarding indicating the failure of event forwarding for the specified time range.

