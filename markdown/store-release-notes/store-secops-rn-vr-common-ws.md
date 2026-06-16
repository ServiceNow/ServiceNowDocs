---
title: Vulnerability Response Common Workspace release notes
description: Version history for the Vulnerability Response Common Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-common-ws.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Common Workspace release notes

Version history for the Vulnerability Response Common Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.5.2 - June 2026 \(USEM\)**
    -   New:
        -   Bulk edit now supports updating Risk Reduction and Compensating Controls fields directly from the workspace.
        -   Added out-of-the-box query range Access Control Lists \(ACLs\) for workspace saved filters to harden security against unauthorized data exposure \(CVE-2025-3648\).
    -   Changed: Accessibility improvements across the workspace home page and the Approval Recommendation experience, including WCAG 2.2 AA compliance and proper layout/reflow at 400% browser zoom.
    -   Fixed:
        -   Fixed the Create Remediation Task popup so the action now opens and completes correctly in the workspace.
        -   Fixed the Save/Update button on the Remediation Task Rule form, which was non-functional and showed an internal placeholder text in its tooltip.
        -   Fixed the Assignment Rule form so the Update button works correctly.
        -   The "Applies To" column on the Approval Rules form view now shows the saved value instead of appearing blank.
        -   Multi-level dot walking now works correctly in the Approval Level configuration.
        -   Users with only the Remediation Owner role no longer see the "New" button to create Approval Rules unless they have the proper management permission.
        -   Delegated approvers can now view the vulnerable items mapped to their approval responsibilities.
        -   The Approve/Reject confirmation popup is now translated into the user's session language \(previously appeared in English regardless of locale\).
        -   Bulk edit no longer reports a misleading "Number of VIs that satisfy filter is 0" error when closing already-resolved records.
-   **Version 1.10.0 - June 2026**
    -   New: Added Access Control List \(ACL\) support for query ranges on workspace-saved filters to comply with internal security requirements.
    -   Fixed: Resolved ambiguous translations for the "View by" label in the Vulnerability Manager workspace, which appeared in multiple contexts without sufficient differentiation.
-   **Version 30.4.4 - April 2026 \(USEM\)**
    -   New:
        -   Users and Groups management is now available in the Security Exposure Management \(SEM\) workspace Administration console for centralized role assignment.
        -   System properties can now be viewed and managed directly within the USEM workspace Administration console.
        -   Remediation task rules now support one-to-one finding-to-remediation task mapping for more granular tracking and resolution.
        -   Bulk deferral now validates that selected vulnerability items are not already deferred, preventing duplicate deferrals and accidental field overwrites.
        -   AI-powered approver recommendations are now delivered through a native AI platform plugin with tier-appropriate availability controls.
    -   Changed:
        -   Update set capture is now supported for a broader set of Unified Security Exposure Management \(USEM\) configuration types, including Exception Management configurations, Exception rules, Exclusion rules, Remediation Task rules, Rollup calculators, and Approval rules.
        -   Integration drill-down navigation now works consistently for integrations built on the new integration framework.
        -   The integrations page now displays a clear message when a connected integration is not supported by Vulnerability Response.
        -   Approval workflow UI has been refreshed for a more consistent and polished reviewer experience.
        -   Exception Management workspace received layout and interaction refinements based on design feedback.
        -   Error notifications from backend processes are now surfaced directly on the Advanced Settings page.GlideRecord queries now support addUserEncodedQuery for improved adherence to platform security standards.
    -   Fixed:
        -   Multiple layout and usability issues across USEM Administration pages including Assignment, Classification, Remediation Target, Rollup Calculator, Risk Rule, and Remediation Task Rule forms have been resolved.
        -   The "Approve/ Reject" button no longer remains incorrectly disabled when opening an approval record.
        -   Delegated approvers can now correctly view vulnerability records shared with them.
        -   The "Applies to" column in the USEM Administration page now correctly filters tag-type fields.
        -   Drag-and-drop reordering in the USEM workspace now functions correctly.
        -   The Condition Builder in Remediation Task rules no longer refreshes on every field change.
        -   Custom columns can once again be added to the Grouping Criteria of Remediation Task rules after upgrading.
        -   The Approval Level configuration now correctly displays all available parent table fields when selecting the approver table field.
        -   The AI approval recommendation panel now renders correctly in dark mode.
-   **Version 30.3.0 - March 2026 \(USEM\)**

    New: Support for adding custom columns to remediation task rule grouping criteria.

-   **Version 1.9.0 - January 2026**

    Minor fixes for this release.

-   **Version 30.2.7 - January 2026 \(USEM\)**

    Changed: Security Fixes.

-   **Version 1.8.1 - December 2025**

    Minor fixes for this release.

-   **Version 1.7.1 - September 2025**

    Minor fixes for the release.

-   **Version 1.7.0 - August 2025**

    Fixed: Resolved Accessibility issues for Vulnerability Manager workspace.

-   **Version 1.5.8 - June 2025**

    Fixed: Removed the unexpected white line on the banner on the Vulnerability Manager Workspace home page when in dark mode.

-   **Version 1.5.5 - May 2025**
    -   Changed:
        -   Added Framework to support reapply CI lookup rules from DI List view.
        -   Removed the Row count for the all the list/related list views in Workspace experience.
-   **Version 1.4.1 - February 2025**

    New: Added capabilities in the common framework to support the ability to manually create Remediation Tasks \(RTs\) in the Vulnerability Manager and IT Remediation workspaces.

-   **Version 1.3.3 - November 2024**

    New: New components have been added to support improvements on the Home page and Re-evaluate UI action in the Vulnerability Manager Workspace.

-   **Version 1.2.2 - August 2024**

    New: Added capabilities in the common framework to support the evaluation of the risk scores, assignments, remediation target date, and remediation tasks for a set of selected vulnerable items, application vulnerable items, container vulnerable items or test results.

-   **Version 1.1.10 - June 2024**

    Fixed: Minor fixes for this release.

-   **Version 1.1.7 - May 2024**

    New: Added new components to support the Bulk Edit feature in the Vulnerability Manager Workspace to update state, assignment group, and request exceptions for multiple records \(application vulnerable items or container vulnerable items\).

-   **Version 1.0.2 - February 2024**

    Vulnerability Response Common Workspace is a framework that supports and provides common resources for Vulnerability Response Workspaces.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

