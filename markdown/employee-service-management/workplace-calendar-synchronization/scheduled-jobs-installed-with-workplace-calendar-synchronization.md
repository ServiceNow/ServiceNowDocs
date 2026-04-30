---
title: Scheduled jobs installed with Workplace Calendar Synchronization
description: The Workplace Calendar Synchronization includes scheduled jobs to process a few synchronizations seamlessly.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Scheduled jobs installed with Workplace Calendar Synchronization

The Workplace Calendar Synchronization includes scheduled jobs to process a few synchronizations seamlessly.

<table id="table_cxs_z1x_dyb"><thead><tr><th>

Scheduled job

</th><th>

Scope

</th><th>

Active

</th><th>

Time

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clean-up Awaiting/Rejected Reservations

</td><td>

Workplace Calendar Synchronization

</td><td>

True

</td><td>

Repeats every 5 hours

</td><td>

This scheduled job clears the reservations that have been stuck in awaiting confirmation for more than 5 hours \(due to rejection from outlook\)

</td></tr><tr><td>

Create and Update Reservations from Events

</td><td>

Workplace Calendar Synchronization

</td><td>

True

</td><td>

Repeats every 1 minute

</td><td>

This scheduled job inserts/updates reservations from &gt; **Microsoft Exchange Online spoke** &gt; **Events** table.

</td></tr><tr><td>

Export reservations to calendar

</td><td>

Workplace Calendar Synchronization

</td><td>

False

</td><td>

Repeats every 15 minutes

</td><td>

This scheduled job is inactive by default. The scheduled job syncs existing Workplace Reservation Management reservations with the calendar.

-   It retrieves details of the reservations that are not synchronized with the calendar.
-   Creates events for all reservations based on the respective location's calendar provider. On successful creation of events, reservations are populated with "Event Id &amp; IcalId".
-   If the script fails to create events for a reservation, you can check the logs to determine the reason behind the failure.

</td></tr><tr><td>

Subscription renewal failure notification job

</td><td>

Workplace Calendar Synchronization

</td><td>

True

</td><td>

Daily

</td><td>

This scheduled job checks for failed subscriptions that are linked to active reservable sync configuration records and notifies users with the rsvsync\_admin role.

</td></tr><tr><td>

WSDRS Multi reservation processor

</td><td>

Workplace Calendar Synchronization

</td><td>

True

</td><td>

Repeats every 15 minutes

</td><td>

This scheduled job turns reservations that are incorrectly created as single from an external source into correctly grouped multi children

</td></tr><tr><td>

WSDRS Reprocess Events

</td><td>

Workplace Calendar Synchronization

</td><td>

False

</td><td>

Repeats every 15 minutes

</td><td>

This scheduled job reprocesses the synchronization calls for WSD events that failed to process.

</td></tr><tr><td>

WSDRS Sync Calendar items

</td><td>

Workplace Calendar Synchronization

</td><td>

False

</td><td>

Repeats every 2 minutes

</td><td>

This scheduled job runs only for Microsoft Exchange Online On-Premises and Google Calendar provider. This job is not applicable to Microsoft Exchange Online.

 This scheduled job synchronizes all the events of a calendar for all the locations that have active reservable sync configurations.

</td></tr><tr><td>

Update attendees of Workplace Reservation \(Google\)

</td><td>

Workplace Calendar Synchronization

</td><td>

True

</td><td>

Repeats every 4 minutes

</td><td>

This scheduled job is installed when the Google Calendar Spoke is installed. This job synchronizes attendees, who were synced from Calendar events and stored in the calendar items, to the Reservations table.

</td></tr><tr><td>

Sync attendees for onPrem

</td><td>

Workplace Calendar Synchronization

</td><td>

True

</td><td>

Repeats every 4 minutes

</td><td>

This scheduled job is installed when Microsoft Exchange Server Spoke is installed. This job synchronized attendee, who were synced from Calendar events and stored in calendar items, to the Reservations table.

</td></tr><tr><td>

Clean-up Awaiting/Rejected Reservations \(OnPrem\)

</td><td>

Workplace Calendar Synchronization

</td><td>

True

</td><td>

Repeats every 5 hours

</td><td>

This scheduled job clears the reservations that have been stuck in Awaiting confirmation for more than 5 hours \(due to rejection from Microsoft Exchange Online On-Premises\).

</td></tr><tr><td>

Queue Webhook Events

</td><td>

Microsoft Exchange Online Spoke

</td><td>

True

</td><td>

Repeats every 1 minute

</td><td>

As Microsoft Exchange Online sends many notifications for each change, to avoid a race condition, the notifications are captured in the Webhook Notification \[sn\_ex\_online\_spke\_webhook\_notification\] table and queued to the Callback Queue \[sn\_ex\_online\_spke\_callback\_queue\] table through this scheduled job.

</td></tr><tr><td>

Weekly schedule scan

</td><td>

Workplace Calendar Synchronization

</td><td>

True

</td><td>

Once a week

</td><td>

This schedule job is a scan performed after the configuration. It is a suite for checking calendar sync configuration.

</td></tr></tbody>
</table>