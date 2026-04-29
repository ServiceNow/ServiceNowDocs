---
title: Move a resource to a different Unused resources job
description: You can add resources to a currently scheduled job, move resources from one job to another, or remove resources from a job.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage unused resources, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Move a resource to a different Unused resources job

You can add resources to a currently scheduled job, move resources from one job to another, or remove resources from a job.

## Before you begin

Run Discovery on each service account.

Ensure that the Billing Download job has completed for each provider.

Ensure that the Price Sheet Download job has completed for each provider.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\] or insights\_owner \[sn\_clin\_core.insights\_owner\].

## About this task

When you change the resources that are included in a job, the app checks for the following conditions:

-   A resource in the job is owned by another user \(as when a insights\_admin updates a job that was created by an insights\_owner or an insights\_owner updates a job that was created by a different insights\_owner\).
-   The job was created by another user.

If either condition is met, the app sends an email notification to the owner of the resource or the creator of the job.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Unused resources**.

2.  In the list on the appropriate tab, select the check boxes for the resources to terminate.

    -   To create an Unused resources job for resources that are new candidates for termination: On the **New Recommendations** tab, select the resources and then select **Schedule Job**.
    -   To create a job for resources that had previously been scheduled but weren’t resized: On the **Declined Recommendations** tab or the **Failed Recommendations** tab, select the resources and then select **Reschedule**.
    **Note:** Microsoft Azure only: The Azure Advisor service generates the recommendations that appear in Rightsizing and Unused resources reports. Cloud Cost Management doesn't generate the recommendations.

3.  In the dialog box, fill in the fields.

<table id="table_e5m_kw3_ggb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Job Type

</td><td>

Type of job action.Select **Add to job**.

</td></tr><tr><td>

Job name

</td><td>

Unique and descriptive name for the Unused resources job.

</td></tr><tr><td>

Action

</td><td>

The action to take on the selected resources:-   **Power off machine**: Power off triggers a Microsoft Azure process called deallocation to set the resource as Stopped \(Deallocated\).
-   **Terminate machine**: Terminated machines can't be recovered.
-   **Terminate machine and delete storage**: If the root volume isn’t automatically deleted when the VM is terminated, the job deletes the root volume. No other volumes are deleted.

**Note:** Terminated resources or deleted volumes can't be recovered.

</td></tr><tr><td>

Schedule

</td><td>

Date and time to run the Unused resources job.

</td></tr><tr><td>

Approval type

</td><td>

Type of change request to use. Unused Machines operations are directly integrated with the ServiceNow® Change Management feature.

 -   **Auto approval \(Standard Change\)**: Generates and auto-approves a change request to terminate or stop the resource. The system also sends the approved change request to the change group. The resource is added to the list of resources that the job terminates or stops.

-   **Manual approval \(Normal Change\)**: Generates a change request \(Normal Change type\) for a member of the change group to terminate or stop the resource and continues to list the resource in the appropriate Unused Machines reports.

    -   Until a member of the change group approves/rejects the change, the resource state is set to Pending, the resource remains listed on reports, and no other action is taken.
    -   If a member of the change group approves the request, the state is set to **Approved** and the resource is added to the list of resources that the job terminates or stops.
    -   If a member of the change group rejects the request, the resource state is set to **Declined**, the resource remains listed on reports, and no action is taken.


</td></tr><tr><td>

Change template

</td><td>

This field appears only when the **Approval type** is selected as **Auto approval**.

 Change request template \(Standard Change type\) to be used. If no template appears in the list, you must create one. See Create a change request template.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Manage unused resources](../concept/manage-unused-mac.md)

