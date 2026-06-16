---
title: Healthcare Operations Core release notes
description: Version history for the Healthcare Operations Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-ops-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Healthcare Operations Core release notes

Version history for the Healthcare Operations Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.5.0 - June 2026**
    -   This release delivers platform-wide accessibility \(WCAG 2.2 AA\), security-directive access-control hardening, and a role-inheritance correction for Healthcare Operations Core.
        -   Security and Compliance
            -   WCAG 2.2 AA accessibility checkers: Added to Healthcare Operations Core to support automated accessibility validation.
            -   Automated WCAG 2.2 AA accessibility testing: Enabled across all Industry Verticals applications in this bundle.
            -   Non-Glide access control hardening: Audited and merged non-Glide ACL changes across Healthcare Operations Core.
            -   Care Team Work Management role boundary correction: The Care Team Work Management administrator role no longer inherits the Care Team Agent Manager persona role, restoring the expected role-model boundary between granular admin and persona roles.
            -   Operations Rounding accessibility checkers: Added WCAG 2.2 AA accessibility checkers to Operations Rounding.
-   **Version 2.3.0 - March 2026**
    -   Fixed:
        -   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow‑owned read‑only fields using g\_form.setValue\(\) or g\_form.clearValue\(\), refer toFor more information about granular read-only security options, see
        -   If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.
-   **Version 2.1.0 - December 2025**
    -   New:
        -   Leverage the streamlined launch context when embedding Care Team Portal into electronic medical record \(EMR\) systems.
        -   Assign roles and responsibilities more efficiently with an updated user configuration process.
-   **Version 2.0.0 - August 2025**

    Changed: Minor improvements were made to UI Actions, UI Policies, and client scripts in support of the new Care Team Operations for Facilities and Care Team Operations for Environmental Services applications.

-   **Version 1.2.0 - May 2025**

    Changed: The HCO core admin role has been granted the view\_changer role.

-   **Version 1.0.0 - February 2025**

    The ServiceNow Healthcare Operations Core application provides the foundation to enable hospitals to streamline and automate their operations.


**Parent Topic:**[ServiceNow Store - Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-healthcare-highlights.md)

