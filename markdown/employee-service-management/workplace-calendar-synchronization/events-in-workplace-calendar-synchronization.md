---
title: Events in Workplace Calendar Synchronization
description: For every reservation-related action, an event is created in Workplace Calendar Synchronization
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage calendar synchronizations, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Events in Workplace Calendar Synchronization

For every reservation-related action, an event is created in Workplace Calendar Synchronization

## About Events

When a synchronization is performed, the Workplace Calendar Synchronization application creates an entry for every new reservation, creation, reservation update, and reservation cancellation. To view events, navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Synchronization** &gt; **Events**.

The following events are created:

-   **Create**: A **Create** event is created whenever a reservation is created in the Workplace Reservation Management Reservation portal.
-   **Update**: An **Update** event is created whenever there’s an update to the reservation created in the Workplace Reservation Management Reservation portal or when a reservation is checked out
-   **Delete**: A **Delete** event is created whenever there is a reservation cancellation or a No show.
-   **Read**: A **Read** event is created when the Workplace Reservation Management application intends to read the reservations created on the rooms calendar in the calendar provider. The **Read** event is created only for Google Calendar and Microsoft Exchange On-Premises calendar providers.
-   **Retrieve attendees**: The **Retrieve attendees** event is created for Microsoft Exchange On-Premises calendar provider to retrieve details related to attendees included in a reservation. The **Read** event does not return attendee details for Microsoft Exchange On-Premises calendar provider.

## Event details

When an event is created, it is set to New state by default. Depending on the processing, the state changes to Processing, Processed or Error.

When an event is created, the event details on an Event form are displayed as follows:

-   In the Request related list:
    -   **Payload**: The **Payload** field contains the details of the reservation in a string format. It contains reservation-related details such as it create, update, or cancel. The format of the payload is set based on the Reservation portal form.
    -   **Provider payload**: The **Provider payload** contains the same details displayed in the **Payload** field but in the format of the calendar provider's reservation form. That is, in the format in which the calendar provider reads.
-   In the Response related list, the **Response** field displays the response to the event from the calendar provider in a string format.
    -   The response is displayed only when an event is processed. That is, when an event is set to Processed or Error.
    -   When an event returns an error, you can view the error-related details in the **Response** field
-   On the form, you can view details such as:
    -   The reservation for which the event is created.
    -   Location of the event.
    -   State and substate of the event.
    -   For what action the event is created.
    -   The provider for which the event is created.
    -   The error details if an event results in an error.
-   You can also change the **Payload**, **Provider Payload** and **Response** format from string format to JSON format using the **Format JSON** option. The **Format JSON** helps with the readability of these fields.
-   If an event fails, you can also manually reprocess the event using the **Re-process** option.

