---
title: Workplace Services Kiosk release notes
description: Version history for the Workplace Services Kiosk application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-services-kiosk.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Services Kiosk release notes

Version history for the Workplace Services Kiosk application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.4 - June 2026**
    -   Fixed:
        -   Fixed an issue with displaying additional check-in options.
        -   Improved validation for Kiosk input fields.
        -   Fixed an issue with camera configuration on devices without a camera.
-   **Version 1.5.2 - December 2025**
    -   New: Added the ability to book a space from a map. See release notes for Workplace Indoor Mapping 1.17.4.
    -   Changed: Moved the language selector to the kiosk header to support single app mode.
    -   Fixed: Added support for special characters when validating names during kiosk visitor check-in.
-   **Version 1.4.2 - September 2025**

    Fixed: The Revert to Homepage property now supports values under 60 seconds for faster return after inactivity.

-   **Version 1.4.1 - August 2025**
    -   New: Added a distance unit field to define the default unit displayed for wayfinding for all kiosks.
    -   Fixed: Resolved issue with the logo size not displaying properly in the kiosk header.
-   **Version 1.3.0 - May 2025**
    -   New:
        -   Camera access is now supported for flows that require the use of the device camera.
        -   Operator experience and notification system for granting camera device access.
        -   Signing capabilities for flows that require a signature.
-   **Version 1.2.0 - February 2025**
    -   New: The kiosk portal now supports the Indoor Mapping application
    -   Changed: The last alive field was moved to another table as it was constantly updating the updated\_by and updated\_at fields of the kiosk records.
-   **Version 1.1.0 - November 2024**

    Fixed issues with translation.

-   **Version 1.0.2 - August 2024**

    Workplace Services Kiosk provides a new kiosk portal and a UI for Workplace Service Delivery features. The initial August '24 release focuses on Visitor Management Kiosk features, including self check-in, self check-out and self registration which require the Visitor Management App. Future releases will expand capabilities.


