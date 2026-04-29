---
title: Set the purge period for records of exporter executions
description: Change the default deletion period. By default, records of exporter executions are deleted after a period of three years.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export a snapshot, Using DevOps Config, DevOps Config, IT Service Management]
---

# Set the purge period for records of exporter executions

Change the default deletion period. By default, records of exporter executions are deleted after a period of three years.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: CDM Admin \[sn\_cdm.cdm\_admin\]

## Procedure

1.  Navigate to **All** &gt; **System Maintenance** &gt; **Table Cleanup**.

2.  In the **Tablename** column, select **sn\_cdm\_exporter\_execution**.

3.  Change the **Age** setting to the retention period in seconds and then save the record.

    Minimum: 1 year. For example:

    -   1 year = 31 536 000
    -   2 years = 63 072 000
    -   3 years = 94 608 000

