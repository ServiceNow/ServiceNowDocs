---
title: Configure a data privacy job
description: Configure a data privacy job on your production instance to use anonymized data on your non-production instance for user and data class jobs.
locale: en-US
release: zurich
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Data privacy \(Classic\) configuration, Data privacy \(Classic\), Data Privacy, Platform Privacy]
---

# Configure a data privacy job

Configure a data privacy job on your production instance to use anonymized data on your non-production instance for user and data class jobs.

## Before you begin

The data privacy job supports two de-identification use cases:

-   Sensitive data of specific sys\_users
-   Sensitive data of particular data class.

Role required: data\_privacy\_processor and admin

## Procedure

1.  Elevate to the **data\_privacy\_processor** role.

    For details on role elevation, see [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Data Privacy Job**.

3.  In the Data Privacy Jobs list, click **New**.

4.  In the form, fill in the fields.

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

Privacy Configuration

</td><td>

The privacy policy configuration to use for this job. For detail on Privacy policy configurations, see [Create a data privacy policy](config-dp-policy.md).

</td></tr><tr><td>

Frequency

</td><td>

-   **Run Once**: The job will run once in the specified time window.
-   **Weekly**: The job will run each day of the **Day of the week** field in the specified time window.
-   **Monthly**: The job will run each day of month as entered in the **Day of the month** field in the specified time window.


</td></tr><tr><td>

Users

</td><td>

Select the users or group of users to be anonymized in this job. Up to 1000 users of a group can be processed.**Note:** This field displays only when the selected privacy policy condition requires a selection of user records.

</td></tr><tr><td>

Dry Run

</td><td>

Run the job as a test. No records are affected when running this job. Results are displayed in the **Summary** field as though the job had executed.**Note:** **Dry Run** must be turned off when configuring a data privacy job with rollback. See [Roll back a data privacy job](rollback-data-privacy-job.md) for details.

</td></tr><tr><td>

State

</td><td>

State of the data privacy job:-   **Completed**: Job completed successfully.
-   **Ready to Schedule**: Default state for new jobs.
-   **Rollback in progress**: The job has been set to roll back anonymization.
-   **Rollback complete**: The anonymization job rollback has successfully completed.
-   **Completed with Errors**: The job completed but has errors. See [Data Privacy Job Logs](dp-job-logs.md) for more information.
-   **Error**: Job did not complete and had an error. See [Data Privacy Job Logs](dp-job-logs.md) for more information
A read-only field.

</td></tr><tr><td>

Estimated record count

</td><td>

The estimated number of records this job affects. A read-only field.

</td></tr><tr><td>

Summary

</td><td>

A read-only field that displays the results of the job when you execute it.

</td></tr><tr><td>

Time window start

</td><td>

The start of the time window to run this job. The job will run after the time entered in this field. A valid time value is in Coordinated Universal Time based on a 24 hour time notation.

</td></tr><tr><td>

Time window end

</td><td>

The end of the time window to run this job. The job runs before the time entered in this field. If the job has not yet completed, the job will pause and resume at the next time window start. The end time must be after the start time.A valid time value is in Coordinated Universal Time based on a 24 hour time notation.

</td></tr></tbody>
</table>5.  Right-click the form header and select **Save** from the context menu.

    After saving the record, the **Schedule Job** and **Delete Job** buttons appear.

6.  Click **Schedule Job** to run your job.

    The job runs between the times selected in the **Time window start** and **Time window end** fields. If the job has not completed during the start and end time window, the job will continue at the next time window start.

    **Note:** A job can only be executed once, even if **Dry Run** is selected. To run the same job again, create a data privacy job using the same field values.

7.  Choose one of the following functions:

    -   **Cancel Job**: Cancels the data privacy job.
    -   **Pause**: Pauses job and rollback recording, if rollback has been selected. A warning message will display after a three-day expiry period for rollback contexts. See [Roll back a data privacy job](rollback-data-privacy-job.md) for details.
    -   **Resume**: Restarts a paused job. Rollback is not supported for resumed jobs if paused. Cancel the job and create a data privacy job. The recording uses an unexpired rollback context.

