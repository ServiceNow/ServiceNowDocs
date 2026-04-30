---
title: Create a Workplace service activity
description: Create a Workplace service activity to trigger a background activity when a Workplace service is selected. The activity can be an approval action, task, or a child case.
locale: en-US
release: xanadu
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create a Workplace service, Configure Workplace Case Management, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create a Workplace service activity

Create a Workplace service activity to trigger a background activity when a Workplace service is selected. The activity can be an approval action, task, or a child case.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

Ensure that you have the following details:

-   Task templates and Case templates to link to a workplace service activity.
-   A workplace service with fulfillment type selected as **Service activity**. For more information, see [Create a Workplace service](create-workplace-service.md).

## About this task

Activities can be approvals, tasks, or child cases. You can specify the order in which these activities must be triggered.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Workplace services**.

2.  Select the workplace service that you want to modify to add more workplace service activities.

3.  Click **New** under the **Workplace Service Activities** section in the **Workplace services** form.

4.  On the form, fill in the fields.

<table id="table_ews_1x4_smb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the service activity.

</td></tr><tr><td>

Activity type

</td><td>

Select the type of service activity that you want to create:-   **Approval**: Creates an approval activity.
-   **Task**: Creates a task activity.
-   **Child case**: Creates a child workplace case.
-   **Execute service item**: Executes the tasks or cases created for workplace service items ordered by an employee along with the workplace service. For more information, see [Add a workplace service item to a workplace service](add-workplace-service-items.md).
-   **Automated task**: Creates an automated task that will be closed without any manual intervention.


</td></tr><tr><td>

Missing all approves

</td><td>

This field appears if you select the **Activity type** **Approval**. From the list of options, select what action to take if all the approvers are missing.

</td></tr><tr><td>

Wait for

</td><td>

This field appears if you select the **Activity type** **Approval**. Select the type of approval required to close the case. From the options, select whether any approver can approve, all approvers must approve, or if the first response from any approver is an approval. Point to the options to view more details.

</td></tr><tr><td>

Application

</td><td>

This field is auto-generated. However, ensure that **Workplace Case Management** is selected.

</td></tr><tr><td>

Parent service

</td><td>

This field is auto-populated with the Workplace service to which you are adding this activity.

</td></tr><tr><td>

Order

</td><td>

Specify an order for this activity. Depending on the order, the service activity initiated. **Note:** You can specify only one Service Activity of type **Approval** in a single order.

</td></tr><tr><td>

Approvers

</td><td>

This field appears if you select the **Activity type** **Approval**. Select approvers for the case from the configured performer criteria. Click the unlock icon \(![Approvers from case unlock icon](../../wsd-reservation-management/image/unlock-icon.png) \) to select.

</td></tr><tr><td>

Workplace case service

</td><td>

This field appears if you select the **Activity type** as **Child case**. Click the search \(![Workplace case service search icon](../image/search-icon.png)\) icon and select the Workplace service you want to set as a child case. To add a Workplace service, see [Create a Workplace service](create-workplace-service.md).

</td></tr><tr><td>

Continue if incomplete

</td><td>

Select this option if you want this activity to continue even if the activity is closed or incomplete.

</td></tr></tbody>
</table>5.  Enter the conditions in the condition builder that you want to trigger the background activity.

    For example, a task for the activity will be created only when the condition matches the case record.

    In releases prior to the Quebec release, fields had to be selected from the Workplace Case \[sn\_wsd\_case\_workplace\_case\] table and service catalog variables such as questions could not be referenced.

6.  Click **Submit**.


## Result

The Workplace Service Activity is created and will be executed when the parent Workplace service is requested.

**Parent Topic:**[Create a Workplace service](create-workplace-service.md)

