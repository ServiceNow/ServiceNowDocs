---
title: Move a resource to a different Rightsizing job
description: You can add resources to a currently scheduled job, move resources from one job to another, or remove resources from a job.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resize resources with Rightsizing, Use, Cloud Cost Management, IT Asset Management]
---

# Move a resource to a different Rightsizing job

You can add resources to a currently scheduled job, move resources from one job to another, or remove resources from a job.

## Before you begin

Run Discovery on each service account.

Ensure that the Billing Download job has completed for each provider.

Ensure that the Price Sheet Download job has completed for each provider.

Role required: insights\_admin or insights\_owner

## About this task

When you change the resources that are included in a job, the app checks for the following conditions:

-   A resource in the job is owned by another user \(as when a insights\_admin updates a job that was created by an insights\_owner or an insights\_owner updates a job that was created by a different insights\_owner\).
-   The job was created by another user.

If either condition is met, the app sends an email notification to the owner of the resource or the creator of the job.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Rightsizing**.

2.  In the list on the appropriate tab, select the check boxes for the resources to rightsize.

    -   On the **New Recommendations** tab, select **Schedule**.
    -   On the **Declined Recommendations** tab or the **Failed Recommendations** tab, select **Reschedule**.
3.  In the dialog box, fill in the fields.

<table id="table_e5m_kw3_ggb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Job type

</td><td>

Type of job action. Select **Add to job**.

</td></tr><tr><td>

Job name

</td><td>

Unique and descriptive name for the Rightsizing job.

</td></tr><tr><td>

Schedule

</td><td>

Date and time to run the Rightsizing job.

</td></tr><tr><td>

Approval type

</td><td>

Type of change request to use.

 -   **Auto approval**: Generates and auto-approves a change request to resize the resource. The system also sends the approved change request to the change group. The resource is added to the list of resources that the job will resize.
-   **Manual approval**: Generates a change request \(Normal Change type\) for a member of the change group to resize the resource and continues to list the resource in the appropriate Rightsizing reports.


</td></tr><tr><td>

Change template

</td><td>

This field appears only when the **Approval type** is selected as **Auto approval**.

Change request template \(Standard Change type\) to be used. If no template appears in the list, you must create one. See [Create a change request template](https://www.servicenow.com/docs/access?context=create-a-change-request-template&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Resize resources with Rightsizing](../concept/resize-res-ci.md)

