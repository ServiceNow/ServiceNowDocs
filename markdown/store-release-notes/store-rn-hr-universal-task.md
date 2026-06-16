---
title: Universal Task release notes
description: Version history for the Universal Task application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-universal-task.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Universal Task release notes

Version history for the Universal Task application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.8.0 - June 2026**
    -   Fixed:
        -   Improved performance of the Universal Task survey result restriction logic by eliminating large result-set queries.
        -   Localized the "--None--" label in the Universal Task Employee Form configuration.
        -   Empty choice field values from a source record no longer copy as "null" when creating a Universal Task from a template.
        -   Enabled arrow-key navigation within the Universal Task list widget on the Standard Ticket page.
        -   Submitting a "Submit catalog item" Universal Task from a saved draft now correctly transitions the task to Complete.
-   **Version 2.7.0 - December 2025**

    Fixed: Minor security enhancements.

-   **Version 2.6.2 - August 2025**

    New: The Universal Task will now support a new 'URL' task type.

-   **Version 2.5.0 - November 2024**

    New: Sandbox access for Client-Callable Script Includes.

-   **Version 2.4.1 - August 2024**

    Fixed closed date issue for a reopened task.

-   **Version 2.4.0 - May 2024**
    -   The tasks assigned through Universal Task are now accessible to the external users \(snc\_external\) and they can perform the following actions:
        -   Upload Document
        -   Collect Employee Input
        -   Mark When Complete
        -   Checklist
-   **Version 2.3.0 - February 2024**

    Universal Tasks components can be created and managed using UIB as part of the Service Operations Workspace \(SOW\).

-   **Version 2.2.2 - January 2024**

    Misconfiguration of table/field ACLs within the com.snc.universal\_task plugin is resolved now.

-   **Version 2.2.1 - August 2023**

    Fixed To-do filters for universal Task.

-   **Version 2.2.0 - February 2023**
    -   New: Support for Next Experience theming on Mobile
    -   Fixed: Universal Task Submit Catalog Item widget load issue
-   **Version 2.1.0 - August 2022**
    -   New: Added assignment group field in the task form
    -   Changed: Updated email template notifications to match the Next Experience theme.
-   **Version 2.0.2 - July 2021**

    Fixed: Minor updates

-   **Version 2.0.1 - May 2021**
    -   New:
        -   New task types - Collect Employee Input, Checklist, Mark When Complete
        -   Universal task templates \(static and dynamic\) for autopopulating fields in Universal task records and scheduling task creation periodically
-   **Version 1.0.6 - February 2021**
    -   New:
        -   Two task types - Submit Catalog Item, Upload Document
        -   Out of box Now Mobile experience.
        -   Out of box support for To-Do configurations in ESC.
        -   Out of box support for Standard Ticket Page.

