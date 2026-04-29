---
title: Scanning with Granular Configuration
description: Granular scan can be used to scan specific table columns for discovery. Traditional Data Discovery jobs scan the entire table to discover data, whereas granular scan targets specific columns of the table thereby offers more control over the discovery process
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Scanning with Granular Configuration

Granular scan can be used to scan specific table columns for discovery. Traditional Data Discovery jobs scan the entire table to discover data, whereas granular scan targets specific columns of the table thereby offers more control over the discovery process

## Before you begin

Role required: admin, sn\_data\_discovery\_admin, data\_privacy\_admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Data Discovery\(Classic\)** &gt; **Granular configuration**.

2.  In the **Granular Configurations** list, select **New**.

3.  In the **Granular Configuration** fields form, fill in the fields.

<table id="table_tgp_2pb_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dictionary Entry

</td><td>

Column to be scanned.

</td></tr><tr><td>

Table

</td><td>

Table to be scanned.

</td></tr><tr><td>

Column label

</td><td>

Label of column to be scanned

</td></tr><tr><td>

Scan start point

</td><td>

Sensitive data will only be discovered for the day of and after the scan start point.**Note:** If the scan start point is left empty, all entries in the column will be scanned. If scan start point is changed, the scanning will be reset to start from the newly configured timestamp.

</td></tr><tr><td>

Active

</td><td>

Check to activate the granular configuration.

</td></tr></tbody>
</table>4.  Select **Submit**.

    Children of extensible tables may be selected for configuration.

5.  Select the Granular Configuration for the parent table, select **Select Child Tables** and select child tables for scanning.


## Result

The specific column of the target table will be scanned for discovery. Granular Scan makes use of [Data patterns](configure-data-discovery-patterns.md) from **Active Data Patterns**. You can review the findings and take action at **All** &gt; **System Security** &gt; **Data Discovery\(Classic\)** &gt; **Granular findings**. See [Granular Findings](../concept/granular-findings.md) for more information.

