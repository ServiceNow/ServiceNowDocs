---
title: SLA duration and schedules
description: Schedules have an impact on the duration specified in an SLA definition.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# SLA duration and schedules

Schedules have an impact on the duration specified in an SLA definition.

This impact is reflected in the timings that are taken into consideration while calculating an SLA.

**Note:** If a schedule is not selected for an SLA, the SLA will run 24X7.

Consider a scenario where you select a duration of one day, which is 24 hours, and a schedule of 9 am to 5 pm, which is 8 hours. The SLA calculation will distribute the 24 hours across three working days of 8 hours each. So a team working on a task associated with this SLA has 3 days to complete the task before the SLA is breached.

![Time distribution](../image/SLM_SchDur.png "Time distribution")

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

