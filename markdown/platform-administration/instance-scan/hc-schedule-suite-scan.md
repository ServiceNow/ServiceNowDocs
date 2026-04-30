---
title: Schedule a suite scan
description: Create a schedule to regularly trigger a suite scan even when you don’t have an active session.
locale: en-US
release: yokohama
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Schedule a suite scan

Create a schedule to regularly trigger a suite scan even when you don’t have an active session.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Suites**.

    A list of suites displays.

2.  Select a suite from the list to schedule a suite scan.

3.  Select Schedule related list.

    A list of scheduled scans displays.

4.  Select **New** to create a schedule for the suite scan.

    The **Schedule Suite Scan** modal displays.

5.  Select a target for the scan.

    -   **Full Instance**: Scans all the available records in the instance.
    -   **Scoped App**: Scans selected scoped apps. You can select multiple scoped apps.
    -   **Update Set**: Scans multiple update sets.
6.  Select **Schedule Scan**.![Image showing Schedule Suite Scan modal](../image/hc-schedule-suite-scan.png)

    **Note:** If a record is inactive, the checks don't generate any findings for that record.

    The **Scheduled Scan** form displays.

7.  On the form, fill in the fields.

<table id="table_rrj_m3k_gnb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the scheduled scan.

</td></tr><tr><td>

Application

</td><td>

Application that has the record.

</td></tr><tr><td>

Combo

</td><td>

References a record which has a list of sources and a list of targets to run the scan against.

</td></tr><tr><td>

Run

</td><td>

Frequency at which the scan should be scheduled to run.-   Daily: Scan is scheduled to run daily.

Time: The time at which the scan is scheduled to start daily.

-   Weekly: Scan is scheduled to run weekly.
    -   Day: The day in the week on which the scan is scheduled to start weekly.
    -   Time: The time at which the scan is scheduled to start.
-   Monthly: Scan is scheduled to run monthly.
    -   Day: The day in the month on which the scan is scheduled to start monthly.
    -   Time: The time at which the scan is scheduled to start.
-   Periodically: Scan is scheduled to run periodically.
    -   Starting: Date and time at which the scan is scheduled to start.
    -   Repeat interval: Date and time at which the scan has been scheduled to repeat.
-   Once: Date and time at which the scan is scheduled to start.
-   On Demand: Scan is not scheduled to run and runs only manually when **On Demand** option is chosen for the **Run** field.
-   Business Calendar: Business calendar time of the user to schedule the scan run either at the beginning of that period or at the end, depending on their selection.


</td></tr><tr><td>

Active

</td><td>

Option to activate the record.

</td></tr><tr><td>

Conditional

</td><td>

Option to write your own script condition, which is always verified before scheduled scan runs.

</td></tr><tr><td>

Run as

</td><td>

User role used to run the scan.

</td></tr><tr><td>

Run as tz

</td><td>

Timezone used to run the scan.

</td></tr></tbody>
</table>8.  Select **Submit**.

    The scan that has been scheduled displays under Schedule related list.


**Parent Topic:**[Using Instance Scan](../concept/hs-using-scans.md)

**Related topics**  


[Create a check](hs-create-health-check.md)

[Create a check suite](hc-create-check-suite.md)

[Executing a scan](../reference/hs-execute-scans.md)

[Schedule a full scan](hs-schedule-full-scan.md)

[Monitoring a scan](hs-progress-status-full-scan.md)

[Reviewing of scans](../reference/hs-review-scans.md)

[Using the Instance Scan dashboard](hs-implement-dashboard.md)

