---
title: Generate reports for attribute value discrepancies
description: Use CMDB 360 to generate reports that highlight discrepancies in attribute values between different discovery sources or between a discovery source and the CMDB baseline.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Telecommunications Service Operations Management]
---

# Generate reports for attribute value discrepancies

Use CMDB 360 to generate reports that highlight discrepancies in attribute values between different discovery sources or between a discovery source and the CMDB baseline.

## Before you begin

Role required: admin

## About this task

Attribute value discrepancy reports help identify conflicting data from multiple sources updating the same configuration item \(CI\). This enables better data quality and integrity across your CMDB.

## Procedure

1.  Navigate to **All** &gt; **CMDB Workspace** &gt; **CMDB 360**.

2.  Select **Create Query**.

3.  In the query type window, select **Compare attribute values**.

4.  Define the query parameters:

    1.  Select **CI Class** you want to analyze \(for example, cmdb\_ci\_computer\).

    2.  Apply filters to narrow the scope \(for example, Discovery source contains "TSOM"\).

    3.  Select attributes to compare values across different discovery sources.

    4.  Choose the sources to compare \(for example, Discovery, SCCM\).

    5.  Select **Compare to CMDB** to compare discovery source data to the current CMDB baseline.

    6.  Click **Save**, provide a name for the query, and then click **Run** to generate the results.

5.  Click **Schedule** to set up the query to run at defined intervals.


## Result

The report displays a comparison of attribute values across sources:

-   Source 1: Current CMDB record.
-   Source 1 Value: Value updated by the most recent discovery source.
-   Source 2: Previous discovery source.
-   Source 2 Value: Value provided by the earlier discovery source.

Each discrepancy is listed as a separate record when a CI has been updated by multiple sources.

**Parent Topic:**[Using Telecommunications Service Operations Management](../concept/using-tsom.md)

**Related topics**  


[Configure attribute value discrepancy in CMDB 360](configure-attribute-value-discrepancy-in-cmdb-360.md)

[Control CI attribute updates using Reconciliation rules](control-ci-attribute-updates-using-reconciliation-rules.md)

