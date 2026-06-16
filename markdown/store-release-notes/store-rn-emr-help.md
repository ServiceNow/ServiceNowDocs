---
title: EMR Help release notes
description: Version history for the EMR Help application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-emr-help.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# EMR Help release notes

Version history for the EMR Help application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.5.0 - June 2026**
    -   This release delivers platform-wide accessibility \(WCAG 2.2 AA, 400% zoom/reflow\), security-directive access-control hardening, and subscription-alignment role changes for EMR Help — including a new EMR Help Fulfiller role and a refined Requester role for tighter entitlement tracking.
    -   Security and Compliance
        -   EMR Help accessibility checkers: Added WCAG 2.2 AA accessibility checkers to EMR Help to support automated accessibility validation.
        -   Automated WCAG 2.2 AA accessibility testing: Enabled across all Industry Verticals applications in this bundle.
        -   WCAG 2.2 AA compliance and 400% zoom/reflow support: Delivered across EMR Help forms, lists, and request flows.
        -   Non-Glide access control hardening: Audited and merged non-Glide ACL changes across EMR Help.
        -   Subscription alignment — access control gap fixes: Fixed access control gaps in EMR Help to align permissions with subscription entitlement boundaries.
        -   New EMR Help Fulfiller role: Introduced a dedicated Fulfiller role \(inheriting Viewer permissions\) so administrators can accurately track EMR Help fulfiller entitlements in subscription management.
        -   EMR Help Requester role refinement: The EMR Help Requester role no longer inherits Service Organization Contributor or Customer Service Consumer Contributor permissions, keeping the Requester role scoped to its intended permission set.
        -   EMR Portal accessibility checkers: Added WCAG 2.2 AA accessibility checkers to the EMR Portal.
-   **Version 5.3.0 - March 2026**
    -   Fixed:
        -   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow‑owned read‑only fields using g\_form.setValue\(\) or g\_form.clearValue\(\), refer toFor more information about granular read-only security options, see
        -   If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.
-   **Version 5.1.0 - December 2025**

    Fixed: Minor correction to the login page.

-   **Version 5.0.0 - August 2025**

    Changed: True-up to Zurich release.

-   **Version 4.0.0 - August 2024**

    New: Added minor improvements to true up to the Xanadu release.

-   **Version 3.0.0 - May 2024**
    -   Changed:
        -   EMR Help has been enhanced to utilize Column Level Encryption Enterprise which consists of a new EMR Help encryption module built out of the box for new customers. Existing customers can use their existing encryption or leverage the new encryption module. The new encryption module is named sn\_ind\_rmt\_help.emr\_data and works on the same OOTB columns as encryption contexts used to for EMR Help.
        -   PHI data protection has been enhanced to only clear the following question answer table fields:
            -   EMR Session Information
            -   Protected Health Information
-   **Version 2.0.0 - February 2024**

    New: Added minor enhancements to true up to the Washington DC release.

-   **Version 1.4.0 - August 2023**

    New: Add minor changes to true up to the Vancouver release.

-   **Version 1.3.0 - May 2023**

    Minor fixes.

-   **Version 1.2.0 - February 2023**

    Fixed: Role modifications for updated PII data security

-   **Version 1.1.3 - March 202**
    -   Fixed:
        -   Formatting issues when spaces were included in a comment within an API response
        -   Performance issue
-   **Version 1.1.1 - June 2021**

    Fixed: The sn\_ind\_rmt\_help.requester role no longer contains the sn\_incident\_read and sn\_incident\_write roles


