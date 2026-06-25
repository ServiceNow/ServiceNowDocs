---
title: Connect Workplace Reservation Management with Zoom
description: Establish connection between Zoom and Workplace Reservation Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/connect-rsv-mtm-with-zoom.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
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

    Refer to the Create a connected app in Zoom topic in [Set up the](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/setup-zoom.md)

    **Note:** While setting up zoom, ensure the following:

    -   Copy the url specified in **Redirect URL for OAuth** to **Add allow list** as well.
    -   Select the following scopes:
        -   In **Meeting**, select the following:
            -   **View and manage sub account’s users meetings \(meeting: master\)**
            -   **View and manage all user meetings \(meeting:write:admin\)**
        -   In **Recording**, select **View all users recordings \(recording:read:admin\)**
    .

2.  [Setup OAuth connectivity between ServiceNow and Zoom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/setup-connectivity-between-servicenow-and-zoom.md).

3.  [Create connection and credential for Zoom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-connection-and-credentials-for-zoom.md).


1.  [Setup OAuth connectivity between ServiceNow and Zoom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/setup-connectivity-between-servicenow-and-zoom.md)  
Register Zoom with ServiceNow instance for OAuth authorization to get create virtual meetings and get recordings after a virtual meeting.
2.  [Create connection and credential for Zoom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-connection-and-credentials-for-zoom.md)  
Setup connection and credentials alias for Zoom.

**Parent Topic:**[Configure Workplace Reservation Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management]()

[Add a workplace space for reservation]()

[Add a workplace room for reservation]()

[Configure a reservable module]()

[Assign spaces to an area]()

[Create a standard service]()

[Create a flexible service]()

[Create a workplace service to provide an extra service for a reservation]()

[Create a reservable view]()

[Create a user criteria record]()

[Configure a reservable purpose]()

[Create a quick reservation time slot]()

[Configure virtual meeting providers]()

[Configure Microsoft Teams as virtual meeting provider]()

[Connect Workplace Reservation Management with Microsoft Teams]()

[Display permanent seat assignments on floor maps]()

[Display name of the person reserving a space]()

[Manage check-in and check-out reservations]()

[Configure automatic check-in for reserved spaces]()

[Configure reservation multi-day settings in Reservable Module]()

