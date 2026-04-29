---
title: Use SLA timeline to determine business schedule
description: This example demonstrates how to use the SLA timeline to determine the business schedules and business percentage time related to a task SLA.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SLA timeline, Service Level Management reference, Service Level Management, IT Service Management]
---

# Use SLA timeline to determine business schedule

This example demonstrates how to use the SLA timeline to determine the business schedules and business percentage time related to a task SLA.

![SLA Timeline](../image/sla-timeline-determines-business-schedule-1.png "SLA timeline")

In the example above, the business percentage for the priority 2 incident is 0 seconds. The dark stripe in the SLA timeline determines the time when the SLA was out-of-schedule. The SLA time is not calculated during the out-of-schedule time. So, the business elapsed time is 0 since the total duration of this SLA is out of schedule.

If you want more detail of the out-of-schedule duration, you can hover over the dark stripe for summary detail or click it. The Out of Schedule detail section provides information on the details of the schedule such as when the out of schedule started, when it ended, the current duration of that out of schedule time and the total duration of all out of schedule time for the entire SLA. This provides detailed insight into when the SLA was accumulating time and the periods of time it did not accumulated time.

![Out of schedule details](../image/sla-timeline-determines-business-schedule-2.png "Out of schedule details")

Using another example, you can understand in details how business time in an SLA is calculated. In the example below, the total SLA defined duration for Task SLA-2 is 8 hours. The highlighted area shows that the SLA is out of schedule from 07:00AM until 08:00AM and starts accumulating time at 8:00AM reaching 50% of it's total duration at 12:00PM. From 12:00PM to 14:00PM the SLA accumulates from 50 – 75% of it's total duration and from 14:00PM to 16:00PM it accumulates from 75 – 100% of it's total duration, ultimately breaching at 16:00PM.

At any time, you can hover over any stage to get a summary of it's detail or click a stage to get comprehensive detail of that SLA’s stage, including a summary and detail of the stage start and stage end.

![Details of task stage](../image/sla-timeline-determines-business-schedule-3.png "Details of task stage")

**Parent Topic:**[SLA timeline](c_SLATimeline.md)

