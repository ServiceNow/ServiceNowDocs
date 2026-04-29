---
title: Configure a Data Discovery job
description: Configure a Data Discovery job and review the status of ongoing jobs. A Data Discovery job defines when a pattern is executed on a target table.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Configure a Data Discovery job

Configure a Data Discovery job and review the status of ongoing jobs. A Data Discovery job defines when a pattern is executed on a target table.

## Before you begin

Role required: data\_discovery\_admin

## Procedure

1.  Navigate to **System Security** &gt; **Data Discovery\(Classic\)** &gt; **Data Discovery Job**.

2.  In the Data Discovery Jobs list, select **New**.

3.  On the Data Discovery job fields form, fill in the fields.

<table id="table_tgp_2pb_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the job.

</td></tr><tr><td>

Description

</td><td>

Description of the job.

</td></tr><tr><td>

Scan Type

</td><td>

Number of entries to be scanned. Possible states are as follows:-   **Sample**: Scans 10,000 entries.
-   **Incremental**:Scans for sensitive data patterns in new or modified records. This scan type is recurring.
-   **Full**: Scans all entries.


</td></tr><tr><td>

Policy

</td><td>

The Data Discovery policy to be used in this job. See [Data Discovery policies](../concept/data-discovery-policies.md) for more information.

</td></tr><tr><td>

Scan Attachments

</td><td>

Scans attachments for any sensitive data patterns. Images embedded under .pdf or .doc files will not be scanned for sensitive data.**Warning:** This feature requires sending your data to a controlled ServiceNow environment. Before enabling, please confirm you have agreed to the additional terms and conditions required to use this feature.

</td></tr><tr><td>

Context

</td><td>

Job details about patterns scanned, target tables entries hit, and time elapsed.

</td></tr><tr><td>

State

</td><td>

State of the Data Discovery job. The possible states are as follows:-   **Ready to Schedule**: Default state for new jobs.
-   **Scheduled**: The job is scheduled to run.
-   **In Progress**: Job is actively running.
-   **Completed**: Job has finished running successfully.
-   **Error**: The job has stopped running due to an error.
-   **Canceled**: The job has been canceled.
-   **Paused**: The job is paused.


</td></tr><tr><td>

Summary

</td><td>

Displays the results of the job after you execute it.

</td></tr><tr><td>

Start Date

</td><td>

Sets the start date for the job.

</td></tr><tr><td>

Time window start

</td><td>

The start of the time window to run this job. The job will run after the time entered in this field. The time entered in the **Time window start** field must happen before the time entered in the **Time window end** field.**Note:** A valid time value is in Coordinated Universal Time based on a 24-hour time notation.

</td></tr><tr><td>

Time window end

</td><td>

The end of the time window to run this job. The job runs until the time entered in this field. If the job hasn't complete this time, the job pauses and resumes at the next time window start. The time entered in the **Time window end** field must happen after the time entered in the **Time window start** field.**Note:** A valid time value is in Coordinated Universal Time based on a 24-hour time notation.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The **Schedule Job** and **Update** buttons appear.

5.  Select **Schedule Job** to run your job.

    The job runs between the times selected in the **Time window start** and **Time window end** fields. If the job hasn’t completed during the start and end time window, the job will continue at the next time window start.

6.  Choose one of the following functions:

    -   **Cancel Job**: Cancels the job.
    -   **Pause**: Pauses the job.
    -   **Resume**: Restarts a paused job.

