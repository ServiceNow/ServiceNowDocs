---
title: Lifecycle event properties
description: Lifecycle event properties control the behavior of lifecycle events. You can set the duration of the activity set closure time in hours.
locale: en-US
release: yokohama
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Lifecycle Events reference, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Lifecycle event properties

Lifecycle event properties control the behavior of lifecycle events. You can set the duration of the activity set closure time in hours.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Properties**.

2.  Update the lifecycle event properties, as appropriate.

<table id="table_tcs_1bq_gjb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_hr\_le.All activity set closure timer

</td><td>

Duration of the activity set closure time in hours and determine when an activity set triggers for a lifecycle event. By default, the time is set to four hours.Use caution if you decide to change the default value. Frequent updates trigger more events and can cause your lifecycle event activity sets to cancel before it can complete.

 **Note:** To trigger an activity set proactively rather than wait for the value entered in this property, see [Lifecycle Events evaluation interval](../concept/le-evaluation-interval1.md).

</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[Lifecycle Events reference](../concept/lifecycle-events-reference.md)

