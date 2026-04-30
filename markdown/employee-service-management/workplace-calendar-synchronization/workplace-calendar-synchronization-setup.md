---
title: Setup Workplace Calendar Synchronization
description: As an admin, establish connections with your calendar service and synchronize reservations.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Setup Workplace Calendar Synchronization

As an admin, establish connections with your calendar service and synchronize reservations.

Perform the following actions to synchronize reservations using the Workplace Calendar Synchronization:

-   Authenticate ServiceNow with your calendar provider.
-   Set up an OAuth connectivity with your calendar provider: Create an application registry and generate OAuth entities.
-   Configure connection &amp; credential aliases.
-   Configure calendar providers.
-   For Microsoft Exchange On-Premises and Google Calendar, activate the **WSDRS Sync Calendar items** scheduled job.

For more information about scheduled jobs and flows, refer to [Scheduled jobs installed with Workplace Calendar Synchronization](../reference/scheduled-jobs-installed-with-workplace-calendar-synchronization.md) and [Flows installed with Workplace Calendar Synchronization](../reference/flows-installed-with-workplace-calendar-synchronization.md).

**Important:** You will not be notified when an event is rejected or declined by Microsoft Outlook. For the same reason, a scheduled job - **Clean-up Awaiting/Rejected Reservations**, is available that you can run on any suitable frequency to clear the reservations rejected or declined by the Microsoft Outlook calendar.

**Warning:** Reservations that are created using calendar providers can’t be edited in the Workplace Reservation Management application.

## Workplace Calendar Synchronization version 1.6.1 and older

If you are using Workplace Calendar Synchronization version 1.6.1 and older, to set up a connection with Microsoft Exchange Online, refer to [Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md).

## Workplace Calendar Synchronization version 2.0.1 and later

From Workplace Calendar Synchronization 2.0.1 and later, the application uses Microsoft Exchange Online spoke. It’s required to install Microsoft Exchange Online spoke version 3.2.1, otherwise, the application doesn’t work.

Workplace Calendar Synchronization 2.0.1 and later uses Integration Hub the REST API to connect with Microsoft Exchange Online spoke.

To set up a connection with Microsoft Exchange Online spoke, refer to [Create a connection with Microsoft Exchange Online spoke](../task/create-connection-with-msspoke.md).

-   **[Set Workplace Calendar Synchronization properties](../task/set-calendar-sync-properties.md)**  
Configure the properties for the Workplace Calendar Synchronization to set the Exchange Online Sync Integration Mode to Strict, Personal Authentication, or Normal mode to synchronize reservations.
-   **[Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md)**  
Synchronize reservations between Microsoft Outlook and Workplace Reservation Management.
-   **[Google Calendar - Calendar synchronization](../reference/google-calendar-calendar-synchronization.md)**  
Create a connection with Google Calendar and synchronize reservations made using the Workplace Reservation Management application. You can synchronize all the reservations that are made using the Workplace Reservation Management to the Google Calendar and vice versa.
-   **[Microsoft Exchange On-Premises - Calendar synchronization](../reference/ms-exchange-on-prem-calendar-synchronization.md)**  
Create a connection with Microsoft Exchange On-Premises and synchronize reservations made using the Workplace Reservation Management application. You can synchronize all the reservations that are made using the Workplace Reservation Management to the On-Premises calendar and vice versa. The reservation synchronization from an On-Premises calendar to the Workplace Reservation Management is performed using various approaches like subscriptions, synchronization tokens, events, and occurrences.
-   **[Add a Reservable Sync Configuration](../task/add-reservable-sync-config.md)**  
Add workplace-workspace/desk \(or\) rooms that must be synchronized with the calendar provider whenever an employee makes a reservation.
-   **[No request handling](../task/no-request-handling.md)**  
Make a 'No request' call to test the configuration with the calendar provider.
-   **[Synchronize past reservations](../task/sync-past-reservation.md)**  
Sync reservations made in the past, that is, before configuring the reservation synchronization setup.
-   **[Retrieve reservations](../task/retrieve-reservations.md)**  
Retrieves all the events for active reservable sync configurations from Microsoft Outlook to Workplace Service Delivery.
-   **[Export reservations to the calendar provider](../task/export-reservations-to-calendar-provider.md)**  
As a one time procedure, export all your confirmed reservations to your calendar provider for synchronization.

**Parent Topic:**[Configure Workplace Calendar Synchronization](configure-rsv-sync.md)

**Related topics**  


[Install Workplace Calendar Synchronization](../task/install-workplace-calendar-synchronization.md)

