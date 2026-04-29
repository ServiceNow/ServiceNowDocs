---
title: Setup Workplace Calendar Synchronization
description: As an admin, create connections with your calendar providers and synchronize reservations.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Setup Workplace Calendar Synchronization

As an admin, create connections with your calendar providers and synchronize reservations.

Perform the following actions to synchronize reservations using the Workplace Calendar Synchronization:

-   Authenticate ServiceNow with your calendar provider.
-   Set up an OAuth connectivity with your calendar provider: Create an application registry and generate OAuth entities.
-   Configure connection &amp; credential aliases: Specify the connection type, OAuth entity profile and type of credentials.
-   Configure calendar providers: Select the calendar processor and specify how and when to perform synchronization.
-   For Microsoft Exchange On-Premises and Google Calendar, activate the **WSDRS Sync Calendar items** scheduled job.

For more information about scheduled jobs and flows, refer to [Scheduled jobs installed with Workplace Calendar Synchronization](../reference/scheduled-jobs-installed-with-workplace-calendar-synchronization.md) and [Flows installed with Workplace Calendar Synchronization](../reference/flows-installed-with-workplace-calendar-synchronization.md).

**Important:** You will not be notified when an event is rejected or declined by Microsoft Outlook. For the same reason, a scheduled job - **Clean-up Awaiting/Rejected Reservations**, is available that you can run on any suitable frequency to clear the reservations rejected or declined by the Microsoft Outlook calendar.

**Warning:** Reservations that are created using calendar providers can’t be edited in the Workplace Reservation Management application.

## Workplace Calendar Synchronization version 1.6.1 and older

If you are using Workplace Calendar Synchronization version 1.6.1 and older, to set up a connection with Microsoft Exchange Online, refer to [Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md).

## Workplace Calendar Synchronization version 2.0.1 and later

From Workplace Calendar Synchronization 2.0.1 and later, the application uses Microsoft Exchange Online spoke. It’s required to install Microsoft Exchange Online spoke version 3.2.1, otherwise, the application doesn’t work.

Workplace Calendar Synchronization 2.0.1 and later uses Integration Hub the REST API to connect with Microsoft Exchange Online spoke.

