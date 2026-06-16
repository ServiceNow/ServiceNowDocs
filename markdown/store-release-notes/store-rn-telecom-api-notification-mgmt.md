---
title: API Notification Management release notes
description: Version history for the API Notification Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-api-notification-mgmt.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Telecommunications Service Management release notes, ServiceNow Store release notes]
---

# API Notification Management release notes

Version history for the API Notification Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.1.1 - March 2026 \(Australia\)**

    Fixed: Security fixes for sql injection, unescaped json string

-   **Version 4.1.0 - January 2026**

    Fixed: Product/Service Order State Change Notification was fixed to trigger correctly whenever there is a state change in customer orders.

-   **Version 4.0.1 - December 2025**
    -   Enhanced the existing Order Management APIs to support Notifications. Key notifications supported are as follow:
        -   TMF 622 API
            -   Cancel Product Order State Change Event
            -   Cancel Product Order Create Event
            -   Product Order State Change Event
            -   Product Order Jeopardy Alert Event
            -   Product Order Create Event
            -   Product Order Delete Event
        -   TMF 641 API
            -   Cancel Service Order State Change Event
            -   Cancel Service Order Create Event
            -   Service Order State Change Event
            -   Service Order Jeopardy Alert Event
            -   Service Order Create Event
            -   Service Order Delete Event
-   **Version 3.0.1 - August 2025**

    No new feature, Enable support for Zurich Family changes for the platform.

-   **Version 2.5.0 - February 2025**

    No changes in this version 2.5.0.

-   **Version 2.1.0 - August 2024**

    Minor improvements to our API notification management inline with the external trigger IH changes to support header and query parameter in the trigger definition.

-   **Version 2.0.0 - February 2024**
    -   New
        -   Producer Notification framework which could use hermes, Kafka, or any other open message bus
        -   Provided support of Trouble ticket notification using the above framework
        -   Localization support
-   **Version 1.0.0 - November 2023**

    API Notification Management is an event driven architecture management that supports Pub/Sub type event processing.


**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

