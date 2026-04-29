---
title: Create a personal authentication mode connection for Google
description: As an admin, establish a personal authentication mode connection for Google Calendar to synchronize reservations. A user-level authentication token is generated that enables you to create, update, or cancel reservations to synchronize events on the Google Calendar.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Google Calendar - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create a personal authentication mode connection for Google

As an admin, establish a personal authentication mode connection for Google Calendar to synchronize reservations. A user-level authentication token is generated that enables you to create, update, or cancel reservations to synchronize events on the Google Calendar.

## Reservation restrictions

Review the restrictions for creating, updating, or deleting user reservations, as well as for blocker and group reservations, when personal authentication mode is enabled.

<table id="table_dqt_hz2_vdc"><thead><tr><th>

Reservation type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Blocker reservations

</td><td>

When Personal mode is enabled, blocker reservations are created in the delegated user's calendar, with the requested for user added as an invitee.If the `sn_wsd_rsv.blocker_user` system property specifies a blocker user, the system creates the reservation in the delegated user's calendar and adds the blocker user as an invitee.

</td></tr><tr><td>

Onbehalf user reservation

</td><td>

The **This reservation is for** field is not displayed in personal authentication mode. In personal mode, you can't create Onbehalf user reservations because you don’t have access to other user's calendar. However, you can create on-behalf reservations for non-synchronized rooms.

</td></tr><tr><td>

Group reservations

</td><td>

Group reservations aren’t supported in Personal mode for synchronize-enabled rooms, even if the **Enable group reservations** check box is selected in the reservable module. You can create group reservations for non-synced rooms.

</td></tr><tr><td>

Create reservation

</td><td>

The following restrictions apply when creating reservations from theWorkplace Service Delivery \(WSD\) portal, Event planner, Quick Reservation, and Now Mobile:-   **In Personal mode**

If the requested-for user doesn’t match the session user, the reservation can’t be created.

**Note:** When the integration mode is Personal Authentication and reservations are created through non-ServiceNow interfaces such as IDEA panels or the Reservation REST APIs, the reservation is created in the Delegated User's mailbox, with the requestor added as an attendee. This behavior is the same as Strict mode.

-   **In Strict or Normal mode**

Reservations can be created without any restrictions.


</td></tr><tr><td>

Update or cancel reservation

</td><td>

The following restrictions apply when updating or canceling reservations from the WSD portal, Event planner, and Now Mobile:-   **In Normal mode**

All reservations can be updated or canceled.

-   **In Personal authentication mode**

    -   If the Sync mailbox of the reservation is set to **other** \(a reservation created in the delegated user calendar\), the reservation can be updated or canceled in the delegated user calendar.
    -   If the Sync mailbox is set to **user**, the following rules apply:
        -   If the reservation is edited or canceled from sources other than WSD Portal, Quick Reservation, WSD Mobile, or Event Planner, it can’t be updated or canceled.
        -   If the session user \(the person who is updating or canceling the reservation\) doesn’t match the requested-for user, the reservation can’t be edited or canceled.
        -   If a personal token doesn’t exist for the user updating or canceling the reservation, the reservation can’t be updated or canceled.
        -   In all other cases, the reservation can be updated or canceled.
**Note:** All the above reservations that can’t be updated or canceled appear dimmed in the schedule view of event planner workspace.

-   **In Strict mode**

Users can only update or cancel a reservation if the Sync mailbox is set to **other** in Strict mode.


</td></tr></tbody>
</table>