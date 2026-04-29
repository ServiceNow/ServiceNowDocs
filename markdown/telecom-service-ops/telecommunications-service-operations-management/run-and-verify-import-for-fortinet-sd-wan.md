---
title: Run and verify an import schedule for Fortinet SGC
description: Manually run a configured import schedule for the Fortinet Service Graph Connector \(SGC\) to verify that data from Fortinet was successfully imported or updated in the Configuration Management Database \(CMDB\). You can also perform the import to validate the connector setup, run one-off imports, or test newly configured connection aliases.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Telecommunications Service Operations Management]
---

# Run and verify an import schedule for Fortinet SGC

Manually run a configured import schedule for the Fortinet Service Graph Connector \(SGC\) to verify that data from Fortinet was successfully imported or updated in the Configuration Management Database \(CMDB\). You can also perform the import to validate the connector setup, run one-off imports, or test newly configured connection aliases.

## Before you begin

Role required: TSOM Visibility admin

If you have configured multiple Fortinet connection aliases for different environments or filters, confirm that the import schedule is set up correctly for each alias.

## About this task

**Note:**

-   If Concurrent Import option is enabled in the import schedule, records are imported into the Concurrent Import Set table instead of the standard Import Set table.
-   Each concurrent job creates its own import set and log entry. The structure of the execution records remains the same.

## Procedure

1.  Navigate to **All** &gt; **Fortinet** &gt; **Import Schedules**.

2.  Select the import schedule that you want to run.

3.  From the list of scheduled data imports, select the scheduled data import.

4.  If the import needs to be run manually rather than having run automatically on a specified schedule, select **Execute now**.

5.  In the Executions related list, verify the import results by selecting the most recent Import Set record created by the execution of the import.

6.  Review the import set log to verify the numbers of rows read, number of rows inserted or updated, or transformation success status, in the CMDB, which indicate that the CIs exist.

    If you delete existing CIs and rerun the import, the log might show multiple inserts and updates, validating end-to-end functionality.


## Result

If configured correctly, the connector brings in the network inventory data from Fortinet into your ServiceNow AI Platform® instance.

**Parent Topic:**[Using Telecommunications Service Operations Management](../concept/using-tsom.md)

