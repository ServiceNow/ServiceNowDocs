---
title: GRC: Advanced Core release notes
description: Version history for the GRC: Advanced Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-advanced-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Advanced Core release notes

Version history for the GRC: Advanced Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Query range ACL's
            -   Consistent access control: All tables include standardized query range security ACLs, ensuring that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience: New query ACL rules are installed automatically during upgrade with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
            -   Post-upgrade review for customized ACLs: If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
-   **Version 22.0.1 - March 2026**
    -   Fixed:
        -   Fixed automatic table name change on Business App Request table.
        -   Fixed security issues.
-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   New: Added a new field in the Evidence Response table to store a reference to the Evidence Collection Details from which the response was generated. Created a new user role called All Evidence Reader for reading all the evidence responses.
    -   Fixed: Copy attachments from both Evidence Request and Evidence Collection Detail to Evidence Response when it is created. Added loader for Create evidence request pop-up. Remove the Evidence Response when the associated collection details are deleted. Fixed security issues.
-   **Version 21.0.1 - August 2025**

    -   New:
        -   Evidence response now can be created in one step using Create new evidence task option.
        -   Evidence response is improved with additional data of source and context.
        -   Evidence requests related list enabled in engagements.
        -   Granular feature roles introduced to leverage evidence capabilities.
        -   Enhanced security on Evidence request, Evidence response and Evidence collection details tables by introducing range queries.
    Fixed: Fixed Security issues.

-   **Version 20.2.0 - June 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.1.0 - May 2025**

    Fixed: Enabled translations on Result field of Issue Triage table.

-   **Version 20.0.0 - February 2025**

    Fixed: Field level duplicate messages on issue triage form.

-   **Version 19.1.1 - November 2024**

    Changed: Security fixes.

-   **Version 19.0.1 - August 2024**
    -   New:
        -   Audit reader role for all read operations.
        -   Audit approver role for approval of Engagements and Audit plans.
-   **Version 18.0.1 - February 2024**
    -   Fixed:
        -   Localisation issues
        -   Updated access controls on evidence-related tables
-   **Version 17.0.0 - August 2023**

    Fixed: Access control issues when plugin is installed without audit application.

-   **Version 16.0.2 - July 2023**

    Fixed: Addressed an issue where the Runtime access tracking field's value was inadvertently changing from "None" to "Enforcing" during the Utah upgrade.

-   **Version 16.0.1 - February 2023**
    -   Changed: Support for Localization
    -   Fixed: Access controls for viewing reports
-   **Version 15.0.2 - December 2022**

    Fixed: Reduction in installation size of the application.

-   **Version 15.0.1 - February 2022**
    -   New:
        -   Ability to request Evidence for other GRC Objects like Policy, Regulation, Citation, etc. from an Evidence Request of type Audit
        -   When creating Evidence Requests, Requester should be able to view and associate existing Evidences
    -   Changed:
        -   When creating Evidence Requests from other GRC Objects, Requester should be able to select the Type of Evidence
        -   Requester should be able to update Name, Description, Instructions, Watch List on Evidence Request and Evidence Tasks when Evidence Request is in New, Work in Progress states
        -   On Evidence Tasks: Name, Desccription, Instructions should be copied from Evidence Collection detail
    -   Fixed:
        -   Unable to assign Evidence Tasks to users with Business User Lite role in Workspace
        -   Security Issues on Evidence Request UI Actions
        -   Issue Triage Owner should not be allowed to Request Information when Issue Triage is in Review state
-   **Version 14.1.1 - March 2022**
    -   New:
        -   Security changes
        -   Issue Triages on Employee Service Portal
    -   Changed: Security updates
-   **Version 13.0.1 - September 2021**
    -   New: Added support for Compliance Workspace
    -   Fixed:
        -   Unable to close Issue Triage record when substate is Information requested
        -   On Evident tasks, attachments are not displayed for members of assignment group
        -   Security issues

**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

