---
title: Define shifts for your workplace
description: Define shifts in Workplace Core with specific schedules so you can designate areas or workplace and assign employees for each shift.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring shifts for your workplace, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Define shifts for your workplace

Define shifts in Workplace Core with specific schedules so you can designate areas or workplace and assign employees for each shift.

## Before you begin

-   [Providing your workplace data](../../workplace-service-delivery/concept/providing-your-workplace-data-wsd.md).
-   Ensure you have the following information:
    -   Appropriate shift schedules
    -   Data of the employees who would operate from the office in this shift
    -   Data of the workplaces to be made available for this shift

Role required: sn\_wsd\_core.workplace\_manager

## About this task

Workplace managers can later reserve workplaces for employees according to the shifts assigned to them.

If your organization does not organize work in shifts, you can use the general shift schedule that is available with the application by default.

You can also access the Shift form by navigating to **Workplace Core** &gt; **Shift Management** &gt; **Create New**.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **Browse Workplace Services**.

2.  Select **Add a shift**.

3.  On the form, fill in the fields.

<table id="table_w1q_c5b_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the shift, for example, Morning Shift.

</td></tr><tr><td>

Schedule

</td><td>

Schedule for the shift.For a general shift schedule, select **General shift**.

 For more information about how to create a shift schedule, see [Define a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_DefineASchedule.md).

</td></tr><tr><td>

Owner

</td><td>

Shift owner who monitors activities during this shift.

</td></tr><tr><td>

State

</td><td>

Status of the shift. Choose one of the following values:-   **Draft**: Indicates that the shift details are incomplete.
-   **Ready**: Indicates that the shift is ready for assignments.
-   **Cancelled**: Indicates that the shift is cancelled.


</td></tr><tr><td>

Start

</td><td>

Date from which this shift is active.

</td></tr><tr><td>

End

</td><td>

Date until which the shift is active.

</td></tr><tr><td>

Region

</td><td>

Region of the workplace site.

</td></tr><tr><td>

Site

</td><td>

Site location of the office campus.

</td></tr><tr><td>

Campus

</td><td>

Name of the campus in which the office building is present.

</td></tr><tr><td>

Building

</td><td>

Name of the building in which the office floor is located.

</td></tr><tr><td>

Floor

</td><td>

Name or number of the floor where the area is located.

</td></tr><tr><td>

Area

</td><td>

Area that is active for operation and use during this shift.

</td></tr><tr><td>

Users

</td><td>

Employees assigned to this shift.This field appears only on Workplace Service Portal.

</td></tr><tr><td>

Locations

</td><td>

Workplaces available for reservation during this shift.This field appears only on Workplace Service Portal.

</td></tr></tbody>
</table>    **Note:**

    -   If this shift is applicable to all office buildings on your campus, you can leave the **Building**, **Floor**, and **Area** fields empty. The shift and its schedule will be automatically applied to all the records of buildings, floors, and areas associated with this campus.
    -   When an employee requests to make a reservation with shifts, only shifts that are active on the dates that the employee selected are displayed on the reservation form.
4.  Select **Submit**.

5.  If you accessed the Shift form from Workplace Service Portal, on the verification page, you can define another shift or view all the existing shifts.

    |Option|Action|
    |------|------|
    |**Define another shift**|Select **Add another shift**.|
    |**View all existing shifts**|Select **View all shifts**.|


## Result

The shift is added to the list of all shifts that you can view by navigating to **Workplace Safety Management** &gt; **Shift Management** &gt; **All**.

If you want to delete a shift, perform the following actions:

-   Navigate to **Workplace Safety Management** &gt; **Shift Management** &gt; **All** and select the shift that you want to delete.
-   On the form, click**Delete**.
-   In the confirmation window, click **Delete**.

    The shift is deleted.


## What to do next

If you created the shift using Workplace Service Portal, you can directly create workplace reservations.

You can configure other information such as employees, workplaces, and maintenance tasks associated with this shift later.

-   Assign more employees to a shift.
-   Associate more workplaces with a shift.
-   Associate tasks with a shift.

**Parent Topic:**[Configuring shifts for your workplace](configuring-shifts-for-your-workplace.md)

