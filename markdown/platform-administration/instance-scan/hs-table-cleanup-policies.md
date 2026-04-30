---
title: Instance Scan table cleanup policies
description: Instance Scan offers table cleanup policies to erase previous scan results.
locale: en-US
release: yokohama
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Instance Scan table cleanup policies

Instance Scan offers table cleanup policies to erase previous scan results.

The cleanup policies are based on the time that the scans are created. The timer starts when you run a scan. **Table Cleanup** is run against the Auto Flushes \[sys\_auto\_flush\] table and cleans up the previous scan results.

-   If the result records are older than 90 days \(**7,776,000** seconds\), the first policy clears all scan result records and related records.
-   If the following conditions are true, the second policy deletes all scan result records and related records.
    -   The **Scan type** is **Test Scan**.
    -   The records are older than 14 days, and **Age in seconds** is equal to or greater than **1,209,600** seconds.

You can also modify these policies by entering any customized time period. See [Customize table cleanup policies](../task/hs-customize-table-cleanup-policies.md) for more information.

