---
title: Care Team Portal release notes
description: Version history for the Care Team Portal application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-care-team-portal.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Care Team Portal release notes

Version history for the Care Team Portal application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.3.0 - June 2026**
    -   This release delivers a menu visibility and layout fix, platform-wide accessibility \(WCAG 2.2 AA, 400% zoom/reflow\), and security-directive access-control hardening for the Care Team Portal.
        -   Fixed: Menu visibility and layout: Resolved menu visibility and layout issues on the Care Team Portal.
        -   Security and Compliance
            -   Care Team Portal accessibility checkers: Added WCAG 2.2 AA accessibility checkers to the Care Team Portal.
            -   Automated WCAG 2.2 AA accessibility testing: Enabled across all Industry Verticals applications in this bundle.
            -   WCAG 2.2 AA compliance and 400% zoom/reflow support: Delivered across Care Team Portal pages and widgets.
            -   Non-Glide access control hardening: Audited and merged non-Glide ACL changes across the Care Team Portal.
-   **Version 2.2.0 - March 2026**
    -   Fixed:
        -   Catalog Access Fix: Fixed catalog and category access for care team members when the glide.sc.use\_user\_criteriaproperty is disabled.
        -   Portal Header/Footer Cleanup: Removed admin-dependent code from care team portal header/footer records that referenced an unowned performance widget.
        -   Case Resolution Acceptance Error: Fixed an issue where case resolution acceptance on the Care Team Portal was throwing an 'AisDisableSearchSignalEvent' error.
-   **Version 2.1.0 - December 2025**
    -   Fixed:
        -   The process for embedding Care Team Portal into your EMR system has been streamlined to enable more efficient launch context configuration.
            -   The portal now supports capturing launch context tokens across multiple launches within the same Hyperspace session when embedding Care Team Portal into Epic's Hyperspace. Previously, tokens were only captured during the first launch of a given session.
        -   The FHIR endpoint is now retrieved dynamically, eliminating the need to embed it directly in the Single Sign-on Script.
        -   Care Team Portal now supports access for snc\_external users.
            -   snc\_external users will only have access to Care Team Ops for Healthcare IT to be support the Community Connect use case.
-   **Version 2.0.0 - August 2025**
    -   New:
        -   Added Care Team Portal support for:
            -   Care Team Operations for Facilities
            -   Care Team Operations for Environmental Services
-   **Version 1.2.0 - May 2025**
    -   Changed:
        -   Service Catalog Enhancements
            -   Record producers were moved into their respective service catalogs specific to their scoped apps.
-   **Version 1.0.1 - February 2025**

    The Care Team Portal provides a responsive portal experience that can be used by care teams in the hospitals to report and track issues for support services departments. This experience can be used on a standalone portal or embedded in EMR systems.


