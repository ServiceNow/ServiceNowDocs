---
title: Create anonymization job
description: Configure a data privacy job on your production instance to use anonymized data on your non-production instance for user and data class jobs.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Data anonymization, Platform Privacy]
---

# Create anonymization job

Configure a data privacy job on your production instance to use anonymized data on your non-production instance for user and data class jobs.

## Before you begin

The data privacy job supports two de-identification use cases:

-   Sensitive data of specific sys\_users
-   Sensitive data of particular data class.

Role required: data\_privacy\_processor and admin

## Procedure

1.  Elevate to the **data\_privacy\_processor** role.

    For details on role elevation, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

2.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Anonymization**.

3.  In an Anonymization policy, select **Schedule job** for the policy to be used in the job.

    A policy must be in a published state in order to schedule an anonymization job.

    **Warning:** Anonymization jobs are highly destructive and can only be reversed on rollback. Double check all information, such as records and table processed, before scheduling a job.

4.  In the form, fill in the fields.

<table id="table_tgp_2pb_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy used

</td><td>

Read only name of the selected privacy policy configuration to use for this job. Edit the policy to view additional information about the policy. For detail on privacy policy configurations, see [Create anonymization policies](dps-create-anonymization-policies.md).

</td></tr><tr><td>

Job description

</td><td>

Description of the job.

</td></tr><tr><td>

Start time

</td><td>

The start of the time to run this job in **HH:MM:SS**.

</td></tr><tr><td>

End time

</td><td>

The end of the time window to run this job in **HH:MM:SS**. The end time must be after the start time. The job runs before the time entered in this field. If the job has not yet completed, the job will pause and resume at the next time window start.

</td></tr><tr><td>

Dry Run

</td><td>

Run the job as a test. No records are affected when running this job. Results are displayed in the **Jobs** list, as though the job had executed.**Note:** **Dry Run** must be turned off when configuring a data privacy job with rollback. See [Data privacy job rollback](../../security/reference/data-privacy-job-rollback.md) for details.

</td></tr><tr><td>

Type of user selection

</td><td>

Select either users or groups to be anonymized.

</td></tr><tr><td>

Select users/groups

</td><td>

Select a the specific set of users or groups to be anonymized in this job. Supports up to a maximum of 1000 users.**Note:** This required field displays only when the selected privacy policy condition requires a selection of user records.

</td></tr></tbody>
</table>5.  **Important:** All tables must have a correct sys\_dictionary entry before scheduling and during its job.

    Select **Schedule job** on the form to place the anonymization in the job queue.

    The job runs between the times selected in the **Start time** and **End time** fields. If the job has not completed during the start and end time window, the job will continue at the next time window start.

    **Note:** A job can only be executed once, even if **Dry Run** is selected. To run a job again based on the same policy, select **Schedule job** and complete the form using the same field values.

    The job is listed in the **Jobs** pane.![Shows the jobs listed on the Jobs pane.](../image/jobs-pane.png)

<table id="table_pq3_3fk_dwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the anonymization job.

</td></tr><tr><td>

Description

</td><td>

Description of the anonymization job.

</td></tr><tr><td>

Updated

</td><td>

The date and time that the job was last updated.

</td></tr><tr><td>

State

</td><td>

State of the data privacy job:-   **Scheduled**: Default state for new jobs.
-   **Completed**: The job has successfully anonymized the selected data.
-   **Cancelled**: The job was manually cancelled.
-   **Error**: There was a problem saving the job. Re-schedule the job or create a new job. There may be issues with the configuration if the error continues.
-   **Rollback in progress**: The job has been set to roll back anonymization.
-   **Rollback complete**: The anonymization job rollback has successfully completed.
A read-only field.

</td></tr></tbody>
</table>6.  Select a job from the **Jobs** pane to open the Job summary.

    After a job is scheduled, the **Cancel Job** and **Pause** buttons appear in the Job summary.

<table id="table_em1_zhk_dwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Estimated record count

</td><td>

The estimated number of records this dry-run job affects before being executed. A read-only field

</td></tr><tr><td>

Total data records processed

</td><td>

The total number of individual data records affected by this job. A read-only field.

</td></tr><tr><td>

Total data tables processed

</td><td>

The total number of data tables processed by this job. A read-only field.

</td></tr><tr><td>

Time remaining to rollback

</td><td>

The remaining time that a completed data anonymization job can be rolled back and de-anonymize the data. A read-only field.

</td></tr><tr><td>

Total users processed

</td><td>

The total number of individual user records this job affects. A read-only field.

</td></tr><tr><td>

Cancel job

</td><td>

Select to cancel the anonymization job. This must be selected prior to the job start time.When selected, the job status updates to Cancelled.

</td></tr><tr><td>

Pause

</td><td>

Select to pause the job and rollback recording, if rollback was selected. A warning message will display after a three-day expiry period for rollback contexts.This must be selected after the job start time and before the job end time.

 When selected, the job status updates to Paused.

</td></tr><tr><td>

Resume

</td><td>

Restarts a paused job. Rollback is not supported for resumed jobs if paused. Cancel the job and create a data privacy job. The recording uses an unexpired rollback context.When selected, the job status updates to Scheduled.

</td></tr><tr><td>

Export

</td><td>

Downloads a .PDF file of the data privacy job details.

</td></tr></tbody>
</table>
