---
title: Manage calendar synchronizations
description: As an admin, monitor the number of events and calendar items in the Workplace Calendar Synchronization application whenever a reservation is synchronized.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Manage calendar synchronizations

As an admin, monitor the number of events and calendar items in the Workplace Calendar Synchronization application whenever a reservation is synchronized.

As an admin, the application enables you to view and manage the following:

-   Approvals
-   Events
-   Calendar items
-   Synchronization deltas

When you configure synchronization, you must keep in mind a few important conditions. Refer to [Synchronization - Prerequisites and implementation](../reference/synchronization-troubleshooting-and-conditions.md).

## Approvals

If there are any reservations created from the calendar provider application that requires approval, you can approve them using the Workplace Core approval configuration. For more information on how to approve a reservation or create a performer criteria, refer to [Create a workplace performer criteria](../../workplace-service-delivery/task/create-workplace-performer-criteria.md).

## Events

Every action during a reservation synchronization triggers an event. These actions include creating, updating, or canceling a reservation. The Workplace Calendar Synchronization handles these events and sends notifications to the calendar services. For more information about an event and the type of events created in the application, refer to [Events in Workplace Calendar Synchronization](../reference/events-in-workplace-calendar-synchronization.md).

-   An event can create one or more calendar items.
-   An event contains a request and a response to the request.
-   To ensure that multiple calendar services can communicate with Workplace Reservation Management, events translate the reservations and messages from the calendar provider into standardized actions in Workplace Reservation Management.

When a workplace item is synchronized with the calendar service, an event is created to get the latest details. The response from the calendar service also creates an event. Similarly, events are created whenever a reservation is created or updated within Workplace Reservation Management for workplace items that are configured to synchronize. You can convert an event into JSON format. You can also reprocess an event if there was an error or for any reason.

## Calendar items

Every action performed by the calendar service is converted to a calendar item that is handled in the Workplace Reservation Management application. A calendar item is either a new reservation or a reservation update. Using calendar items, you can also create, update, or cancel a reservation in the Workplace Reservation Management application.You can convert a calendar item into JSON format.

## Synchronization deltas

When a workplace item is synchronized, a delta key is generated. A delta key is used and updated every time a workplace item synchronizes with the calendar service. Each sync delta contains a token that indicates how much information was synced last time so that a delta with the new changes can be returned in the next request instead of the complete calendar history. You can know the details of the workplace item such as the number of reservations created, or any changes made on the reservation. The delta key ensures that only the changes that occurred between the previous and the current synchronization is retrieved. The delta key retrieves details of any new, updated, and canceled reservations on the workplace item.

**Note:** Synchronization deltas are used only for Microsoft Exchange On-Premises and Google Calendar.

-   **[View synchronization details](../task/view-synchronization-details.md)**  
Check the number of the events and calendar items that are created during a synchronization.
-   **[Events in Workplace Calendar Synchronization](../reference/events-in-workplace-calendar-synchronization.md)**  
For every reservation-related action, an event is created in Workplace Calendar Synchronization
-   **[Synchronization - Prerequisites and implementation](../reference/synchronization-troubleshooting-and-conditions.md)**  
When you connect to your calendar provider for synchronization, you may incur a few connection or synchronization-related issues.
-   **[Run Instance scan to check Microsoft Exchange Online synchronization configuration](../task/run-instance-scan-on-your-workplace-cal-sync-configs.md)**  
Execute an Instance scan on your ph keyref="var.workplace-calendar-sync"/&gt; configuration with Microsoft Exchange Online. The Instance Scan application diagnoses the configurations with the calendar provider by running a series of checks using suites.

**Parent Topic:**[Workplace Calendar Synchronization](workplace-calendar-sync-feat.md)

