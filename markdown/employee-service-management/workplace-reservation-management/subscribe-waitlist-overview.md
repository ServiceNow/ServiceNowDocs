---
title: Manage and configure reservation waitlist
description: A reservation waitlist lets employees queue for a preferred space, duration, and location. The waitlist record is held until the preferred space is available.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/subscribe-waitlist-overview.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 6
breadcrumb: [Manage employee reservations, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Manage and configure reservation waitlist

A reservation waitlist lets employees queue for a preferred space, duration, and location. The waitlist record is held until the preferred space is available.

Employees can join a waitlist when building spaces are fully booked. They can join a waitlist queue until a space is available. A space can be freed up or made available. When a space is available, application assigns the space for reservation and the waitlist gets confirmed. Joining a waitlist helps avoid manual monitoring of available or freed up spaces on the reservation portal. It also streamlines the reservation process and helps avoid friction.

Joining or subscribing to a waitlist helps workplace administrators and reservation event planners as follows:

-   Reduces scheduling friction for both employees and workplace administrators.
-   Helps avoid manual monitoring for available or freed-up spaces for reservation.
-   Improves office space utilization by filling vacated spaces automatically. Workplace Event Planners and Workplace Managers get insights on space utilization, space optimization, and space demand requirements for a given location.
-   Event planners can review and update waitlist records that are queued. They can change the weight or priority of a Queued waitlist record and move it up in the queue for space allocation. They can also manage space assignments on behalf of employees. They can assign a space when employees are unable to find a preferred reservable space and time slot.

## Reservation waitlist workflow

The following steps describe the waitlist lifecycle:

1.  The **Enable waitlist** check box on the Reservation Module configuration is enabled by workplace administrators to allow employees to join a waitlist.
2.  Employees can join a waitlist and select their preferred neighborhoods. They can waitlist on a neighborhood.

    **Note:** The **Enable browse by neighborhood** check box must be selected by workplace administrators .

3.  Employees can make a reservation using the reservation portal. For more information, see [Create a reservation]().
4.  Employees can submit a Reservation waitlist record using the Employee Center portal. The application creates a waitlist record.

    **Note:** Employees can only subscribe to the waitlist when the Reservation waitlist record producer is enabled by workplace administrators.

    For more information, see [Create a reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-rsv-waitlist.md).

5.  Initially, the waitlist record is **Queued**. When a space is freed up or available, the status of the waitlist changes from **Queued** to **Confirmed**. The waitlist status changes to **Confirmed** when a space is assigned to an employee.

    If at the moment of submitting the waitlist, a space is available, the waitlist request is completed instantly. A reservation is created for the employee and the waitlist record is marked as completed. If no spaces are available while submitting a waitlist request, the request moves to **Queued** status until a space is made available and it moves to **Confirmed** state.

6.  Employees receive an email notification and a push notification that a space is assigned for reservation. For all stages of a Waitlist record lifecycle, employees receive an email and push notification \(Queued, Confirmed, Completed, and Expired\).
7.  Workplace reservation event planners can update the weight or priority of a queued waitlist record to move it up in the queue for confirmation.

    The application fetches the waitlist queue records and assigns a space based on the highest weight or priority assigned for a queued waitlist. If weight or priority is missing for a queued waitlist, the application checks for **Created** column value in the Workplace Reservation table. It prioritizes space assignments based on the first in, first out \(FIFO\) logic or first-come, first-served basis . Based on the start time of a queued waitlist record, space assignment is done. The oldest record or a record with the oldest start time is prioritized. Recent or newly added waitlist records are queued and wait behind all previously queued records. For more information, see [Reservation Waitlist data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/waitlist-configuration.md).

    For more information, see [Reservation Waitlist data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/waitlist-configuration.md).

8.  Workplace event planners can also assign a space manually on behalf of employees. If employees are unable to find a space or when they request event planners to assign a space, they can assign a space. If a space is available, the waitlist request is fulfilled immediately and confirmed. A reservation is created and the **Fulfilled by** column in the Reservation Waitlist table is updated with the event planner's name who assigned a space manually.

    For more information, see [Reservation Waitlist data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/waitlist-configuration.md).

    **Note:** Only Reservation Event planners can update and change the priority or weight of a Queued waitlist record.

9.  The**Waitlist expiration** scheduled job runs nightly . It removes canceled, expired, or queued waitlist records with an older start time \(timestamp\). If no space is available on the requested start time and date, the waitlist entry expires automatically. The waitlist expiration scheduled job removes or expires stale or past waitlisted records. The expired records aren't permanently removed from the system. For more information, see [Create a schedule job for waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/schedule-job-waitlist.md).
10. Expired and canceled entries older than one month are permanently deleted from the system . For more information, see [Purge a waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/purge-waitlist.md).

1.  [Reservation Waitlist data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/waitlist-configuration.md)  
The Reservation Waitlist data model describes the tables and configuration options that support waitlist requests, space allocation, and reservation fulfillment for employees.
2.  [Create a reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-rsv-waitlist.md)  
When all spaces in a location are fully booked, and when employees are unable to find a space, they can join a reservation waitlist queue.
3.  [Create a schedule job for waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/schedule-job-waitlist.md)  
A nightly scheduled job Waitlist Expirations handles expiration of past or stale waitlist records that are in Queued state. The nightly job runs daily and sets the status of any record with an expired or stale stale start time.
4.  [Purge a waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/purge-waitlist.md)  
An auto flush rule on the Reservation Waiting List \(**sn\_wsd\_rsv\_waitlist**\) table purges expired waitlist records older than 30 days to maintain accurate waitlist management reporting.

**Parent Topic:**[Manage employee reservations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/manage-reservation-requests.md)

**Related topics**  


[View or update reservations]()

[Approve a reservation]()

[Print workplace reservations]()

