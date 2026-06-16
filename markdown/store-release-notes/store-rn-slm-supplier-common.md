---
title: Supplier Common Architecture release notes
description: Version history for the Supplier Common Architecture on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-slm-supplier-common.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Supplier Lifecycle Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Supplier Common Architecture release notes

Version history for the Supplier Common Architecture on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.0 - June 2026 \(Australia\)**
    -   Fixed:
        -   Improved access controls for better security.
        -   Fixed translation of user interface text to ensure accurate display of product capabilities across multiple languages, resolving issues reported.
-   **Version 8.0.0 - June 2026 \(Zurich\)**
    -   Fixed:
        -   Improved access controls for better security.
        -   Fixed translation of user interface text to ensure accurate display of product capabilities across multiple languages, resolving issues reported.
-   **Version 5.9.3 - June 2026**
    -   Fixed:
        -   Improved access controls for better security.
        -   Fixed translation of user interface text to ensure accurate display of product capabilities across multiple languages, resolving issues reported.
-   **Version 7.0.0 - March 2026**
    -   New:
        -   Monitor and enforce time-bound documents from suppliers.
            -   Provides escalation pathways if document upload tasks are not completed.
            -   Enables admins to configure document lead time, grace period, and reminder frequency.
            -   Supplier managers or contacts can fill the expiry date while uploading documents. Based on this, automated upload document tasks are created \(Supported only in the Australia release\).
            -   Ensures seamless management of documents with expiration dates and reduces manual oversight on renewals.
        -   Assess supplier performance at scale powered by the Smart Assessment Engine application.
            -   Bulk distribution via segmentation rules: Associate assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one-off outreach.
            -   Internal stakeholder completion: Sourcing and procurement teams complete assessments in the Source-to-Pay Workspace, keeping evaluations centralized and auditable.
            -   Supplier self-service completion: Supplier contacts complete their assessments through the Supplier Collaboration Portal.
        -   Email-driven capabilities to simplify supplier interactions and centralize communication.
            -   Email-based task completion: Suppliers can directly complete tasks via email, such as marking tasks complete, playing videos, and accessing shared links.
            -   Centralized email tab: Email tab at supplier, case, and task levels to view all communications in one place.
            -   Email summarization: Summarization within emails provides quick and clear context for users \(for tasks and cases\).
-   **Version 5.6.0 - March 2026 \(Yokohama\)**
    -   New:
        -   Monitor and enforce time-bound documents from suppliers by:
            -   Providing escalation pathways if document upload tasks are not completed.
            -   Enabling admins to configure document lead time, grace period, and reminder frequency.
            -   Ensures seamless management of documents with expiration dates and reduces manual oversight on renewals.
        -   Assess supplier performance at scale powered by the Smart Assessment Engine application.
            -   Bulk distribution via segmentation rules: Associate assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one-off outreach.
            -   Internal stakeholder completion: Sourcing and procurement teams complete assessments in the Source-to-Pay Workspace, keeping evaluations centralized and auditable.
            -   Supplier self-service completion: Supplier contacts complete their assessments through the Supplier Collaboration Portal.
        -   Email-driven capabilities to simplify supplier interactions and centralize communication.
            -   Email-based task completion: Suppliers can directly complete tasks via email, such as marking tasks complete, playing videos, and accessing shared links.
            -   Centralized email tab: Email tab at supplier, case, and task levels to view all communications in one place.
            -   Email summarization: Summarization within emails provides quick and clear context for users \(for tasks and cases\).
-   **Version 5.0.2 - September 2025**
    -   Fixed: Minor fixes
    -   Features:
        -   The Supplier Common Architecture application enables employees to collaborate with suppliers by:
            -   Having a single repository for all supplier-related data.
            -   Simplify and streamline the way employees engage with suppliers to request help in sourcing, procuring goods and services, or assisting suppliers with issues.
            -   Suggest and guide employees to correct suppliers.
-   **Version 4.2.2 - September 2025 \(Yokohama\)**
    -   Fixed: Minor fixes
    -   Features:
        -   The Supplier Common Architecture application enables employees to collaborate with suppliers by:
            -   Having a single repository for all supplier-related data.
            -   Simplify and streamline the way employees engage with suppliers to request help in sourcing, procuring goods and services, or assisting suppliers with issues.
            -   Suggest and guide employees to correct suppliers.
-   **Version 5.0.1 - August 2025**
    -   New: Added Relish validations for existing suppliers, including Address, Banking, and Sanctions checks.
    -   Fixed: Minor fixes
-   **Version 4.2.0 - May 2025**

    Minor fixes.

-   **Version 4.1.0 - March 2025**

    Minor fixes.

-   **Version 3.0.0 - December 2024**
    -   Enables effortless access to supplier contact information across multiple suppliers with a single set of login credentials
    -   Centralises case and task tracking from various suppliers, enhancing efficiency within a single platform
-   **Version 2.9.0 - November 2024**
    -   New:
        -   Implementation of segmentation rule table.
        -   Customisation of segmentation rule actions with custom scripts.
        -   Scheduled jobs which executes segmentation rule based on frequency.
-   **Version 2.8.2 - September 2024 \(Washington DC\)**
    -   Fixed:
        -   The issue where the supplier contact could read the payment information of other suppliers has been fixed.
        -   The activity definition missing error seen in the Supplier onboarding playbook has been resolved.
        -   The issue causing the "Mark complete" button to show in the Review case lane of the Case playbook has been fixed.
-   **Version 2.4.8 - September 2024 \(Vancouver\)**

    Fixed: The issue where the supplier contact could read the payment information of other suppliers has been fixed.

-   **Version 2.8.1 - August 2024**

    Minor fixes.

-   **Version 2.6.9 - July 2024**
    -   Fixed:
        -   The Close notes field and Reject Supplier button are now displayed properly in the Supplier onboarding playbook.
        -   The Close notes field is now rendered properly in the Case playbook for all case types.
        -   Fixed issue related to the Skip button being unresponsive or not visible in playbooks.
-   **Version 2.6.7 - June 2024**
    -   Fixed:
        -   You no longer receive an error when creating a task of action type Survey.
        -   After upgrading to the Washington DC release from prior releases, the Action description field data is now copied to the Description field for supplier tasks.
        -   The Sign document supplier task is now marked as Closed complete in the Source-to-Pay Workspace after you complete the document task in the Supplier Collaboration Portal.
-   **Version 2.6.2 - May 2024**

    Minor fixes.

-   **Version 2.5.0 - February 2024**

    Minor fixes.

-   **Version 2.4.2 - November 2023**

    Minor fixes.

-   **Version 2.3.3 - August 2023**

    Minor fixes.

-   **Version 2.2.1 - May 2023**

    Changed: Renamed this application to Supplier Common Architecture. This application was formerly named Supplier Common.

-   **Version 2.0.1 - February 2023**

    The ServiceNow Supplier Common Architecture application enables employees to engage and collaborate with suppliers anytime, anywhere.


