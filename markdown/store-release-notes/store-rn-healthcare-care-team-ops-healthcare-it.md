---
title: Care Team Operations for Healthcare IT release notes
description: Version history for the Care Team Operations for Healthcare IT application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-care-team-ops-healthcare-it.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Care Team Operations for Healthcare IT release notes

Version history for the Care Team Operations for Healthcare IT application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.6.0 - June 2026**
    -   This release delivers platform-wide accessibility \(WCAG 2.2 AA, 400% zoom/reflow\) and security-directive access-control hardening for Care Team Operations for Healthcare IT.
        -   Security and Compliance
            -   WCAG 2.2 AA accessibility checkers: Added to Care Team Operations for Healthcare IT to support automated accessibility validation.
            -   Automated WCAG 2.2 AA accessibility testing: Enabled across all Industry Verticals applications in this bundle.
            -   WCAG 2.2 AA compliance and 400% zoom/reflow support: Delivered across Healthcare IT forms, lists, and agent workspaces.
            -   Non-Glide access control hardening: Audited and merged non-Glide ACL changes across Care Team Operations for Healthcare IT.
-   **Version 2.4.0 - March 2026**
    -   Fixed:
        -   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow‑owned read‑only fields using g\_form.setValue\(\) or g\_form.clearValue\(\), refer toFor more information about granular read-only security options, see
        -   If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.
-   **Version 2.1.0 - December 2025**

    Fixed: When a Healthcare IT case is created through the workspace the Incident will now be properly linked to the case.

-   **Version 2.0.0 - August 2025**
    -   New:
        -   Added new service catalog named Healthcare IT.
            -   Realigned existing Healthcare IT service categories and catalog items to the new Healthcare IT catalog.
-   **Version 1.2.0 - May 2025**
    -   Changed:
        -   Service catalog improvements
            -   Published service catalog specific to Care Team Operations for Healthcare IT and migrated record producers into the scoped app.
        -   Epic Hyperspace Support
            -   Improved SMART on FHIR EHR launch support to include capturing tokens from the oAuth launch context.
-   **Version 1.0.0 - February 2025**

    The ServiceNow Care Team Operations for Healthcare IT application contains case types, record producers, and flows designed to enable care teams to report EMR and other IT related issues. The out of the box flows synchronizes data between the Healthcare IT case and Incidents, allowing technicians to work with incidents to fulfill their care teams reported issues while providing care teams with visibility into all of the issues reported by members of their team.


