---
title: Run and verify import for Nokia Altiplano Service Graph Connector
description: Manually execute a configured import schedule for the Nokia Altiplano Service Graph Connector. You can also execute the import to validate the connector setup, run ad-hoc imports, or test newly configured connection aliases. This task helps ensure that data from Altiplano is successfully imported or updated in the CMDB.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Telecommunications Service Operations Management]
---

# Run and verify import for Nokia Altiplano Service Graph Connector

Manually execute a configured import schedule for the Nokia Altiplano Service Graph Connector. You can also execute the import to validate the connector setup, run ad-hoc imports, or test newly configured connection aliases. This task helps ensure that data from Altiplano is successfully imported or updated in the CMDB.

## Before you begin

Role required: TSOM Visibility admin

## About this task

After configuring the Nokia Altiplano Service Graph Connector and setting up one or more import schedules, you can execute an import job. This task helps you verify that the integration is working as expected and that CIs are successfully imported or updated in the CMDB.

You can either enable the import schedules to run automatically based on their defined frequency, or trigger them manually for immediate execution and validation.

**Note:** If you have configured multiple Altiplano connection aliases \(for different environments or filters\), confirm that the import schedule is set up correctly for each alias.

The following screenshot helps you understand the scheduled data import process and displays the executions in the form of import sets.

![Scheduled data import screen of Nokia Altiplano bulk discovery and the list of executions.](../images/scheduled-data-import.png)

## Procedure

1.  Navigate to **All** &gt; **Nokia Altiplano** &gt; **Import Schedules**.

2.  Select the import schedule that you want to run.

    The list of scheduled data imports appear.

3.  Select the scheduled data import.

4.  Do one of the following:

    -   If the schedule is **Active**, the job runs automatically at the defined interval. So wait until it’s executed.
    -   Select **Execute Now** to run the import immediately.
5.  To monitor the execution and verify results:

    1.  Scroll down to the **Executions** list or the table linked to the import schedule.

    2.  Open the most recent **Import Set** record created by the execution.

6.  Review the import set log to verify the numbers of rows read, number of rows inserted or updated in the CMDB, or transformation success status.

7.  Navigate to **All** &gt; **CMDB** &gt; **CI Classes** or your custom telecom tables \(such as TNI base item\) to confirm the CIs were created or updated as expected.


## Result

The import schedule runs immediately, and you can verify the import set execution and the corresponding CI updates in the CMDB. If configured correctly, the connector brings in the network inventory data from Nokia Altiplano into your ServiceNow instance.

Example: After executing the import schedule:

-   The log shows: “12 rows read, 0 inserted/updated.” This indicates that CIs exist.
-   If you delete existing CIs and rerun the import, the log might show multiple inserts and updates, validating end-to-end functionality.

**Note:**

-   If **Concurrent Import** option is enabled in the import schedule, you’ll see records in the **Concurrent Import Set** table instead of the standard Import Set table.
-   Each concurrent job creates its own import set and log entry. The structure of the execution records remains the same.

**Parent Topic:**[Using Telecommunications Service Operations Management](../concept/using-tsom.md)

**Related topics**  


[Configure Nokia Altiplano service graph connector](../concept/configuring-service-graph-connector-nokia-altiplano.md)

[Telecom Discovery via Nokia Altiplano](../concept/service-graph-connector-for-nokia-altiplano.md#)

