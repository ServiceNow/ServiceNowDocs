---
title: Create granular job
description: Scan specific table columns in Data Discovery Store.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Discovery scheduled discovery, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Create granular job

Scan specific table columns in Data Discovery Store.

## Before you begin

Role required: discovery.admin

## Procedure

1.  Navigate to **All** &gt; **Data Discovery** &gt; **Scheduled Discovery**.

2.  Select **Granular Configuration** in the right side navigation pane.

3.  Select **Create new**.

4.  Fill in the form.

<table id="table_ukw_qjg_cgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table to be scanned

</td></tr><tr><td>

Column label

</td><td>

The column to be scanned

</td></tr><tr><td>

Scan start point

</td><td>

Sensitive data will only be discovered for the day of and after the scan start point.**Note:** If the scan start point is left empty, all entries in the column will be scanned. If scan start point is changed, the scanning will be reset to start from the newly configured timestamp.

</td></tr></tbody>
</table>5.  Set **Active** slider.

6.  Select **Save**.


## Result

A granular scan is scheduled to run on the target table and column, after it executes you can [review the scan findings](dds-review-granular-findings.md).

