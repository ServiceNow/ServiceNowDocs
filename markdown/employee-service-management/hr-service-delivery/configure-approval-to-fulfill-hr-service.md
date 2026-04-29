---
title: Configure an approval
description: Configure a service activity that is an approval. Approvals require one or more users to approve the case before it can proceed.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a service activity for an HR service, Configure an HR service, HR service configuration, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure an approval

Configure a service activity that is an approval. Approvals require one or more users to approve the case before it can proceed.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  On the Service Activity form, set the **Activity type** field to `Approval`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_cbs_4ml_mfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity type

</td><td>

Set the value to **Approval**.

</td></tr><tr><td>

Name

</td><td>

Name of the service activity.

</td></tr><tr><td>

Missing any approver

</td><td>

Select one of the following actions for when any approver is missing:-   Select replacements
-   Skip missing
-   Close incomplete


</td></tr><tr><td>

Missing all approvers

</td><td>

Select one of the following actions for when all approvers are missing:-   Select replacements
-   Close incomplete


</td></tr><tr><td>

Wait for

</td><td>

Select one of the following actions for when an approval is completed:-   Anyone to approve
-   Everyone to approve
-   First response from anyone


</td></tr><tr><td>

On rejection

</td><td>

Select one of the following actions for when an approval is rejected:-   Allow resubmit of approvals

**Note:** When an approval is rejected, the **Assigned to** user for the case can submit another request for approval with work notes or comments. See [Resubmit an HR case for approval](t_ApproveAnHRCase.md).

-   Close incomplete
 **Note:** To reject an approval, users should have the HR case writer \[sn\_hr\_core.case\_writer\] role.

</td></tr><tr><td>

Parent HR service

</td><td>

This field is automatically set to the parent HR service.

</td></tr><tr><td>

Order

</td><td>

Order number for when the service activity is made available. Lower numbered service activities are made available before higher numbered service activities.**Note:**

-   The current service activity must be closed, completed, accepted, or rejected before the next service activity is made available.
-   Service activities with identical order numbers are made available at the same time.


</td></tr><tr><td>

Approvers from case

</td><td>

User fields from the HR case to approve the task.

</td></tr><tr><td>

Approver users

</td><td>

Users to approve the task.

</td></tr><tr><td>

Approver groups

</td><td>

Groups to approve the task.

</td></tr></tbody>
</table>3.  Click **Submit** or **Update** on the Service Activity form.

4.  Click **Update** on the HR Service form.


**Parent Topic:**[Configure a service activity for an HR service](configure-service-activity-for-hr-service.md)

