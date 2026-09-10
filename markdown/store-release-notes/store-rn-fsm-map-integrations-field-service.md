---
title: Map Integrations for Field Service release notes
description: Version history for the ServiceNow Map Integrations for Field Service application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fsm-map-integrations-field-service.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Field Service Management version history release notes, ServiceNow Store version history release notes]
---

# Map Integrations for Field Service release notes

Version history for the ServiceNow® Map Integrations for Field Service application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 30.0.4 - September 2026**
    -   New: This version is compatible with Brazil Family Release.
    -   Changed:
        -   Invalid coordinates are now stripped before sending requests to map providers and allowing valid entries.
        -   If all coordinates are invalid, an error is returned early instead of forwarding an empty request.
-   **Version 29.0.8 - March 2026**
    -   Map Integrations for Field Service lets organizations connect a travel estimate provider to FSM, improving the accuracy of travel time estimates used in scheduling and task assignment.
    -   Beans.ai is supported out of the box, providing more precise travel time estimates and automatically excluding locations that fail geocoding validation or aren't reachable by road. Third-party map providers are also supported using the same configuration process, with credentials and API authentication handled at setup.
    -   More accurate travel estimates mean better scheduling windows, cleaner assignments, and fewer surprises in the field.

**Parent Topic:**[ServiceNow Store - Field Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fsm-highlight.md)

