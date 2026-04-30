---
title: Configure reservation multi-day settings in Reservable Module
description: Set the Max days in future value for configuring reservation.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2025-11-12"
reading_time_minutes: 5
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure reservation multi-day settings in Reservable Module

Set the Max days in future value for configuring reservation.

The option to create a multi-day reservation is configured by your administrator using the **Max days for multi-day** Reservable Module Configuration property. For more information, see [Configure a reservable module](../task/config-reservable-module.md). Multi-building selection is supported for multi-day reservation. For more information about multi-day reservation, see [Create a multi-day reservation](../task/create-multi-day-reservation.md).

For multi-day reservation covering multiple days, the start date and end date span across multiple days \(for example, Start date: October 12, 2023. End date: October 17, 2023\). For more information, see [Create a multi-day reservation](../task/create-multi-day-reservation.md).

-   If your administrator has set a limit on the maximum days that you can reserve in future, you can’t select days in the future beyond the set the date by the admin. A warning is displayed about the limitation.
-   For example, if your administrator has limited the days of future to 45 days, you can’t select a date beyond 45 days while making a recurring reservation. The number of days available for **End on this date** option differs based on the **Daily**, **Weekly**, or **Monthly** selections. The end date and time specified for recurring reservation are used to indicate the end date and time of the reservation.
-   If no such limitation is set by your administrator on the future days in the Reservable module, you can select any date. This also depends on how many occurrences you can select and make.

    **Note:** You can't select a date beyond a duration that is configured in the Max days in the future reservable module. For example, if Max days in future value are 45, you can’t select a date beyond this duration while making a recurring reservation. The number of days available for **End on this date** option differs based on the **Daily**, **Weekly**, or **Monthly** selections. If the **Max days in future** value isn’t configured on the Reservable module, the date selection isn’t restricted and employees can select a date based on the **Max number of occurrences** configuration.


Space and reservation planners \(sn\_wsd\_rsv.reservation\_planner\) with the dedicated role \(sn\_wsd\_rsv.bypass\_module\_validation\) can ignore or bypass certain settings in the Reservable module configuration. For more information, see [Allow Event planners to handle reservations with more flexibility](../../workplace-central/concept/event-planner-bypass-validation-rule-overview.md).

For example, reservation planners or space planners with the dedicated role \(sn\_wsd\_rsv.bypass\_module\_validation\) can ignore or bypass the following settings in the Reservable module:

-   Max days in the future
-   Max number of occurrence
-   Min and Max duration
-   Available in
-   All day

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

[Configure automatic check-in for reserved spaces](configure-rsv-check-in.md)

