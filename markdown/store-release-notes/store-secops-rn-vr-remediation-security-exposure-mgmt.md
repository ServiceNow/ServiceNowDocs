---
title: Remediation for Security Exposure Management release notes
description: Version history for the ServiceNow Remediation for Security Exposure Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-remediation-security-exposure-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Remediation for Security Exposure Management release notes

Version history for the ServiceNow® Remediation for Security Exposure Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 31.0.2 - June 2026 \(USEM\)**
    -   Fixed:
        -   Resolved an issue where vulnerable items remained linked to a remediation task after the task's rule conditions no longer matched during a re-evaluate operation.
        -   Improved performance and stability of remediation task lookups by applying a result limit during retrieval queries.
-   **Version 31.0.1 - April 2026**
    -   New:
        -   Remediation tasks in the Security Exposure Management \(SEM\) workspace now map one-to-one with findings for more precise tracking and ownership.
        -   The Admin console now includes a Users and Groups list view for centralized access and role management.
        -   Manual remediation tasks can now be created for remediation orders using "All" selection mode to include all eligible findings at once
        -   AI-powered approver recommendations are now available in the workspace, suggesting approvers based on context \(available to eligible service tiers\).
    -   Changed:
        -   SEM workspace configurations including exception rules, exclusion rules, remediation task rules, rollup calculators, and exception management settings can now be exported to update sets for easier promotion across environments.
        -   System properties in the Security Exposure Management workspace are now modularized for simpler management directly from the Administration console.
        -   The advanced settings page now shows inline success and error notifications when configuration changes are saved or fail.
        -   Approval forms have been updated with cleaner layouts and more consistent field behavior.
        -   Exception management pages have been refreshed with clearer interactions and a more refined visual presentation.
        -   The integrations page now displays an explicit message when an integration is not supported, replacing an ambiguous empty stateIntegration drill-down is now supported in the new integration framework, enabling navigation into integration details from the workspace.
        -   Bulk deferral now validates that selected items are not already deferred before processing, and notifies users when items are excluded.
    -   Fixed:
        -   Delegated approvers can now correctly view vulnerability items assigned to them, resolving a security constraint that previously blocked access.
        -   The New Risk Rule form no longer pre-fills with values from a previously viewed rule.
        -   The "Approve/Reject" button is no longer incorrectly disabled during approval or rejection actions.
        -   Approval level records now display the full set of approver field choices after upgrading to v30.
        -   Now Assist approval recommendations now display correctly in dark mode.
        -   Drag-and-drop interactions now work correctly across all supported workspace views.
        -   Custom columns can once again be added to the grouping criteria of remediation task rules.
        -   The Condition field in remediation task rules no longer refreshes on every keystroke, improving the rule authoring experience.
        -   The "Applies to" column filter in the USEM administration page now correctly filters tag-type fields.
        -   A security vulnerability in query handling has been resolved.
        -   Multiple layout, spacing, and field visibility issues across administration forms have been corrected.
        -   Messaging, button states, and read-only enforcement in administration rule forms now behave consistently regardless of the user's role.
-   **Version 30.2.0 - January 2026**
    -   **Note:** This app version is intended for Unified Security Exposure Management \(USEM\), a significant architectural upgrade to the Vulnerability Response applications. If you are currently using Vulnerability Response and upgrading to USEM for the first time, you must use the Migration assistant for Unified Security Exposure Management to ensure a safe and successful upgrade. If you do not intend to upgrade to USEM, please select a version below 30.x when installing or upgrading.

    -   The Remediation for Security Exposure Management application enables security teams to efficiently group and manage exposure findings across all Unified Security Exposure Management \(USEM\) applications into remediation tasks.
    -   Tasks can be created manually or automatically usingRemediation Task Rules—all defined centrally in theAdmin Console within the Security Exposure Management \(SEM\) Workspace. This ensures consistent remediation workflows across infrastructure, application, container, and configuration compliance exposures.

**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

