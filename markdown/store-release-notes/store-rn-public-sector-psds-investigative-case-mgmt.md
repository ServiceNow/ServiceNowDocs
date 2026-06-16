---
title: PSDS Investigative Case Management release notes
description: Version history for the ServiceNow PSDS Investigative Case Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-public-sector-psds-investigative-case-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Public Sector Industry release notes, ServiceNow Store release notes]
---

# PSDS Investigative Case Management release notes

Version history for the ServiceNow® PSDS Investigative Case Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 1.2.1 - June 2026**

    Enhancements &amp; foundational updates for AI Native development and upcoming features.

-   **Version 1.1.0 - May 2026**
    -   What's New:
        -   Primary Supervisory Agent Assignment
            -   Cases now support a dedicated Primary Supervisory Agent role, distinct from the existing Supervisory Agent role. This enables agencies to clearly identify the single person responsible for case-level oversight, approvals, and review.
            -   Key behaviors:
                -   A new "Primary Supervisory Agent" role is available on the case Teams tab.
                -   Assigning a user in the Supervisory Agent field on the case automatically adds them to the Teams tab with the Primary Supervisory Agent role — and vice versa.
                -   The system enforces a single Primary Supervisory Agent per case.
                -   This foundation supports upcoming Now Assist AI-driven case creation workflows.
        -   Java Runtime Upgrade: The underlying Java runtime has been upgraded from 17.0 to 21.0, bringing improved performance, security patches, and long-term support alignment.
        -   Security: Case record access control hardened — Resolved an issue where users without any ICM role could read investigative case records through an inherited platform ACL. A dedicated access control rule now ensures that only users with appropriate ICM roles can view case data.\(Moderate\)
        -   Usability:
            -   "Add Case" button on entity records restored — The "Add Case" action on entity record pages \(Person, Location, Vehicle, etc.\) was not opening the case-linking modal. This has been corrected and the button functions as expected.\(Low\)
            -   Evidence list empty state added — The Evidence list on case records and the main Evidence list view now display a proper empty-state message when no evidence items exist, instead of showing a blank area.\(Low\)
        -   Data Integrity
            -   Location-to-case linking errors resolved — A business rule that runs when linking a location to a case contained incorrect field references, causing script errors and preventing the intended cache-clearing side effect. Field references have been corrected and the rule now executes cleanly.\(Low\)
-   **Version 1.0.2 - April 2026**

    Enhancements and fixes only. No new features added.

-   **Version 1.0.1 - March 2026**
    -   Investigative Case Management \(ICM\) is the AI-first platform for government fraud, waste, and abuse investigations, designed to modernize investigative operations, accelerate case resolution, and ensure regulatory compliance.
    -   Purpose-built foundation of data models, workflows, and AI agents transforms paper-based and spreadsheet-driven processes into unified digital operations. ICM provides a standard architecture for managing complex investigations with a government-optimized data model supporting diverse investigation types and comprehensive evidence management.
    -   With ICM, investigative agencies can:
        -   Accelerate case intake and reduce administrative burden
        -   Improve investigative quality through comprehensive evidence management
        -   Ensure compliance with regulatory requirements and audit standards
        -   Scale investigative capacity without proportional headcount increases

**Parent Topic:**[ServiceNow Store - Public Sector Industry release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-public-sector-highlight.md)

