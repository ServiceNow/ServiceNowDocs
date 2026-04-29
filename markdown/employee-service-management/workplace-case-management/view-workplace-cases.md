---
title: View and track workplace cases
description: View and track open, closed, and unassigned workplace cases.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 5
breadcrumb: [Manage, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# View and track workplace cases

View and track open, closed, and unassigned workplace cases.

## Before you begin

Role required: sn\_wsd\_case.admin, sn\_wsd\_case.manager, sn\_wsd\_case.case\_reader

## About this task

You can view any workplace case when required.View the details provided by the user in the Variables section of the workplace case.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Cases**.

2.  Select any of the following options to view workplace cases:

    -   **Assigned to me**: Select this option to view workplace cases assigned to you.
    -   **Assigned to my group**: Select this option to view workplace cases assigned to your group.
    -   **Open:** Select this option to view open workplace cases.
    -   **Open-unassigned**: Select this option to view open but unassigned workplace cases.
    -   **Closed**: Select this option to view closed workplace cases.
    -   **All**: Select this option to view the workplace cases.
3.  To view all the workplace cases, select **All**.

4.  Select any workplace case to view the details.

<table id="table_zpt_wdj_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique ID assigned to a workplace case request.

</td></tr><tr><td>

State

</td><td>

State of a workplace case request. For example: Workplace case is active, closed, complete, or work in progress, ready, or canceled.

</td></tr><tr><td>

Workplace case task type

</td><td>

 

</td></tr><tr><td>

Workplace location

</td><td>

Location for which the workplace case request was raised.

</td></tr><tr><td>

Workplace service item

</td><td>

Name of the service item. For example, space arrangement, tea, coffee, and so on.

</td></tr><tr><td>

Quantity

</td><td>

Service item quantity number.

</td></tr><tr><td>

Created

</td><td>

Date and time when the workplace case was created.

</td></tr><tr><td>

Updated

</td><td>

Date and time when the workplace case was updated.

</td></tr><tr><td>

Assignment group

</td><td>

Workplace assignment group to which the case is assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to this case task.

</td></tr><tr><td>

Vendor

</td><td>

Name of the vendor fulfilling the request.

</td></tr><tr><td>

Parent

</td><td>

Parent case ID number.

</td></tr><tr><td>

Delivery time

</td><td>

Delivery time of the requested service item.

</td></tr><tr><td>

Clean up duration

</td><td>

Clean up the duration time for a space.

</td></tr><tr><td>

Preparation start time

</td><td>

Start time when the service item will be prepared.

</td></tr><tr><td>

Preparation duration

</td><td>

Preparation duration for a service item request.

</td></tr><tr><td>

Cost

</td><td>

Cost of the service items.

</td></tr><tr><td>

Active

</td><td>

Option to enable and indicate that the case task is active.

</td></tr><tr><td>

Replacement for

</td><td>

When a service is updated or edited on the Workplace Reservation Management portal, the workplace case that was originally raised is replaced by a new workplace case.This notification is meant for the workplace manager or workplace agent and does the following:

-   On the old case, a notification is displayed pointing to the new case.
-   On the old case, a notification is displayed to enable easy access to the previous case to look up past actions.

For example: If while making a reservation, the original case that you raised for a service request is WCASE0001207. After you edit or update while changing a space \(location\), date, and time, a new service case, WCASE0001208, is raised as a replacement to the original case request \(WCASE0001207\). When you open the newly created request WCASE0001208, the following notification is displayed: `This is a replacement task, please check the parent case comments to see the changes, if required. The previous parent case: WCASE000127`.

For more information about retaining or discarding services while updating a reservation location, see

[Create a reservation](../../wsd-reservation-management/task/create-reservation-request-1.md).

</td></tr><tr><td>

Time worked

</td><td>

Tracks the total time spent on a case or task. The timer starts at zero, tracks time until the record is saved or closed, and resumes when revisited. You can also manually adjust, pause, or resume the timer.

</td></tr></tbody>
</table>5.  Select the gear icon \(Gear icon ![Gear settings icon.](../../workplace-space-mapping/images/gear-icon.png)\) to add the additional fields that you require.

    For example, the **Quantity**, **Total cost**, **Reservation** fields, and so on.

6.  Select the **Fulfillment instructions** tab and select the Checklist list to create a checklist for fulfilling the service request.

7.  Check the Comments and Work Notes section to see the comments added to a service request, date and time when the service was updated, or when the service was canceled.

    Applicable only for cases created as part of a reservation. When the employee changes the service and a new case is created, a summary is added to the work notes of the new case showing the following information:

    -   Added
    -   Changed
    -   Removed
    -   Not changed
    The work notes also shows the services that are not changed along with the name of the service and quantity.

8.  To see tasks associated with a case \(applicable only when services are ordered as part of a reservation\), select the **Child tasks** related link.

    New child cases for services on a category level can be created and replaced with existing ones after an employee changes services or updates a reservation. The previous cases are set to **Cancelled**.

    -   Select the child task to see the details, if applicable.

        A message is displayed describing that this case is a replacement case for a previous case.

    -   Select the case ID to view the previous case request details.
    For more information, see [Create a reservation](../../wsd-reservation-management/task/create-reservation-request-1.md).

9.  Costs are visible in the case and task level and are calculated and updated when an employee orders or edits services as part of a reservation.

    -   **Parent**: In a Parent case, cost is shown as a sum of the active child \(category\) cases.
    -   **Child \(category\)**: For child cases, cost is shown as a sum of the costs for the related tasks and cases.
    -   **Tasks**: In related tasks and cases, cost is shown as price per item, quantity, and the total costs.
10. To retain services while making a reservation using the Workplace Reservations for Microsoft Outlook Add-in, employees must open the reservation and open the plugin to change the date, time, or locations.

11. Select **Save reservation** to confirm that the services are retained,

    **Note:** Only updating the reservation in Workplace Reservations for Microsoft Outlook Add-in cancels the services.


**Parent Topic:**[Managing Workplace cases](../concept/manage-workplace-cases.md)

**Related topics**  


[View emergency maintenance case details](view-emergency-maint-case.md)

[View change event reservation case details](view-case-change-event-reservation.md)

[Print workplace cases](print-workplace-cases.md)

[Managing print cases](../concept/manage-case-print.md#)

