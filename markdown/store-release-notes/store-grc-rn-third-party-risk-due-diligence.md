---
title: GRC: Third-party Risk Due Diligence release notes
description: Version history for the GRC Third-party Risk Due Diligence application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-third-party-risk-due-diligence.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Third-party Risk Due Diligence release notes

Version history for the GRC Third-party Risk Due Diligence application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New:
        -   Added SBOM questionnaire auto-assignment on engagement creation.
        -   Added SAE template versioning capability support.
    -   Changed:
        -   Replaced GlideRecord with GlideRecordSecure in TPRMDueDiligenceAjax for security compliance.
        -   Updated ACL query rules based on 2025 May MSI \(CVE-2025-3648\).
        -   Replaced vendor reviewer role with GRC reader on report view ACLs.
        -   Added retired=false filter to SAE template reference qualifiers.
        -   Removed orphan ACLs from dd\_element table.
    -   Fixed:
        -   Corrected domain separation issues on issues and event-driven rules \(PRB2020926\).
        -   Fixed duplicate audit creation on current.update\(\) \(PRB1992222\).
        -   Resolved engagement primary contact creation issue when toggling "Same as third-party contact" option \(PRB1988772\).
-   **Version 22.0.1 - March 2026**
    -   New: Support for assessments on elements has been added.
    -   Changed: Event driven rule configured with "Use the last IRQ assessor" has been updated to select the most recent assessor from the same third-party.
    -   Fixed: Event driven rules not working as expected when SAE turned on has been addressed.
    -   Removed: Assessments using entities is no longer supported.
-   **Version 21.1.3 - December 2025**
    -   Fixed:
        -   Incorrect population of closed and duration\_days was appearing on Due Diligence records.
        -   Info message has been added/updated to indicate next steps during the various stages of the Due Diligence process.
-   **Version 21.0.1 - August 2025**
    -   New: The Due diligence workflow has been improved to work with Smart Assessment Engine.
    -   Fixed: The engagement name auto-populating with an appended timestamp has been addressed.
-   **Version 20.1.1 - May 2025**
    -   Fixed:
        -   'Third party is not listed' checkbox is not getting checked after switching request type.
        -   i18N translation issues have been addressed.
-   **Version 20.0.0 - February 2025**
    -   Fixed:
        -   The issue of saving a third-party risk due diligence request as a draft not working from Employee service center has been addressed.
        -   The issue of the percentage bar not updating for a Vendor risk assessment questionnaire even when it has been completed by third party has been addressed.
-   **Version 19.1.4 - November 2024**
    -   Changed:
        -   Updated default sandbox access for client callable scripts.
        -   Improved third-party elements due diligence workflow for engagements.
    -   Fixed:
        -   Filter was missing on the expiring risk assessments widget on risk activity WS page.
        -   Due diligence request risk intelligence scores were not being assigned as expected when the 'active' field for the due diligence request was toggled.
        -   Fixed table ACL for Third-party risk due diligence.
-   **Version 19.0.3 - August 2024**
    -   Fixed:
        -   Event-driven rule was not referencing the user date or time when setting up a schedule for that rule.
        -   Due diligence request fields for the third-party and engagement basic information sections were not read-only after the IRQ in progress state.
    -   New:
        -   Risk Intelligence Screening Report requests
        -   Third-party elements for Engagements
-   **Version 18.1.1 - July 2024**

    Fixed: Fixed app compatibility for the glide family releases.

-   **Version 18.1.0 - May 2024**
    -   New:
        -   Ability to automatically attach external questionnaires to Third-party Risk Assessments based on 'Internal Risk Questionnaire rating'.
            -   Ability to set this up in the Classic UI.
-   **Version 18.0.1 - February 2024**
    -   New:
        -   Event-driven Management Rules.
        -   Licensing tracking table added to see your licensable activity.
    -   Changed:
        -   Renamed Internal Scores to Inherent Risk Score in Due Diligence workflows.
        -   Removed the ability to open Third-party Risk Assessments when the associated Due Diligence request is in Contract terminated, Contract not terminated, Contract not renewed, or Cancelled states.
        -   When reopening a Third-party Risk Assessment associated with a Due Diligence request, the approvals will be cancelled until they are resubmitted.
    -   Fixed: Due diligence request workflow was updated to accommodate multiple IRQs that can generate external questionnaires based on the IRQ answers.
-   **Version 17.0.7 - November 2023**
    -   New: Auto-populate third-party questionnaires with answers from previous questionnaires
    -   Fixed:
        -   On the main Due Diligence flow, updated 'run as user' to not be System
        -   Issue where engagements were not terminating if the start date is in the future
        -   Duplicate "New" buttons on the questionnaire templates list
        -   Incorrect filters on the Due Diligence Management workspace dashboard
        -   "Request for Approval" UI action was incorrectly showing for TPR Reviewers
-   **Version 17.0.7 - November 2023**

    The ServiceNow Third-party Risk Management application offers preconfigured workflows for seamless onboarding, reassessments, renewals, and offboarding to manage the full due diligence lifecycle. It also includes a Risk Concentration Map and an intuitive Due Diligence Management page for efficient workflow oversight.


