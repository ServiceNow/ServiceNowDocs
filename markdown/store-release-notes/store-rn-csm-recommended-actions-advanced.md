---
title: Recommended Actions - Advanced release notes
description: Version history for the Recommended Actions - Advanced application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-recommended-actions-advanced.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# Recommended Actions - Advanced release notes

Version history for the Recommended Actions - Advanced application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.0.0 - June 2026**
    -   New:
        -   Java 21 compile upgrade – The Recommended Actions application has been upgraded to compile with Java 21, ensuring platform compatibility and performance improvements.
        -   Role inheritance &amp; ACL review in the base system – Role inheritance and ACL configurations in the base system have been reviewed and aligned for subscription-based access control.
        -   Accessibility \(A11y\) improvements – Core UI and seismic components now meet WCAG 2.2 AA standards, including 400% zoom and reflow support for improved accessibility compliance.
        -   Agentic Workflow Enhancement – Dynamic search terms can now be passed as Guidance input to support agentic workflow execution in Recommended Actions.
-   **Version 13.0.1 - March 2026**
    -   New: The total number of search results is displayed in the AI search tab of the Recommended Actions Contextual side panel when Hybrid Search is enabled.
    -   Fixed: Minor fixes for this release.
-   **Version 12.0.1 - December 2025**

    Fixed: Minor fixes for this release.

-   **Version 11.0.2 - September 2025**
    -   Fixed:
        -   The field recommendations now display correctly upon page refresh.
        -   The search results now update correctly when you select a source or facet filters on the Search page.
        -   The default timeout for similarity resource generator has been increased.
-   **Version 11.0.1 - August 2025**
    -   Improved the TI/ML error logs to identify issues in the RA x TI/ML integration.
    -   Minor bug fixes for this release.
-   **Version 10.0.2 - May 2025**

    New: Added more support for logging in task intelligence resource generator type.

-   **Version 9.0.1 - February 2025**

    Added threshold on timeout of ML prediction API calls when called from recommended actions framework via system property.

-   **Version 8.0.2 - November 2024**
    -   Added TI Similarity with Trend resource generator type
    -   Update RA resource generator for TI similarity to handle different input/output tables
-   **Version 7.0.2 - August 2024**
    -   New Resource Generator Type for TIAC Similarity.
    -   Authoring changes for configuring Resource Generator.
    -   Implementation to show active/staging solutions for Similarity/Classification.
-   **Version 6.0.0 - February 2024**

    Changes to Task Intelligence Classification \(TIC\) Resource Generator to support Top N Results for classification rules.

-   **Version 5.0.0 - November 2023**

    Uptake schema change to support simplified TI admin console flow. Allows Monitor Only configuration for each output field of Task intelligence models.

-   **Version 4.0.0 - August 2023**
    -   Changes to Task Intelligence Classification \(TIC\) Resource Generator to track prediction results.
    -   Changes to handle background monitoring modes for the TIC models.
    -   Fixes for Similarity-based resource generator.
-   **Version 3.0.0 - May 2023**
    -   Added support for the new resource generator of type Task Intelligence Classification.
    -   Fixes.
-   **Version 2.0.0 - November 2022**

    Fixes

-   **Version 1.0.0 - August 2022**

    Recommended Actions - Advanced enables users to create recommendations based on Artificial Intelligence/Machine Learning models that were created using ServiceNow Predictive Intelligence.


**Parent Topic:**[ServiceNow Store - Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

