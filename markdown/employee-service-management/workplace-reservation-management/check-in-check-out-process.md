---
title: Manage check-in and check-out reservations
description: Reservation check in and check- out reminders are managed through the Check-in and check out reminder scheduled jobs
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2025-12-09"
reading_time_minutes: 4
breadcrumb: [Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Manage check-in and check-out reservations

Reservation check in and check- out reminders are managed through the Check-in and check out reminder scheduled jobs

The following properties are being used in this scheduled job:

-   sn\_wsd\_rsv.time\_before\_check\_in\_out\_reminder
-   sn\_wsd\_rsv.time\_when\_reservation\_cancelled\_without\_check\_in

Ensure check-in is required on the Reservable module at the space level. For more information, see [Configure a reservable module](../task/config-reservable-module.md).

-   This can be enforced through the Reservable Module property value **Override check-in policy**” on the Reservable Module to **always require check-in**
-   This can be managed at the space level. Space is indicated as check-in required. Set **Override check-in policy** on the Reservable Module to **no override**.
-   On the Reservation summary page, the check-in state should be set to **awaiting\_check\_in**.
-   Reservations are only cancelled when the **Cancel reservations exceeding check-in time** check box is selected on the Reservable Module
-   The check-in and check-out schedule job runs every 30 minutes by default. It takes into account all the workplace reservations that require check-in or check-out, and validates the next action.

<table id="table_izg_yg4_4hc"><thead><tr><th>

Check-in required

</th><th>

Within time\_before\_check\_in\_out\_reminder is 30min by default

</th><th>

Within time\_when\_reservation\_cancelled\_without\_check\_in is 30min by default

</th><th>

Action

</th></tr></thead><tbody><tr><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

Reservation is not handled by the scheduled job.

</td></tr><tr><td>

Yes

</td><td>

No, before start time

</td><td>

No

</td><td>

No action required.

</td></tr><tr><td>

Yes

</td><td>

Yes, 10 minutes past reservation start time.

</td><td>

No

</td><td>

Employee receives an email notification.Template: Check-in Reminder PL

</td></tr><tr><td>

Yes

</td><td>

Yes

</td><td>

Yes, 40min past the reservation start time.

</td><td>

Reservation is cancelled.

</td></tr><tr><td>

Yes

</td><td>

Yes, 10 minutes past the reservation end time.

</td><td>

NA

</td><td>

If the reservation is checked in, employee receives an email notification.

 Template: Check-out Reminder PL

</td></tr></tbody>
</table>    **Note:**

    -   Takes about 30 minutes \(based on the default configuration\) to receive an email notification for an employee who has not checked in the reservation.
    -   Takes about 60 minutes \(based on the default configuration\) for the reservation to be cancelled in case the employee did not check-in the reservation.
    The daily scheduled job **Reservation daily tasks** closes all reservations at the end of the office working hours. Reservation may be closed the day after. The check-in state for reservations that are checked-in is indicated as **no\_check\_out**.


**Parent Topic:**[Configure Workplace Reservation Management portal](wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](../task/install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](../task/add-reservable-items.md)

[Add a workplace room for reservation](../task/add-workplace-rooms.md)

[Configure a reservable module](../task/config-reservable-module.md)

[Assign spaces to an area](../task/add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](../task/add-standard-services.md)

[Create a flexible service](../task/add-flexible-service.md)

[Create a workplace service to provide an extra service for a reservation](../task/create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](../task/create-a-reservable-view.md)

[Create a user criteria record](../task/create-user-criteria.md)

[Configure a reservable purpose](../task/configure-reservable-purpose.md)

[Create a quick reservation time slot](../task/add-reservable-time-slots.md)

[Configure virtual meeting providers](../task/configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](../task/configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](../task/connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](../task/connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](../task/display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](../task/displayname-person-booking-rsv.md)

[Configure automatic check-in for reserved spaces](configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](rsv-config-rsv-mod-value.md)

