---
title: Account Lifecycle Events release notes
description: Version history for Account Lifecycle Events application the on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-account-lifecycle-events.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Account Lifecycle Events release notes

Version history for Account Lifecycle Events application the on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.2.2 - June 2026 \(Zurich\)**
    -   This release delivers a unified Touchpoint data model, AI Web Agent enablement for customer experimentation, accessibility upgrades, and a set of productivity enhancements that help Customer Success Managers work faster and more proactively.
        -   General CSM improvements — Auto-initiation of Success Initiatives, outcome templates enriched with metric data, AI-driven search, internal-only touchpoints, and play sequencing.
        -   Unified Touchpoint data model — Touchpoint tables migrated to the new CRM Touchpoint for a unified, scalable, CRM-aligned data architecture.
        -   AI Web Agents enabled for customer experimentation — Customers can now experiment with prompt-driven and show-me-once agent models on their own CSM workflows.
        -   Accessibility — WCAG 2.2 AA + 400% zoom/reflow support — CSM now meets the accessibility bar for this release.
-   **Version 6.2.0 - April 2026 \(Zurich\)**

    For this release, we are not shipping any new functionalities.

-   **Version 5.9.1 - March 2026 \(Yokohama\)**
    -   We are releasing the following features in this release:
        -   Success Initiatives Automation &amp; CSM Workflow Enhancements
        -   Native Meetings Management
        -   Touchpoint \| M2M Association Framework &amp; Source Linking Enablement
        -   Enhanced Success Outcome Templates with Metric Integration – Pre-configured metrics auto-populate on outcome creation
        -   AI-Powered Search – Contextual keyword search across 13 CSM tables via right sidebar
        -   Internal Touchpoint Management – Restrict touchpoints to internal users only
        -   Success Report Navigation Enhancement – Moved to top-level menu for faster access
        -   Approval Workflow for Success Objective Template – Supports approval requests, state updates, and cancellations
-   **Version 5.6.6 - December 2025 \(Yokohama\)**
    -   The following is the list of features that we are shipping in the December Z Release:
        -   Moving the Health metric from PA to DCE
        -   Risk timeline visualisation
            -   Addition of a new M2M table -&gt; Risk Impacted records
            -   Extending support of Risk signal and issues, touchpoints to the Onboarding case
        -   Taking up the data workflow fabric in DCE
        -   Security Directives
            -   Granular Admin Roles Enablement – Reducing Risk by Decomposing the "admin" Role
            -   Enforcing Dot walk Cross-Scope Access Checks on Restricted Tables – Australia Release
            -   Remediate Read-Only Fields per Australia Security Directive
-   **Version 4.1.9 - June 2025**
    1.  Account Onboarding Access IssueUsers with the roles sn\_acct\_lc.customer\_success\_agent or sn\_acct\_lc.agent can now access Account Onboarding cases. This was previously restricted due to role-based access issues.
    2.  Success Landing Page - Health Score
        1.  The health score on the Overall Engagement Health Card is no longer truncated.
        2.  The filter "current user is part of squad" now supports the AND operation properly when used in the card's record list.
    3.  PA Scorecard API - Indicator Breakdown LimitThe PA Scorecard API now returns more than 10 indicator breakdown elements. Previously, it was limited to only 10.
    4.  Success Objectives - Product Model FieldThe Product Model field is now available on Success Objectives. Users can select a product from the product list as expected.
-   **Version 4.0.8 - June 2025 \(Washington DC, Xanadu\)**
    1.  Account Onboarding Access IssueUsers with the roles sn\_acct\_lc.customer\_success\_agent or sn\_acct\_lc.agent can now access Account Onboarding cases. This was previously restricted due to role-based access issues.
    2.  Success Landing Page - Health Score - The health score on the Overall Engagement Health Card is no longer truncated. The filter "current user is part of squad" now supports the AND operation properly when used in the card's record list.
    3.  PA Scorecard API - Indicator Breakdown LimitThe PA Scorecard API now returns more than 10 indicator breakdown elements. Previously, it was limited to only 10.
    4.  Success Objectives - Product Model FieldThe Product Model field is now available on Success Objectives. Users can select a product from the product list as expected.
