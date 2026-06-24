---
title: Create a reservation waitlist
description: When all spaces in a location are fully booked, and when employees are unable to find a space, they can join a reservation waitlist queue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/create-rsv-waitlist.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 7
breadcrumb: [Manage and configure reservation waitlist, Manage employee reservations, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a reservation waitlist

When all spaces in a location are fully booked, and when employees are unable to find a space, they can join a reservation waitlist queue.

## Before you begin

Employees can join a waitlist when no spaces are available for reservation. When a space is freed up or is available, application assigns the space to an employee in the waitlist. The space allocation is done on the basis of weight \(priority\), created date \(start time when the reservation record was created\), and alphabetical order. Email and push notifications are sent when a waitlist is Queued, Confirmed, Canceled, or Expired.

Make sure you have installed and configured the following:

-   Workplace Reservation Management
-   Workplace Core
-   Workplace Central
-   The **Enable waitlist** and **Enable browse by neighborhood** Reservable Module configuration options are enabled by your workplace administrator. For more information, see [Configure Workplace Reservation Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md).

Role required: sn\_wsd\_core.workplace\_user

## About this task

You can directly join a waitlist by submitting a reservation waitlist request on the Employee Center portal. When employees join a waitlist, they are added to the waitlist queue. When a Queued space is freed up and is available, a space is assigned for reservation. Status of the waitlist record changes from **Queued** to **Confirmed**.

## Procedure

1.  Create a reservation and if no spaces are available for your preferred location and selected date and time, join a waitlist.

2.  Join a waitlist by navigating to **All** &gt; **Self-service** &gt; **Employee Center**.

3.  Select **Help Center** &gt; **Workplace Services** &gt; **Reservation Waitlist**.

    You can also navigate to the Reservation Waitlist record form by searching for **Reservation Waitlist** or **waitlist** in the search box.

4.  The Reservation Waitlist form opens.

    Fill in the form fields:

<table id="table_hgm_l2n_3jc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requested for

</td><td>

Automatically updated with the logged in username.

</td></tr><tr><td>

Reservable type

</td><td>

Option to enter a Reservable Module type configuration. For example, **Desks**, **Meeting rooms** and so on.**Note:** Shift-based Reservable Module configurations aren't supported for waitlisting a space.

The **Enable waitlist** check box option in the Reservable Module configuration should be selected by your workplace administrator for you to create reservation waitlist. The Reservable Module configuration selected is shown for selection here. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

</td></tr><tr><td>

Building

</td><td>

Select a building location where you want to create a reservation waitlist.**Note:** Buildings added to the **Reservable Table configuration** are shown for selection. If you have updated the **Workplace Locations** in Reservable Table configuration, the Workplace Locations are prioritized over Buildings updated in the Reservable Table Configuration. For example, if you configure any buildings \(AMSB1 or CALB1\) in **Workplace Locations**, these locations get prioritized over the Buildings added in the Reservable Table Configuration.

For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

</td></tr><tr><td>

Neighborhood

</td><td>

Option to select a Neighborhood.**Note:** Neighborhoods assigned to a selected building and to which an employee has access to are only shown for selection.

The **Enable browse by Neighborhood** check box option should be enabled by your administrators in the Reservable Module Configuration. Only then Neighborhoods are displayed for selection. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md)

</td></tr><tr><td>

Floor

</td><td>

Select a floor in a building.**Note:** If you have selected a neighborhood, the floors in a neighborhood are shown for selection.

</td></tr><tr><td>

Start Time

</td><td>

Option to select a start time for your reservation waitlist. **Note:**

Start time for a reservation should not be in the past. Start time value is dependent on the Max days in future Reservable Module configuration value. Time is shown in the selected Building time zone.

For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md)

</td></tr><tr><td>

End Time

</td><td>

Select an end time for your waitlist.**Note:** End time must be after start time. End time shouldn't be in the past.

</td></tr></tbody>
</table>5.  Review the waitlist request form and confirm that the details are correct.

