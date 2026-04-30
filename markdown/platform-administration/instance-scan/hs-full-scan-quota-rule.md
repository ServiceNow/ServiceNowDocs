---
title: Implement a scan timeout threshold
description: Set the execution time of a single scan by implementing Transaction Quota Rules. Setting of a quota rule prevents your instance from running a long scan.
locale: en-US
release: yokohama
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Timeout threshold, Configuring Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Implement a scan timeout threshold

Set the execution time of a single scan by implementing **Transaction Quota Rules**. Setting of a quota rule prevents your instance from running a long scan.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Transaction Quota Rules**.

2.  To set a definite execution time, select **Scan timeout**.

3.  Enter the definite execution time in the **Maximum Duration \(seconds\)** field and select **Update**.

    **Note:** The minimum allowed timeout threshold is 5 seconds. If you set the timeout to anything less than 5 seconds, the system still considers it to be 5 seconds. By default, it has been set to 10,800 seconds.

    The scan fails if the execution time exceeds the set timeout. For more information on the type of scan you want to run, see [Configuring Instance Scan](../concept/hs-intro-scans.md) .


