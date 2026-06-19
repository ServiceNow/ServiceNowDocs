---
title: Add a default agent work schedule
description: Add a default agent schedule so that agents have a schedule assigned to them if their work schedule expires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-scheduling/add-agent-schedule.html
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assigning tasks using Dynamic Scheduling, Scheduling and dispatching, Use, Field Service Management]
---

# Add a default agent work schedule

Add a default agent schedule so that agents have a schedule assigned to them if their work schedule expires.

## Before you begin

Role required: wm\_dispatcher

The `Allow Dynamic Scheduling to only use work schedule/WFO` system property must be set to `false` before adding a default agent work schedule. Contact your administrator to update this system property. For more information, see [Dynamic scheduling system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/dynamic-sched-system-properties.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dynamic Scheduling Administration** &gt; **Configuration**.

2.  The **Work Order Task Dynamic Scheduling Config** form opens.

3.  Select the Lookup using list icon \(\[Omitted image "lookup-seizmic.png"\] Alt text: lookup icon\).

4.  Select a schedule.

5.  Select **Update**.


