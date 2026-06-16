---
title: GRC: Audit Management Workspace release notes
description: Version history for the GRC: Audit Management Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-audit-mgmt-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Audit Management Workspace release notes

Version history for the GRC: Audit Management Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New: Third-line users can now create audit entries in the audit universe for independent testing across the following objects:
        -   Risk statements
        -   Risks
        -   Controls
        -   Control Objectives
        -   Entities
        -   Engagements
-   **Version 22.0.1 - March 2026**
    -   Fixed issues:
        -   Audit word reports can now be generated even when an engagement is marked as confidential.
        -   Resolved security-related defects.
-   **Version 21.1.2 - December 2025 \(Zurich\)**
    -   New: Added Audit Period Start and Audit Period End fields to Engagement records to enable auditing of past or future periods within an ongoing engagement. Authority document, citation and control objective lists visible for feature roles.
    -   Changes: Engagement planned start dates and end dates behaviour has been changed to remove rollups on the basis of Audit tasks.
    -   Fixed:
        -   Fixed CORAL theme issues on engagement overview page.
        -   Fixed Polaris dark theme issues.
        -   Fixed security defects.
-   **Version 21.0.1 - August 2025**
    -   New:
        -   Light weight audit management has been introduced to offer core capabilities of Engagement, Entity Scoping, Activities, and Evidence \(when Advanced Core is installed\) and a lighter version of the home page.
        -   Granular feature roles introduced to leverage light weight audit capabilities.
        -   Test steps are introduced to perform Control testing at a more structured and granular level.
    -   Changed: Added data visualizations to show engagements and plans by state on the Audit manager home page and realigned the engagements and plans list alongside the new visualizations.
    -   Fixed:
        -   Drill down issues from Audit home page are now fixed.
        -   Implemented security fixes.
        -   Fixed CORAL theme and accessibility issues in home page.
        -   Performance issue fixes to improve the load time of home page.
    -   Removed: Tasks section from the Audit manager and Audit user home pages.
-   **Version 20.1.0 - May 2025**
    -   Changed:
        -   Control test issues will be shown on the homepage when you select a filter. This will help the page load faster when you first load it.
        -   Timeline widget on the homepage will be displayed on click of the "chevron" icon, to improve performance timings on initial load of the page.
    -   Fixed:
        -   Fixed typography issues for CORAL theme across Audit workspace.
        -   Fixed accessibility issues related to label drop-down and zoom issues on audit manage homepage , audit user homepage, engagement overview page.
        -   Fixed email not getting generated on failure of Audit word template report generation.
-   **Version 20.0.1 - February 2025**
    -   Changed: Issues widget on Audit manager homepage split to show Engagement issues and Control test issues separately
    -   Fixed:
        -   Test Plan related list from Control record doesn't show pop-up on click of add button
        -   Add Action Assignment button broken on Entities related list for engagement
-   **Version 19.1.1 - November 2024**

    Changed: Improved workspace experience for users with low vision or those who rely on assistive technology, such as screen readers. This includes optimising zoom capabilities.

-   **Version 18.1.0 - June 2024**

    Fixed: The URL locates the correct resource on clicking the List module items of the Audit Workspace.

-   **Version 18.0.1 - February 2024**
    -   New: Ability to manage engagement and audit task-related documents on Microsoft OneDrive.
    -   Fixed: Audit users are not able to create observations from the issue landing page in the Audit Workspace.
-   **Version 17.0.0 - August 2023**
    -   Changed: Workspace record pages are migrated to risk record page template which extends standard record page template.
    -   Fixed:
        -   Engagement field work percent complete field not updating correctly.
        -   Engagement actual start and end date validations.
-   **Version 16.0.3 - July 2023**

    Fixed: Addressed an issue where the Runtime access tracking field's value was inadvertently changing from "None" to "Enforcing" during the Utah upgrade.

-   **Version 16.0.2 - February 2023**
    -   Changed:
        -   Ability to scope common controls into Engagements
        -   Ability to associate multiple Engagements to the same issue and vice-versa
        -   Support for Accessibility standards
        -   Support for Localization
    -   Fixed: Engagement parent field is not getting populated when an issue is created from Audit workspace
-   **Version 15.0.1 - August 2022**
    -   Fixed:
        -   Search in Audit Workspace is not working.
        -   Addressed Localization issues.
-   **Version 14.1.0 - March 2022**
    -   Changed:
        -   Task page changes.
        -   Security changes
    -   Fixed: Configure Workspace is taking users to Agent Workspace instead of Audit Workspace Configuration.
-   **Version 14.0.0 - February 2022**

    Changed: Updated for San Diego platform compatibility

-   **Version 13.0.2 - September 2021**

    Audit Workspace is a single-pane view for an audit supervisor and auditor to view the overall audit timeline and status, track budget and resources for engagements, track high priority observations and issues, and monitor ongoing control testing and audit task progress. The workspace allows the audit supervisors to define audit plans and engagements, assign budget and resource to engagements, and track the progress of engagements. Auditors are able to test effectiveness of controls, request evidence, create observations and complete other audit activities. Using the central issue management capability they can also define the remediation plan of action and follow up on issues to ensure the gaps are fixed at the earliest.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