6.  Select **Submit**.

    A message is displayed "You have been added to the waitlist. We will notify you when the space is available."

    An email notification and push notification is sent to the employee when they are added to a waitlist.

    To view the notifications, navigate to **All** &gt; **System Logs** &gt; **Emails**. Filter and search by waitlist. Select **Preview Email** from Related links to open the email notification.

    \[Omitted image "waitlist-email-notification-1.png"\] Alt text: Email notification sent to employees to inform that they are on a waitlist.

    **Note:** If a space is available for a preferred location, date, and time, the waitlist reservation request is immediately fulfilled and a space is assigned for reservation. In this case, the waitlist record is not queued as the request is fulfilled immediately.

7.  The Waitlist Summary page opens when you submit a waitlist request.

    1.  The waitlist record status is shown as **Queued**.
    2.  Review the Waitlist number, location, and time details \(start and end time, duration, and time zone details\).
    3.  Select **Quick Actions** &gt; **Cancel Request**.

        You can cancel a waitlist request if you don't want to join a waitlist. Workplace Reservation Event Planners can also cancel a waitlist record.

8.  Navigate to **Help Center** &gt; **Workplace Services** &gt; **Open my reservation list**.

    My Reservations page opens.

9.  Select the **Waitlist** tab option on My reservations page.

    \[Omitted image "rsv-my-reservations-page-showing-waitlist-status.png"\] Alt text: My Reservations page showing waitlist records and their statuses.

10. Reservation waitlist status is shown as **Confirmed**, **Queued**, **Canceled**, or **Expired**.

    -   Confirmed: Confirmed waitlist records can't be canceled. You can only view details or view reservation for a confirmed waitlist. Select the more options icon \(\[Omitted image "waitlist-more-options-icon.png"\] Alt text: Select the icon to see additional options to view, cancel, or update a waitlist record.\) to View Details or View Reservation.
    -   Queued: Queued waitlist records can be canceled and you can view the waitlist details. Select the more options icon \(\[Omitted image "waitlist-more-options-icon.png"\] Alt text: Select the icon to see additional options to view a waitlist record..\)

        \[Omitted image "waitlist-rsv-summary-queued-more-options.png"\] Alt text: Queued Waitlist record shows the View Details and Cancel Waitlist options.

        Select **Cancel waitlist** to cancel a waitlist record.

        Select **View details** to review the Waitlist Summary detail.

        \[Omitted image "reservation-details-page-selection-status.png"\] Alt text: Select a waitlist record to see the waitlist record summary details.

    -   Canceled: You can only view details for a canceled waitlist record. Select the more options icon \(\[Omitted image "waitlist-more-options-icon.png"\] Alt text: Select the icon to see additional options to view a waitlist record.\) to **View Details** for a waitlist record.
    -   Expired: Expired waitlist records aren't shown on the My Reservation Waitlist page.
    Workplace reservation event planners can prioritize a waitlist that is queued. They can increase the weight of a Queued waitlist record to move it up in the queue for faster space assignment. They can update the weight of a waitlist record to prioritize it in the queue. They can also assign a space on behalf of others for waitlisting a space. For more information, see [Manage reservation waitlist records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/rsv-planner-subscribe-waitlist.md).

11. To view all waitlist records, navigate to **All** &gt; **Workplace Reservations Management** &gt; **Reservations Overview** &gt; **My Waiting list**.

    The Reservations Waiting Lists \(sn\_wsd\_rsv\_waitlist\_list\) table opens.

    \[Omitted image "waitlist-my-waiting-list-table-page.png"\] Alt text: Reservation waiting list table shows all waitlist record entries along with their status and priority or weight assigned.

12. Email and push notifications are sent to users for every waitlist record status change.

    When your waitlist is Queued, you get notified. When it gets canceled, you are notified. When it expires, you get a notification. For every state change, you get a notification.

    \[Omitted image "waitlist-email-notification-1.png"\] Alt text: Email notification sent to employees.

    **Note:** When the employee has an waitlist for the same module, date, and overlapping time, the waitlist record is created and the employee is informed. Resolving a waitlist item, will not complete any other overlapping items. These remain in the queue until these are cancelled, confirmed, or expired.


**Parent Topic:**[Manage and configure reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/subscribe-waitlist-overview.md)

**Previous topic:**[Reservation Waitlist data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/waitlist-configuration.md)

**Next topic:**[Create a schedule job for waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/schedule-job-waitlist.md)

