---
title: Create a check
description: Create your own checks by implementing the following procedure.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Instance Scan, Maintain and monitor, Administer]
---

# Create a check

Create your own checks by implementing the following procedure.

## Before you begin

Role required: scan\_admin

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Checks**.

2.  Select **New** from the Checks context menu.

    The Check Interceptor list appears.

3.  Select one of the available types of checks.

    See [Check types](../concept/hs-intro-health-check.md#hs-health-check-types) for more information.

    **Note:** If you want to update an existing check, the **Version** field increments itself. The new version provides you a change history. You can also know which particular version of the check ran with a given scan.


-   **[Create a table type check](hs-create-table-health-check.md)**  
Create a check by selecting **Create a new Table Check** if you know which specific table and conditions you want to test. This check type is applied on only one table at a time. You can also include your own script for more complex capabilities by selecting the **Advanced** option on the form.
-   **[Create a column type check](hs-create-column-health-check.md)**  
Retrieve all records containing a specific column field type from all tables in an instance by selecting **Create a new Column Type Check**. The **Column Type Check** type implements the rule you created to iterate all records matching the target column field type.
-   **[Create a script only check](hs-create-script-health-check.md)**  
Create a check without specifying a table or a column type by selecting **Create a new Script Only Check**. You can verify meta data, configurations, and execute complex checks by writing your own script.
-   **[Create a linter check](hc-linter-check.md)**  
Create a linter check to identify any issues in a script. When a linter check is run on a record, an abstract syntax tree for its code is generated. You can use the abstract syntax tree to analyze issues with the code.

**Parent Topic:**[Using Instance Scan](../concept/hs-using-scans.md)

**Related topics**  


[Create a check suite](hc-create-check-suite.md)

[Executing a scan](../reference/hs-execute-scans.md)

[Schedule a full scan](hs-schedule-full-scan.md)

[Schedule a suite scan](hc-schedule-suite-scan.md)

[Monitoring a scan](hs-progress-status-full-scan.md)

[Reviewing of scans](../reference/hs-review-scans.md)

[Queue your scan](hs-queue-scan.md)

[Cancel a scan](hs-cancel-scan.md)

[Using the Instance Scan dashboard](hs-implement-dashboard.md)

