---
title: Create an alert correlation rule
description: Create an alert correlation rule to designate primary and secondary alerts. The primary alert is identified as the root cause of the alert group and the secondary alerts are grouped under the primary alert.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Rule-based alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an alert correlation rule

Create an alert correlation rule to designate primary and secondary alerts. The primary alert is identified as the root cause of the alert group and the secondary alerts are grouped under the primary alert.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Alert Correlation Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    For information on the fields, see [Alert correlation rule form](../reference/alert-correlation-rule-form.md).

4.  Select **Submit**.


## Result

A rule-based alert group is created when a new alert is generated or when the status of an existing alert changes from Closed or Flapping to Open or Reopened, provided the filter criteria are matched.

