---
title: Schedule resources to be rightsized
description: To rightsize a resource, add it to a Rightsizing job and specify when the job should run. You can also move resources out of one scheduled job into a different job or remove a resource from a job.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Resize resources with Rightsizing, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Schedule resources to be rightsized

To rightsize a resource, add it to a Rightsizing job and specify when the job should run. You can also move resources out of one scheduled job into a different job or remove a resource from a job.

## Before you begin

Run Discovery on each service account.

Ensure that the Billing Download has completed for each provider.

Ensure that the Price Sheet Download job has completed for each provider.

Role required: insights\_admin or insights\_owner

## About this task

When you change the resources that are included in a job, Cloud Cost Management checks for the following conditions:

-   A resource in the job is owned by another user \(as when a insights\_admin updates a job that was created by an insights\_owner or an insights\_owner updates a job that was created by a different insights\_owner\).
-   The job was created by another user.

If either condition is met, the app sends an email notification to the owner of the resource or the creator of the job.

**Note:** If a recommendation to rightsize a Google Cloud resource is dismissed from the Google Cloud management portal, the resource doesn't appear in Rightsizing recommendations.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Rightsizing**.

2.  In the list on the appropriate tab, select the check boxes for the resources to rightsize.

    -   To create a Rightsizing job for resources that are new candidates for rightsizing: On the **New Recommendations** tab, select resources and then select **Schedule**.
    -   To create a new job for resources that had previously been scheduled but were not resized: On the **Declined Recommendations** tab or the **Failed Recommendations** tab, select resources and then select **Reschedule**.
3.  In the dialog box, fill in the fields.

<table id="table_e5m_kw3_ggb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Job type

</td><td>

Type of job action.Select **Schedule job**.

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

**Note:**

The **Short description**, **Description**, **Assignment group**, and **Affected CIs** fields are auto populated. For more information, see [Create a change request](https://www.servicenow.com/docs/access?context=t_CreateAChange&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Change template

</td><td>

This field appears only when the **Approval type** is selected as **Auto approval**.

Change request template \(Standard Change type\) to be used. If no template appears in the list, you must create one. See Create a change request template.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The Rightsizing job is created and will run at the scheduled time.

-   Until a member of the change group approves or rejects the change, the resource state is set to **Pending**, the resource remains listed on reports, and no other action is taken.
-   If a member of the change group approves the request, the state is set to **Approved** and the resource is added to the list of resources that the job will resize.
-   If a member of the change group rejects the request, the resource state is set to **Declined**, the resource remains listed on reports, and no action is taken.

**Parent Topic:**[Resize resources with Rightsizing](../concept/resize-res-ci.md)

**Related topics**  


[Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

[Standard change catalog](https://www.servicenow.com/docs/access?context=c_StandardChangeCatalogPlugin&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

[bundle-itsm.create-a-change-request-template]

[Exclude a resource from all Cloud Cost Management reports](exclusion-list-add-to-cloudin.md)

