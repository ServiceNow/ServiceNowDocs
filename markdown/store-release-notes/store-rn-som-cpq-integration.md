---
title: CPQ Integration release notes
description: Version history for the ServiceNow CPQ Integration application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-cpq-integration.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management version history release notes, ServiceNow Store version history release notes]
---

# CPQ Integration release notes

Version history for the ServiceNow® CPQ Integration application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.3 - September 2026**
    -   New: You can configure and manage ramped pricing that accommodates early contract termination, enabling more flexible quoting and contract management.
    -   Changed:
        -   Field mappings and their sources synchronize during blueprint sync, with more accurate quantity handling for picker-based products and improved identification of characteristics.
        -   Product synchronization tracks job status more accurately and reports status efficiently, ensuring sync processes complete successfully.
        -   Improved role assignment during initial configuration to ensure greater accuracy and consistency.
        -   Enhanced blueprint variable name generation removes special characters, preventing sync errors.
        -   Tenant URL entries are validated and sanitized during configuration, to ensure smoother and more secure setup experience.
        -   Implemented internal cleanup and expanded automated testing to improve reliability and reduce future regressions.
-   **Version 3.4.2 - August 2026**
    -   New: Support for early-termination ramp scenarios in quotes and contracts. Users can now configure and manage ramped pricing that accounts for early termination, enabling more flexible contract structures.
    -   Changed:
        -   Field mapping and characteristic sync improvements. Field mappings and their sources now sync during blueprint synchronization, with more accurate quantity handling for picker-based products and improved characteristic identification.
        -   Product sync reliability enhancements. Product synchronization jobs now provide improved status tracking, ensuring sync processes complete and report status dependably.
        -   Role assignment logic improvements during setup. The logic for assigning roles during initial setup has been refined to ensure more accurate and consistent role configuration.
    -   Fixed:
        -   Special characters are now stripped from generated blueprint variable names, preventing synchronization errors during blueprint generation.
        -   Tenant URL entries are now validated and sanitized during configuration, resulting in a smoother and more secure setup experience.
        -   Internal cleanup and expanded automated testing have improved overall performance and stability, reducing the likelihood of future regressions.
-   **Version 3.3.0 - July 2026**
    -   What's New
        -   Early termination ramps: Support early-termination ramp scenarios in your quotes and contracts
        -   Smarter characteristic field-mapping sync: Field mappings and their source now sync during blueprint sync, with more accurate quantity handling for picker-based products and improved characteristic identification
        -   More reliable product sync: improved job-status tracking so product sync completes and reports status dependably
        -   Improved role assignment: Refined logic for assigning roles during setup
    -   Fixes &amp; Improvements
        -   Cleaner blueprint generation: Special characters are now stripped from generated blueprint variable names, preventing sync errors
        -   More robust setup: Tenant URL entries are validated and sanitized during configuration for a smoother, more secure setup experience
        -   Performance &amp; stability hardening: Internal cleanup and expanded automated testing to improve reliability and reduce future regressions
-   **Version 3.2.1 - June 2026**
    -   New:
        -   Playbook experience for setting up the ServiceNow and Logik integration.
        -   Context variables synchronization from ServiceNow to the Rules Engine in the Configurator.
-   **Version 3.0.0 - March 2026**

    New: Improved user experience for attribute based configuration - Removed manual steps

-   **Version 2.1.0 - December 2025**

    The CPQ Integration application enables product catalog data synchronization between Sales and Order Management and the CPQ Configurator. The application provides a unified product catalog admin experience for defining the catalogs and serves as a gateway to launch the CPQ Configurator for the buy-time experience.


**Parent Topic:**[ServiceNow Store - Sales Customer Relationship Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-sales-order-management-highlights.md)

