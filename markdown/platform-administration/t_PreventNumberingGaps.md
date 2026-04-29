---
title: Prevent numbering gaps
description: By default, numbers are generated every time a new record is created.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Record numbering, Customize, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Prevent numbering gaps

By default, numbers are generated every time a new record is created.

## Before you begin

Role required: admin

## About this task

When records are created but not saved, a gap in the numbering is created. You can prevent these numbering gaps by generating numbers only when records are saved.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System**.

2.  Set the property **Assign a task number only upon insert \(prevents unused numbers\)**, **glide.itil.assign.number.on.insert**, to **true**.

    **Note:** If an insert is aborted, it still consumes a new task number, leading to gaps in the sequence.

3.  Click **Save**.


**Parent Topic:**[Record numbering](../concept/c_ManagingRecordNumbering.md)

