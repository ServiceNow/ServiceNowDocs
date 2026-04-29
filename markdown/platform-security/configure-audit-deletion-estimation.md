---
title: Enable an audit deletion estimate
description: Enable the audit deletion estimation feature that calculates the approximate number of records that will be deleted based on retention policies. This information helps you make an informed decision before applying a retention policy, which permanently deletes audit data and cannot be reversed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Audit Management Console, Configuring auditing for a table, Auditing]
---

# Enable an audit deletion estimate

Enable the audit deletion estimation feature that calculates the approximate number of records that will be deleted based on retention policies. This information helps you make an informed decision before applying a retention policy, which permanently deletes audit data and cannot be reversed.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  Set the relevant system properties.

    |Name|Value|
    |----|-----|
    |com.glide.stats.table\_stats.data\_source|information\_schema|
    |com.glide.stats.storage\_disk\_usage.information\_schema|true|

3.  Select **Submit**.


## Result

The estimated number of records to be deleted appears in the **Retention** tab of the Audit Management Console.

