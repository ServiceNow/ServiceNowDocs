---
title: Create a workplace service to provide an extra service for a reservation
description: Create a workplace service and provide it as an extra service to employees while making a reservation. Use the Workplace Case Management application to create the workplace service.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a workplace service to provide an extra service for a reservation

Create a workplace service and provide it as an extra service to employees while making a reservation. Use the Workplace Case Management application to create the workplace service.

## Before you begin

Ensure that you have the following:

-   Have the Workplace Case Management application installed.
-   Task templates and Case templates to link to the workplace service.
-   Record producer to link to the workplace service.
-   Active flows in case you want to create a workplace service flow.

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## About this task

To understand workplace services and the workplace service-related options, refer to [Workplace Services](../../workplace-case-mgmt/concept/workplace-services.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Workplace services**.

2.  Click **New**.

3.  On the form, fill in the fields.

    For a description of the field values, see [Workplace Service form](../../workplace-case-mgmt/reference/workplace-service-form.md).

4.  Click **Submit**.


## Result

The workplace service is created and will be available to employees as an extra service.

When an employee requests an extra service, a workplace case is created in the Workplace Case Management application. If the extra service is modified by the employee, then the existing workplace case is canceled and a new workplace case is again created with the modified details.

## What to do next

-   If the extra service requires an employee to select from a list of options, then you must add those options as workplace service items to the workplace service. To add workplace service items, refer to the following:
    -   [Add a workplace service item to a workplace service](../../workplace-case-mgmt/task/add-workplace-service-items.md).
    -   [Make a workplace service item available to a workplace location](../../workplace-case-mgmt/task/add-workplace-service-item-to-workplace-locs.md).
-   To view the workplace cases, navigate to **Workplace Case Management** &gt; **Workplace Cases**.
-   You can also view the reservation details of a Workplace case. To view the details, perform the following actions:
    1.  Right-click the form header.
    2.  Select **View** &gt; **Reservation View**.

        In the **Reservation view**, you can view details such as the reservation and comments added by the employee while requesting an extra service.

-   You can also view the extra service cases and tasks in the Workplace Reservation Management application.
    -   To view the cases, navigate to **Workplace Reservation Management** &gt; **Reservation Overview** &gt; **Extra Service Cases**.
    -   To view the tasks created for the cases, navigate to **Workplace Reservation Management** &gt; **Reservation Overview** &gt; **Extra Service Tasks**.

**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Configure a reservable module](config-reservable-module.md)

[Assign spaces to an area](add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](add-standard-services.md)

[Create a flexible service](add-flexible-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

