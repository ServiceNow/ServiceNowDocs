---
title: Software Asset Workspace release notes
description: Version history for the ServiceNow Software Asset Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itam-software-asset-ws.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - IT Asset Management version history release notes, ServiceNow Store version history release notes]
---

# Software Asset Workspace release notes

Version history for the ServiceNow® Software Asset Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 12.0.4 - September 2026 \(Brazil\)**
    -   New:
        -   Reclamation Summary provides a consolidated view of reclamation opportunities. Software Asset Managers can now access a consolidated Reclamation Summary list in the workspace, grouping opportunities by software and justification with a drill-down into underlying candidate records.
        -   A new Reclamation sub-section is available under License Operations, featuring both the consolidated Reclamation Summary and individual Removal Candidates list views, accessible to all License Operations users.
    -   Changed:
        -   The Reclamation Candidate tab in the workspace is now labeled "Summary" and displays consolidated summary data, replacing individual candidate rows. The tab is also renamed to "Reclamation" for clarity.
        -   The Removal Candidates list has been migrated from the Administration category to the new Reclamation section, making it visible to a broader set of users beyond just administrators.
        -   The Reclamation Summary list now supports filtering and sorting by software model, justification, and integration profile, with improved drill-down navigation.
    -   Fixed: The Key metrics section in the Software Asset Workspace now displays clearer naming and role definitions for numbers, improving user understanding.
    -   Removed: The Removal Candidates list is no longer available under the Administration category; it is now accessible within the Reclamation section under License Operations.
-   **Version 11.0.20 - September 2026 \(Australia\)**
    -   The Resource Value Framework now includes out-of-the-box license metric content with the following enhancements:
        -   Support for configurable metric types via two new tables \(samp\_license\_metric\_config and samp\_default\_consumption\_tier\) and a resource value reconciliation calculator
        -   Backward-compatible dictionary updates to existing fields
        -   Conditional UI rendering that only appears when metric types are configured
        -   No changes to existing data or unconfigured customer environments
-   **Version 11.0.18 - August 2026 \(Australia\)**
    -   The Software Asset Workspace now provides accurate drill-down navigation and consistent localization across dashboards.
        -   Drilling down from license usage into Unlicensed CAL counts now displays records accurately at the publisher and product levels.
        -   List view titles for widget drill-downs on the Lifecycle Management Dashboard and Optimization &amp; Savings Dashboard now display in the correct locale, regardless of user language settings.
    -   Product naming update: Starting with Software Asset Workspace v11.0.18, Now Assist has been renamed to ServiceNow Otto.
-   **Version 10.0.19 - August 2026 \(Zurich\)**
    -   The Software Asset Workspace now provides accurate drill-down navigation and consistent localization across dashboards.
        -   Drilling down from license usage into Unlicensed CAL counts now displays records accurately at the publisher and product levels.
        -   List view titles for widget drill-downs on the Lifecycle Management Dashboard and Optimization &amp; Savings Dashboard now display in the correct locale, regardless of user language settings.
    -   Product naming update: Starting with Software Asset Workspace v10.0.19, Now Assist has been renamed to ServiceNow Otto.
-   **Version 11.0.15 - July 2026 \(Australia\)**
    -   In this version, the Software Asset Workspace includes the following fixes:
        -   Security fix for Multi Record Associator pop-up page
        -   Fixed incompatible script in 'SAM - Software Estate Weekly Job' PA Job
-   **Version 11.0.10 - July 2026 \(Australia\)**

    In this version, the Software Asset Workspace includes the following fix: Security fix for Multi Record Associator pop-up page

-   **Version 10.0.16 - July 2026 \(Zurich\)**
    -   In this version, the Software Asset Workspace includes the following fixes:
        -   Security fix for Multi Record Associator pop-up page
        -   Fixed incompatible script in 'SAM - Software Estate Weekly Job' PA Job
-   **Version 11.0.9 - June 2026 \(Australia\)**
    -   In this version, the Software Asset Workspace includes the following enhancements:
        -   Value Builder tasks can now be added through the Multi Record Associator \(MRA\) pop-up.
        -   Improved accessibility on the Software Asset Analytics – Discovered Inventory page.
        -   Enhanced reliability of the software estate scheduled job on the Software Asset Analytics – Discovered Inventory page.
-   **Version 10.0.13 - June 2026 \(Zurich\)**
    -   In this version, the Software Asset Workspace includes the following enhancements:
        -   Unlicensed CAL count reporting in the License Workbench has been improved for better accuracy.
        -   Report view ACL configurations now work as expected and do not affect visibility unexpectedly
-   **Version 11.0.5 - May 2026 \(Australia\)**

    Defects were fixed as part of this release.

-   **Version 10.0.9 - May 2026 \(Zurich\)**

    Defects were fixed as part of this release.

-   **Version 11.0.4 - April 2026 \(Australia\)**

    This version contains a defect fix for a critical workspace display issue.

-   **Version 10.0.8 - April 2026 \(Zurich\)**

    Added alerts and banners to indicate if there are any errors or failures in the SaaS integrations, which is part of the new feature 'Resolve SaaS connection errors' in Now Assist for Software Asset Management \(SAM\). This will enable users to debug the error and failures using the logs.

-   **Version 11.0.3 - April 2026 \(Australia\)**
    -   Obligation management has been introduced so SAM admins and users can easily track and follow contract commitments throughout their lifecycle. It is available in the contract record page. Now Assist AI Agents power automated extraction of metadata and obligations directly from contract documents, available to users with the sn\_cm\_gen\_ai.ai\_contract\_fulfiller and sn\_cm\_obligation.obligation\_fulfiller roles.
    -   Updated the visual design and styling of AI banners and highlighters.
-   **Version 11.0.1 - March 2026 \(Australia\)**

    Defect fixes have been implemented in the Software Asset Workspace to enhance performance and the health check dashboard.

-   **Version 10.0.6 - March 2026 \(Zurich\)**

    In the AI activity log card, a new link has been added to show the number of requests fulfilled by the AI agent for Microsoft 365 Subscription products.

-   **Version 10.0.2 - December 2025**

    Software Asset Workspace is an intuitive and streamlined user interface of the Software Asset Management application, to manage software licenses, compliance, and optimization. It is a unified medium with multiple views enabling you to create entitlements, software models, run and review reconciliation results, remediate non compliance, give visibility into your software assets, and provides access to analytics via dashboards.


**Parent Topic:**[ServiceNow Store - IT Asset Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itam-highlight.md)

