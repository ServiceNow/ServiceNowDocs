---
title: PSDS Investigative Case Management release notes
description: Version history for the ServiceNow PSDS Investigative Case Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-public-sector-psds-investigative-case-mgmt.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Public Sector Industry version history release notes, ServiceNow Store version history release notes]
---

# PSDS Investigative Case Management release notes

Version history for the ServiceNow® PSDS Investigative Case Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 2.8.0 - September 2026**

    New Feature: Investigators can see the Link Analysis - Node Map for each entity in the Link Analysis Tab

-   **Version 2.5.0 - August 2026**
    -   New:
        -   Investigators can manage tasks and escalate field work directly within case records. A dedicated area to view all investigative tasks is now available on investigative case records. Investigators can initiate new tasks and escalate any task to a formal work order using a new "Create Work Order" action, without leaving the case workspace. Work orders are automatically linked to their originating tasks.
        -   Investigative tasks are accessible from the contextual side panel. Investigators can view and manage investigative tasks directly from the case's contextual side panel, including quick-reference summaries and task creation, reducing context-switching.
        -   Index entities now support immutable versioning and case-scoped snapshots. Every create, update, delete, or merge action on Index entities generates a new version. When entities are linked to cases, the system records a snapshot of the entity at the moment of association, preserving historical accuracy and auditability across multi-case investigations.
        -   Investigators can view entity version history and linkage context. Entity records display all versions, version numbers, and field changes in the activity stream. Cases show which entity version was linked and highlight changes since linkage. Investigators are notified if concurrent edits occur and can see the impact of entity changes across cases.
        -   Updated modals and info messages in entity case link record pages. Entity case link pages now display updated modals and info messages consistent with entity cards, including multi-case impact alerts for relationship records.
    -   Changed: All customer-facing "Now Assist" references have been rebranded to "ServiceNow Otto". UI text, labels, help content, and localization files now use the new branding as directed. Assertions and translations have been updated accordingly.
-   **Version 2.0.0 - July 2026**

    This epic introduces two configurable system properties, x\_snc\_icm.case\_write\_access and x\_snc\_icm.case\_read\_access, enabling agencies to extend write access and restrict read access to cases based on Assigned Office, Assignment Group, or both. This allows automatic case access alignment with organizational units without manual Teams tab management, preserving existing access pathways and role-based permissions. The system enforces validation ensuring read access always encompasses write access, preventing invalid configurations. The outcome provides flexible, secure case visibility and editability at implementation, supporting efficient collaboration and tighter data control while maintaining global visibility of linked entities.

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

**Parent Topic:**[ServiceNow Store - Public Sector Industry version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-public-sector-highlight.md)

