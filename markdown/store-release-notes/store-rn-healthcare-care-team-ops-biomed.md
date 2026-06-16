---
title: Care Team Operations for Biomed release notes
description: Version history for the Care Team Operations for Biomed application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-care-team-ops-biomed.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Care Team Operations for Biomed release notes

Version history for the Care Team Operations for Biomed application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.6.0 - June 2026**
    -   This release delivers platform-wide accessibility \(WCAG 2.2 AA\) and security-directive access-control hardening for Care Team Operations for Biomed.
        -   Security and Compliance
            -   WCAG 2.2 AA accessibility checkers: Added to Care Team Operations for Biomed to support automated accessibility validation.
            -   Automated WCAG 2.2 AA accessibility testing: Enabled across all Industry Verticals applications in this bundle.
            -   Non-Glide access control hardening: Audited and merged non-Glide ACL changes across Care Team Operations for Biomed.
-   **Version 2.4.0 - March 2026**
    -   Fixed:
        -   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow‑owned read‑only fields using g\_form.setValue\(\) or g\_form.clearValue\(\), refer toFor more information about granular read-only security options, see
        -   If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.
-   **Version 2.1.0 - December 2025**
    -   New:
        -   Roles and responsibilities are updated to allow for more selective user access
            -   The following responsibilities were added:
                -   Support department agent
                -   Support department manager
            -   Users can be assigned these responsibilities in the Edit member related list within healthcare organizations.
-   **Version 2.0.0 - August 2025**
    -   New:
        -   Added new service catalog named Biomed Service.
            -   Realigned existing Biomed service categories and catalog items to the new Biomed Service catalog.
-   **Version 1.2.0 - May 2025**
    -   Changed:
        -   Service catalog improvements
            -   Published service catalog specific to Care Team Operations for Biomed and migrated record producers into the scoped app.
-   **Version 1.0.0 - February 2025**

    The ServiceNow Care Team Operations for Biomed application is built on the Healthcare Operations Core application and contains case types, record producers, and flows designed to enable care teams to report medical device and other biomed related issues. For organizations that own Clinical Device Management or Field Service Management, the out of the box flows synchronizes data between the case and work order, allowing biomed technicians to work with work orders to fulfill their care teams corrective maintenance requests.


**Parent Topic:**[ServiceNow Store - Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-healthcare-highlights.md)

