---
title: Retail Mobile release notes
description: Version history for the Retail Mobile application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-retail-mobile.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Retail version history release notes, ServiceNow Store version history release notes]
---

# Retail Mobile release notes

Version history for the Retail Mobile application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.4 - September 2026 \(Brazil\)**

    New: Java 21 compatibility

-   **Version 3.5.0 - September 2026 \(Australia\)**
    -   New:
        -   Integration with Strategic Portfolio Management \(SPM\) through which all store opening, closing, relocation and refurbishment project tasks to be performed at the store can be made visible to store employees on Retail mobile.
        -   Adds a Projects navigation entry to My Store and a Tasks segment to My Work when App SPM Retail is installed, surfacing customer\_project\_task records.
        -   Architecture: Added if/app-spm-retail/ conditional folder so all SPM-RO artifacts install only when App SPM Retail is present, with no runtime guard logic needed at the screen level.
    -   Changed: My Work: Reuses the existing unified My Work list with a new sys\_sg\_filter\_category pill targeting customer\_project\_task rather than introducing a separate list screen .
-   **Version 3.4.1 - August 2026**

    Changed: Added due date field on retail case card and retail task

-   **Version 3.3.0 - June 2026**
    -   New:
        -   Navigation and entry-point behaviour for taking and viewing questionnaires.
        -   Plugin structure, role placement, and configuration for Retail Questionnaire Mobile.
        -   Triggering of questionnaires from store task in Mobile.
        -   Close Task button visibility is now controlled by questionnaire completion status — the button is hidden until all required questionnaires are submitted.
-   **Version 3.2.0 - June 2026 \(Zurich\)**
    -   New:
        -   Navigation and entry-point behavior for taking and viewing questionnaires.
        -   Plugin structure, role placement, and configuration for Retail Questionnaire Mobile.
        -   Triggering of questionnaires from store task in Mobile.
        -   Close Task button visibility is now controlled by questionnaire completion status — the button is hidden until all required questionnaires are submitted.
-   **Version 3.1.0 - March 2026 \(Australia\)**

    New: Store Associates and Managers can fulfill assigned Store Tasks on "My Work".

-   **Version 3.0.0 - March 2026 \(Zurich\)**

    New: Store associates and managers can fulfil assigned store tasks from the My Work tab in Retail Mobile.

-   **Version 2.2.0 - August 2025**

    The Retail Mobile application offers a tailored mobile experience for retail operations, enabling frontline teams to efficiently manage store activities and resolve issues on the go.It provides real-time insights into key KPIs, supports issue tracking, and is compatible with both Android and iOS platforms.


**Parent Topic:**[ServiceNow Store - Retail version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-retail.md)

