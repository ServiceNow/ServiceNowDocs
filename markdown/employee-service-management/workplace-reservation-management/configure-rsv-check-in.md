---
title: Configure automatic check-in for reserved spaces
description: Configure automatic reservation check-in using the Occupancy state of a location or space. If a location is using occupancy data sensors, it checks for Occupancy state of each space in the Space Occupancy data table
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure automatic check-in for reserved spaces

Configure automatic reservation check-in using the Occupancy state of a location or space. If a location is using occupancy data sensors, it checks for Occupancy state of each space in the Space Occupancy data table

The Workplace Reservation Management scheduled job **Check-in/out reminder** runs every half an hour \(30 minutes\) daily. It checks for the location state \(Occupied, Unoccupied, Invalid, currently not occupied, etc.\) in the Space Occupancy data table. It also checks if the reservation is checked in or checked out. For more information, see [Retrieving Space Occupancy Data](../../workplace-connectors/task/space-occupancy-data.md).

**Note:** Reservation check-in and check-out is currently not supported for multi-location reservations \(combining two or more reservations into one reservation\). Check-in or check-out of reservations with multiple locations for the same date and time and with the same reservation owner is not allowed by the application. In case of group reservations, each space is assigned to a different employee, check-in for group reservations is also not allowed in bulk. You have to check-in a reservation one at a time.

Role required: sn\_wsd\_rsv.admin

If the space state is Occupied, it triggers an automatic check-in process and sends an updated push notification to Workplace Service Delivery for Mobile "Your reservation for &lt;location\_name&gt; has started. You are automatically checked in based on the presence detected at the space. No further action is required."

Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Module** and ensure that the following properties are configured:

-   The Override check-in policy: Select **Always require check-in**.
-   Cancel reservations exceeding check-in time: Select the check box.
-   Time before employee can check-in value: Enter a value. For example, 10 minutes.

In Reservation properties list \(**All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Properties**\), configure the following properties:

-   **The amount of time in minutes until a reminder should be sent to the reservation host** \[sn\_wsd\_rsv.time\_before\_check\_in\_out\_reminder\]. For example, set the property value to 5 minutes.
-   **The amount of time in minutes until a reservation is cancelled without a check-in** \[sn\_wsd\_rsv.time\_when\_reservation\_cancelled\_without\_check\_in\]. For example, set the property value to 30 minutes.

    For example, after setting the above properties and reservable module properties, if an employee creates a reservation at 5 pm, the application checks for the following conditions:

    -   The Workplace Reservation Management application waits till 5.05 PM as per the value set in the property **Amount of time in minutes until a reminder should be sent out to the reservation host \(sn\_wsd\_rsv.time\_before\_check\_in\_out\_reminder\)** to check whether the reservation is checked in or not.
    -   After 5.05 PM, the scheduled job **Check-in/out reminder** checks the Space Occupancy data table to check if the reserved space \(for example, A1001\) is available in the Space Occupancy data table.
    -   In the Workplace Connectors, the system property **sn\_wsd\_wc.stale\_time** checks if the **Event Timestamp** field in the Space Occupancy data table has the latest timestamp. This property checks for the time beyond which the occupancy data is considered stale. Beyond the stale time, the fresh data is fetched from the Occupancy data provider \(for example, Metrikus Spoke\). If the **sn\_wsd\_wc\_stale\_time** property value is set to 30 minutes, application queries the Space Occupancy table and fetches the fresh data state for a location or space from Metrikus Spoke.

        If the state is **Occupied**, then, application automatically checks in the reservation. The reservation state moves to **In progress** state. A push notification is sent to Workplace Service Delivery for Mobile "Your reservation has started. You are automatically checked in based on the presence detected at the space. No further action is required."

    -   When workplace spaces are having occupancy sensor and if the state of the space is unoccupied or Invalid, application sends push notification "Your reservation for Reservation for &lt;space-name&gt; has started. Check in to confirm your attendance or Release Booking to Cancel the space reservation".
    -   When the workplace spaces are not having a occupancy sensor, and if the user does not check in the reservation, application cancels the reservation if the Reservable Module property **Cancel the reservation exceeding check in time** is selected.
    -   If the **Cancel the reservation exceeding check in time** is not selected, then the reservation is moved to **Confirmed** state, and the Workplace Reservation Management scheduled job **Reservation daily tasks** takes care of such reservations at the end of the day.

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

[Manage check-in and check-out reservations](check-in-check-out-process.md)

[Configure reservation multi-day settings in Reservable Module](rsv-config-rsv-mod-value.md)

