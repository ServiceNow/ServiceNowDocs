---
title: Create workplace reservations for an employee
description: Create workplace reservations for an employee in the Workplace Core application using the shifts and shift schedules that you defined.
locale: en-US
release: australia
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing workplace reservations for employees, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Create workplace reservations for an employee

Create workplace reservations for an employee in the Workplace Core application using the shifts and shift schedules that you defined.

## Before you begin

-   [Define shifts for your workplace](create-shifts-wsd.md).
-   [Assign employees to a shift](associate-employees-with-shifts-wsd.md).
-   [Associate areas and spaces with a shift](associate-workspaces-with-shifts-wsd.md).
-   [Define the capacity of workplace areas](define-capacity-of-workplace-areas-wsd.md)
-   Ensure you have the data that shows the mapping of employees to the workplaces in your workplace.

**Important:** Starting with Workplace Core \(sn\_wsd\_core\) version 2.1, all updates and new features are available only on the Workplace Service Portal. The workplace services provided by ServiceNow® are removed from the Service Portal on Workplace Core \(sn\_wsd\_core\) beginning with version 2.1. To configure the Workplace service catalog in the Service Portal, see [Configure a catalog in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/associate-portal-catalog.md).

Role required: sn\_wsd\_core.workplace\_manager

## About this task

Reserve a workplace for an employee according to the assigned shift for a single day or multiple days.

You can also access the Reservation form by navigating to **Workplace Core** &gt; **Space Reservations** &gt; **Create New**.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **Browse Workplace Services**.

2.  Scroll and select **Reserve a space**.

3.  On the form, fill in the fields.

<table id="table_eqz_3f4_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shift

</td><td>

Shift for which this reservation is being made.

</td></tr><tr><td>

Location

</td><td>

Area or space for which this reservation is being made.

</td></tr><tr><td>

Requested for

</td><td>

Employee for whom this reservation is being made.

</td></tr><tr><td>

Start date

</td><td>

Date and time from which the reservation is active.

</td></tr><tr><td>

End date

</td><td>

Date and time until which the reservation remains active.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  If you accessed the Reservation form from Workplace Service Portal, on the verification page, you can create another reservation or view all the existing reservations.

    |Option|Action|
    |------|------|
    |**Create another workplace reservation**|Select **Reserve another space**.|
    |**View existing workplace reservations**|Select **View all reservations**.|


## Result

-   If you've reserved a space, then child reservation records are generated for every applicable occurrence of the specified period.
-   A preconfigured email with the reservation details is sent to the shift owner and the employee for whom you reserved the workplace.
-   The reservation is added to the list of all reservations that you can view by navigating to **Workplace Core** &gt; **Space Reservations** &gt; **All Reservations**.

**Parent Topic:**[Managing workplace reservations for employees](../concept/managing-workplace-reservations-wsd.md)

