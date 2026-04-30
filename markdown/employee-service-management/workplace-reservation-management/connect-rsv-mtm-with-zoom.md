---
title: Connect Workplace Reservation Management with Zoom
description: Establish connection between Zoom and Workplace Reservation Management.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Connect Workplace Reservation Management with Zoom

Establish connection between Zoom and Workplace Reservation Management.

## Before you begin

Ensure that the following plugins are installed:

-   Zoom spoke
-   ServiceNow Integration Hub Action Template - Data Stream \(for getting recordings\)
-   Workplace Reservation Management

Role required: admin

## Procedure

1.  Setup Zoom to enable virtual meeting.

    Refer to the Create a connected app in Zoom topic in [Set up the](https://www.servicenow.com/docs/access?context=setup-zoom&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

    **Note:** While setting up zoom, ensure the following:

    -   Copy the url specified in **Redirect URL for OAuth** to **Add allow list** as well.
    -   Select the following scopes:
        -   In **Meeting**, select the following:
            -   **View and manage sub account’s users meetings \(meeting: master\)**
            -   **View and manage all user meetings \(meeting:write:admin\)**
        -   In **Recording**, select **View all users recordings \(recording:read:admin\)**
    .

2.  [Setup OAuth connectivity between ServiceNow and Zoom](setup-connectivity-between-servicenow-and-zoom.md).

3.  [Create connection and credential for Zoom](create-connection-and-credentials-for-zoom.md).


1.  [Setup OAuth connectivity between ServiceNow and Zoom](setup-connectivity-between-servicenow-and-zoom.md)  
Register Zoom with ServiceNow instance for OAuth authorization to get create virtual meetings and get recordings after a virtual meeting.
2.  [Create connection and credential for Zoom](create-connection-and-credentials-for-zoom.md)  
Setup connection and credentials alias for Zoom.

**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Configure a reservable module](config-reservable-module.md)

[Assign spaces to an area](add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](add-standard-services.md)

[Create a flexible service](add-flexible-service.md)

[Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