-   **Version 4.1.6 - May 2025 \(Yokohama\)**
    -   Fixes:
        -   Squad members are not able to see active engagements
        -   My active engagements 6 week health score provides no alt text
        -   Engagement - Spacing and font inconsistencies among tabs
        -   Highlighted color for engagement health in Record page is wrong
        -   \[Perf\] ALE Performance: Touchpoint Planner: Slow Data Broker in 2 requests increasing the overall page load time.
        -   Closed or canceled risks incorrectly do not considered as "addressed"
        -   Touch point record UI/UX feedbacks
        -   Engagement - Renewal and expansion UI Feedback
        -   \[Enhancement\] Risk details card must show category and engagement risk definition on Risk record page Create success play button overlaps on Refresh Health Button in Engagement record page after increasing the text spacing
-   **Version 4.0.6 - May 2025 \(Washington, Xanadu\)**
    -   Fixes:
        -   Squad members are not able to see active engagements
        -   My active engagements 6 week health score provides no alt text
        -   Engagement - Spacing and font inconsistencies among tabs
        -   Highlighted color for engagement health in Record page is wrong
        -   \[Perf\] ALE Performance: Touchpoint Planner: Slow Data Broker in 2 requests increasing the overall page load time.
        -   Closed or canceled risks incorrectly do not considered as "addressed"
        -   Touch point record UI/UX feedbacks
        -   Engagement - Renewal and expansion UI Feedback
        -   \[Enhancement\] Risk details card must show category and engagement risk definition on Risk record page
        -   Create success play button overlaps on Refresh Health Button in Engagement record page after increasing the text spacing
-   **Version 4.1.0 - February 2025**
    -   Data Model
    -   Context Map Engine Health and Risk Definitions Success Objective and Outcome Blueprints
    -   AI Uses Cases
    -   Summarization skills for Onboarding, Engagements, and overall Touchpoint record, requires the Now Assist for TMT plugin to be installed.
    -   User Experience
    -   -   L1 Touchpoint/Meeting Calendar
-   L1 Risk Signals and Issues Dashboard
-   Updated Success Portfolio and Engagement Pages with Health and Renewals
-   Updated Data Import Task pages
-   Success Blueprint UX and Planner Touchpoint UX
-   Risk Signal and Issues UX
    -   General Improvements\*\*
    -   Reference Architecture for Zoom/Teams Integration and CRM
-   **Version 2.8.5 - November 2024**
    -   Fixes:
        -   Security Bug Table ACL Bypass via GlideAggregate/GlideRecord Encoded Query - DIRS0000179
        -   State field is not editable on Success Objective form
        -   Success Agent cannot able to view open the Engagement record
-   **Version 2.4.0 - August 2024**
    -   New Features:
        -   Data Validation Builder and Validation Assist tables and supporting logic
            -   NOTE: For the Data Validation Builder the System Admin must be application scope of the target table is present. For example, if importing to Contacts table, when using the builder the System Admin should be in the same application scope of the Contacts table \(like Global\)
        -   First version of the Customer Success Management data model and user experience
        -   -   Process Based Layout Success Initiatives
        -   Homepages for both Onboarding and Customer Success Management personas
        -   Pre-built Recommended Actions for specific onboarding case tasks, such as Data Capture or Service Bridge setup and Registration
        -   Service Portal lists and ticket-form widget for Onboarding Cases and Case Tasks
        -   Success Play Capability
        -   ALE Choice and Definition tables
        -   Customer Success Manager fulfiller role, application viewer role, and granular read/write roles.
    -   Changed:
        -   Change from the Standard Record Page to the Process Based Layout page for the Onboarding Case Type
        -   Incorporation of the Data Validation Assist feature in client scripts and supporting logic
    -   Fixed: Several minor code fixes to time calculations
    -   Removed: Unused data capture task fields
-   **Version 1.0.6 - March 2024**

    Fixed: Remove dependency of plugin com.snc.uib.sn\_dyn\_rel\_rec from ALE app.

-   **Version 1.0.4 - August 2023**

    TheServiceNow Account Lifecycle Events applications enables Telecommunications, Media, and Technology service providers to structure, measure, and collaborate on key activities related to their enterprise customers account journey.


