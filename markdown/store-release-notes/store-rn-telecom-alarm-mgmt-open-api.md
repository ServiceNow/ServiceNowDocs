---
title: Telecommunications Alarm Management Open API release notes
description: Version history for the Telecommunications Service Management Telecommunications Alarm Management Open API on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-alarm-mgmt-open-api.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Telecommunications Service Management release notes, ServiceNow Store release notes]
---

# Telecommunications Alarm Management Open API release notes

Version history for the Telecommunications Service Management Telecommunications Alarm Management Open API on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.0.0 - March 2026 \(Australia\)**

    Fixed: Security fixes for sql injection, unescaped json string

-   **Version 7.1.0 - January 2026**

    Removed: Update Incident Open API Flow in Telecommunication Alarm Management Open API, which was in draft status, was been removed from the workflow list.

-   **Version 7.0.1 - December 2025**

    Re-certified the Alarm Management API to the latest TMF compliance of v5.

-   **Version 6.0.0 - August 2025**

    No new feature, Enable support for Zurich Family changes for the platform.

-   **Version 5.5.0 - February 2025**
    -   Fixed:
        -   i18 fixes
        -   Localisation changes
        -   Demo data fixes
-   **Version 5.1.0 - August 2024**

    We made changes to support changes done by external trigger on which we are dependent for new event based alarm management.

-   **Version 5.0.0 - February 2024**

    New: Localisation support.

-   **Version 4.0.1 - November 2023**
    -   New:
        -   Introduce incoming notification support for the Alarm Management Open API.
        -   Pub/Sub: Define API to receive the topics from external systems.
        -   Alarm Event API for inbound should be as per TMF 688 definition \(attribute level details\).
        -   \{On-Cloud\} Hermes messaging service and Kafka stream connect for On Cloud customer to consume Alarm API
-   **Version 3.0.0 - August 2023**

    Dependent app - no changes.

-   **Version 2.0.1 - November 2022**

    Changed: Internal optimization to align to NOW engineering standards

-   **Version 2.0.0 - August 2022**

    Changed: Updated APIs to support pagination and make it TMF conformant.

-   **Version 1.1.8 - May 2022**

    Fixed: Fixed a compatibility issue caused by an underlying application dependancy

-   **Version 1.1.0 - February 2022**

    New: Added additional validation and extensibility support to the Alarm Management Open API

-   **Version 1.0.4 - December 2021**

    Changed: Telecom core dependency version update

-   **Version 1.0.3 - October 2021**

    New: REST extensions enabling users to add support for additional inbound actions, additional validation of inbound payloads, and additional field mapping from an inbound payload.

-   **Version 1.0.2 - March 2021**

    Fixed: Fix to allow the application to be installed on an instance by any user with the admin role

-   **Version 1.0.0 - December 2020**

    The Telecommunications Alarm Management Open API application is an implementation of the TMForum TMF642 Alarm Management Open API specification.


**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

