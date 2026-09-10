---
title: Unified Content Management release notes
description: Version history for the ServiceNow Unified Content Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-unified-content-mgmt.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance version history release notes, ServiceNow Store version history release notes]
---

# Unified Content Management release notes

Version history for the ServiceNow® Unified Content Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 23.0.5 - September 2026 \(Brazil\)**
    -   New:
        -   Regulatory content updates are now delivered dynamically via Content Delivery Service \(CDS\), decoupling content from UCM application upgrades Administrators can receive the latest regulatory framework content automatically, without manual upgrades or reconciliation.
        -   Plugin compatibility filtering is now supported for UCM contentThe system evaluates whether content is compatible with the current instance based on plugin and version requirements, ensuring only relevant content is installed.
        -   Error handling and rollback for content imports are now supportedFailed installs aggregate errors and roll back partial inserts, with error details visible in the UI.
        -   Admins can now highlight AI-assisted records with an AI icon in list viewsRecords generated via AI are visually distinguished for easier identification.
        -   Zurich platform support is restored for Cobalt Raven ACLsACLs have been restructured to enable compatibility with both Zurich and Australia platforms.
        -   Boolean values and authority document handling for AI risk and compliance content have been correctedContent for these domains is now accurately captured and processed.
    -   Changed:
        -   Parent-staging tables now include plugin compatibility columnsNew fields for target plugin, minimum, and maximum compatible version are added, inherited by child tables, with existing records unaffected.
        -   CDS client-side changes enable automated data synchronization from CDS ServerInstances with UCM plugin can now pull content and store it in pre-staging tables, with updated ACLs for enhanced security.
        -   UI actions for extracting and verifying pre-staging records are now availableAdmins can validate content preparation directly from the interface.
-   **Version 22.4.0 - July 2026 \(Australia\)**

    New Content support for the OSFI framework within the Audit and Compliance workspace.

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   Changed: This release includes security enhancements that strengthen access controls across the application.
    -   Fixed:
        -   SAE template import failure
        -   Fixed an issue where importing SAE templates was failing due to an incorrect display value setting.
-   **Version 22.0.1 - March 2026**
    -   Added guided tour for content management pages.
    -   Fixed accessibility issues for the content management home page.
    -   Fixed minor UI issues.
-   **Version 21.1.2 - December 2025**

    Unified Content Management is a modular content delivery application that streamlines and accelerates the deployment of foundational content across ServiceNow Risk and ESG applications.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

