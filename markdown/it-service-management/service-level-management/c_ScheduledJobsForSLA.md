---
title: Scheduled jobs for SLA
description: SLA has default scheduled jobs to regularly refresh the time calculations on each active task SLA.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Scheduled jobs for SLA

SLA has default scheduled jobs to regularly refresh the time calculations on each active task SLA.

-   SLA update \(breach after 30 days\): repeats every 5 days
-   SLA update \(breach within 1 day\): repeats every hour
-   SLA update \(breach within 1 hour\): repeats every 10 minutes
-   SLA update \(breach within 10 min\): repeats every 1 minute
-   SLA update \(breach within 30 days\): repeats every day
-   SLA update \(already breached\): repeats every day

    **Note:** By default, the **SLA update \(already breached\)** scheduled job will calculate either for up to one year after it was breached or if 1000% of its allocated time is breached. You can set this maximum actual elapsed percentage value property in the SLA Engine properties.


Scheduled job runs more frequently when the task SLA is closer to being breached.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

**Related topics**  


[bundle-platadm.c_ScheduleEvents]

[bundle-platadm.t_CreateAScheduledJob]

[SLA engine properties](../task/t_ConfigureSLAProperties.md#)

