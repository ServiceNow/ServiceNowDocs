---
title: GRC: Advanced Audit release notes
description: Version history for the GRC: Advanced Audit on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-advanced-audit.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Advanced Audit release notes

Version history for the GRC: Advanced Audit on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.1 - June 2026 \(Australia\)**
    -   New: Enhanced application review with relevant query range ACLs.
    -   Changed: User roles now contain feature roles.
    -   Fixed: Corrected the dictionary override shipped for business\_app\_request.watch\_list.
-   **Version 22.0.1 - March 2026**
    -   Fixed:
        -   Observations can now be editable even if owner and respondent are same.
        -   Security defect fixes.
-   **Version 21.1.2 - December 2025 \(Zurich\)**

    Fixed: Fixed security defects.

-   **Version 21.0.1 - August 2025**
    -   New: Enhanced security on Observation, Auditable unit tables by introducing range queries.
    -   Fixed: Security bugs fixed.
-   **Version 20.2.0 - June 2025**

    Fixed: Enhanced security by creating Query range ACLs across multiple tables.

-   **Version 20.1.0 - May 2025**

    New: Entity-based access capabilities now supported for Advanced Audit. EBA can be leveraged to manage access to Observations.

-   **Version 20.0.1 - February 2025**

    Fixed: Security issues related to client callable script includes.

-   **Version 19.1.1 - November 2024**

    Changed: Security fixes.

-   **Version 19.0.1 - August 2024**
    -   New:
        -   Audit reader role for all read operators.
        -   Audit approver role for approval of Engagements and Audit plans.
-   **Version 18.0.0 - February 2024**

    Changed: Upgrades related to Advanced risk assessments on auditable units.

-   **Version 17.0.1 - August 2023**
    -   Changed: Access controls for tables extending planned task tables.
    -   Fixed: Observations report is not showing up on issue landing page on workspace.
-   **Version 16.0.2 - July 2023**

    Fixed: Addressed an issue where the Runtime access tracking field's value was inadvertently changing from "None" to "Enforcing" during the Utah upgrade.

-   **Version 16.0.1 - February 2023**
    -   Changed: Support for Localization
    -   Fixed: Access controls for viewing reports
-   **Version 15.0.4 - December 2022**

    Fixed: Reduction in installation size of the application.

-   **Version 15.0.3 - August 2022**
    -   Fixed:
        -   Audit Plan End date is not populated when the System date format is changed.
        -   When other language packs are installed, Observations are not getting Closed on Finalize.
        -   When an Observation is closed as an Issue, not able to assign Issue Manager on Observation.
-   **Version 14.1.1 - March 2022**

    New: Security updates

-   **Version 13.0.2 - September 2021**
    -   New: Added support for Workspaces
    -   Fixed:
        -   Security access issue on Milestones table
        -   Error on Time card portal while adding unassigned record in the timesheet when Advanced Audit is installed.
-   **Version 12.0.2 - June 2021**

    Fixed: Security issues.

-   **Version 12.0.1 - March 2021**
    -   New: PPM Timesheets Integration for Engagements and Audit Tasks.
    -   Fixed: Addressed security issues, observation issues.
-   **Version 11.0.1 - October 2020**
    -   New:
        -   Perform basic resource and cost planning
        -   Perform detailed resource and cost planning, and timecard tracking using Project Portfolio Management \(PPM\) integration
        -   Track observations as reportable issues or simply close them as recommendation or best practice
        -   Track engagement milestones

