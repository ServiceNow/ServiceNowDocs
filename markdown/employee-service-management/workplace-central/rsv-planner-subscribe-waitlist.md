---
title: Manage reservation waitlist records
description: Workplace Reservation event planners can view and update the weight of a queued record and cancel waitlist records. You can also manually assign a space to employees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/rsv-planner-subscribe-waitlist.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-05-23"
reading_time_minutes: 4
breadcrumb: [Manage, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Manage reservation waitlist records

Workplace Reservation event planners can view and update the weight of a queued record and cancel waitlist records. You can also manually assign a space to employees.

## Before you begin

Role required: sn\_wsd\_rsv.reservation\_planner

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

2.  Select the Lists \(\[Omitted image "list-options.png"\] Alt text: List icon.\) on the home page.

3.  Select **Waitlist Management** &gt; **Reservation Waitlist**.

    All reservation waitlist records are shown. Time is rendered in the selected building's time zone.

    \[Omitted image "waitlist-event-planner-list-view.png"\] Alt text: Waitlist records shown in Lists along with their status.

    **Note:** Event Planners can manually assign spaces when the record is in a **Queued** state.

4.  Select a **Queued** waitlist record status to review details and update the weight or priority.

    The event planner form opens.

    \[Omitted image "waitlist-priority-field-assign-space.png"\] Alt text: Selected reservation waitlist record showing priority field and Assign a space tab.

    Event Planners can change the weight or priority of a waitlist record that is in **Queued** status and save it. Event Planners can cancel a waitlist record that is queued on behalf of an employee.

    **Note:** Event planners can update only a **Queued** waitlist record.

5.  Update **Weight** \(priority\).

    Event planners can prioritize a waitlist record in the queue. Prioritizing a waitlist record moves the selected record to rank higher in the queue. Provide the highest possible weight number to a record. The Queued waitlist record for a space is prioritized for space assignment. For example, if a Queued waitlist is showing **Weight** as `50`, change it to `100` so that the waitlist entry moves up in the queue for quicker space assignment.

    When a weight or priority value is not added, the application filters waitlist records based on the **Create by** field in the Reservation Waiting Lists Table. For example, if there are 5 waitlist records, the application prioritizes the waitlist record that was created first, based on the date and time field values. For example, a waitlist record that was created on 16/05/2026 will be prioritized before a waitlist record that was created on 21/05/2026. For more information, see [Reservation Waitlist data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/waitlist-configuration.md).

6.  Select **Save**.

7.  Select **Assign a space** to assign a space as an event planner.

    Event planners managing space assignments on behalf of employees can manually assign a space to an employee. Manual assignment can be done when an employee is unable to find a space or search for a space using the Reservation portal search page.

    **Note:** The **Assign Space** option is not available for **Confirmed** waitlist records.

    The Make a reservation page opens for assigning a space.

    \[Omitted image "waitlist-assign-space-make-reservation.png"\] Alt text: Make a reservation page showing prefilled values from a waitlist record.

    All values in the selected waitlist record are carried forward and automatically populated on the Make a reservation page. Module name, building, floor, neighborhood, start time, and end time show prefilled values from the selected waitlist record.

8.  Select a building, floor, preferred time, and date to find an available space.

9.  Make the required changes and select **Next**.

    For more information, see [Create a reservation]().

10. Review the Reservation details page and make changes as required.

    \[Omitted image "assign-space-rsv-details-page.png"\] Alt text: Reservation details page showing updated reservation entries.

    **Note:** **This reservation is for** field on the Reservation Details page is automatically set to the current logged-in waitlisted user and not the current workplace event planner.

11. Submit the reservation.

12. Navigate to **All** &gt; **Workplace Central** &gt; **Lists** &gt; **Waitlist Management** &gt; **Reservation Waitlist**.

    The Reservation Waitlist shows status changes to **Confirmed** from previous **Queued** status.

    \[Omitted image "waitlist-assign-space-rsv-status-confirmed.png"\] Alt text: Waitlist entry showing status as confirmed.

    The **Priority** \(Weight\) field is a read-only field for waitlist records that are **Confirmed**. The **Cancel** button is not available for a confirmed waitlist record.

13. Open the confirmed waitlist record.

    The Reservation summary page opens.

14. Navigate to **All** &gt; **Workplace Reservation Management** &gt; **My Reservation Waiting Lists** to review the waitlist reservation records along with their status.

    For more information, see [Reservation Waitlist data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/waitlist-configuration.md).

    \[Omitted image "waitlist-my-waiting-list-table-page.png"\] Alt text: My Reservation Waiting List table showing waitlist status and priority field values.


**Parent Topic:**[Manage Workplace Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/manage-workplace-central.md)

**Related topics**  


[Approve a scenario]()

[View workplace scenarios]()

[Raise a space assistance request]()

[Approve a space assist request]()

[Manage and configure reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/subscribe-waitlist-overview.md)

[Create a reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-rsv-waitlist.md)

