---
title: GRC: Crisis map release notes
description: Version history for the GRC: Crisis map application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-crisis-map.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Crisis map release notes

Version history for the GRC: Crisis map application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.1 - June 2026 \(Australia\)**
    -   Fixed:
        -   Issues with zooming in the Crisis map have been resolved. Users can now zoom in and out on the Crisis map without encountering errors or unexpected behavior.
        -   The Crisis map no longer accumulates multiple radius impact areas when switching between alerts. Each alert now displays only its relevant impact area.
        -   The location search on the Crisis Map now correctly applies the resource configuration filter. Search results are limited to locations that match the configured resources.
-   **Version 10.0.1 - March 2026**

    Defect fixes in search and filters.

-   **Version 9.1.2 - December 2025 \(Zurich\)**
    -   Fixed:
        -   Cancel button not working after selecting to declare a crisis event
        -   Localization issue
-   **Version 9.0.3 - September 2025**

    Fixed: Restored the ability to customize impacted areas for alerts on crisis map, including support for custom shapes, editing, and reverting changes.

-   **Version 9.0.1 - August 2025**
    -   Updated: Optimized Crisis map to handle over 10,000 resources and 1,000 alerts
    -   Fixed: Assets are not auto-populated when declaring an event from Crisis map
-   **Version 8.1.1 - May 2025**
    -   Changed: Design change for "Search Location" to resolve accessibility findings
    -   Fixed:
        -   Tab labels in Crisis Map overlaps with description text \(workspace\)
        -   Crisis map caching issues for:
            -   After declaring crisis, the alert does not refresh and has no alert message
            -   The modal to notify crisis and declare crisis is cached when reopening
            -   For dismiss-reopen alert on alert details
        -   Crisis map localization gaps for "Alert subscribed"
        -   Accessibility issues on button with no accessible text
        -   Crisis Map fails to load Associates when the count exceeds 50K
-   **Version 8.0.6 - February 2025**

    Changed: Updated map component to Geo map, the Next Experience component.

-   **Version 7.0.1 - August 2024**
    -   Fixed:
        -   Fixed tile icon for UI Builder
        -   Fixed accessibility WCAG 2.1AA gaps
-   **Version 6.0.0 - February 2024**
    -   Fixed:
        -   Fixed error message for a required empty short description
        -   Fixed to use updated short description when declaring a crisis event
-   **Version 2.0.4 - August 2023**

    New: Added crisis map to new BCM next experience workspace.

-   **Version 1.1.2 - March 2022**

    New: Enabled multi-language support and included translations.

-   **Version 1.0.1 - June 2021**
    -   New:
        -   Application with the following capabilities
        -   View the critical assets and threat alerts in geo-map
        -   Notify the stakeholders responsible for the impacted assets
        -   Declare Crisis Events to be tracked in BCM to monitor the recovery progress

**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

