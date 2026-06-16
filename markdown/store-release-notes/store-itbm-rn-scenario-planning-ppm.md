---
title: Scenario Planning for PPM release notes
description: Version history for the IT Business Management Scenario Planning for PPM on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-scenario-planning-ppm.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Scenario Planning for PPM release notes

Version history for the IT Business Management Scenario Planning for PPM on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.6.0 - June 2026**
    -   New:
        -   Added out-of-the-box query\_range ACLs for multiple tables.
        -   Added two fix scripts to carry forward customizations seamlessly during the Cobalt directive upgrade.
        -   Added a deprecation banner to the Scenario Planning page.
-   **Version 2.4.0 - December 2025**
    -   Changed: Implemented the Read-Only Field Remediation Security Directive for the Scenario Planning for PPM \(app-ppm-scenario-planning\) application.
    -   Fixed: \[Security\] Resolved an ACL bypass vulnerability in the Portfolio Workbench Scenario Planning Scripted REST API for the Scenario Planning for PPM \(app-ppm-scenario-planning\) application.
-   **Version 2.3.6 - February 2025**

    Fixed: The Planning Window field displays multiple languages in Scenario Planning in Portfolio Planning Workbench.

-   **Version 2.3.5 - September 2024**
    -   Fixed:
        -   Redirecting to new Project Workspace instead of classic workspace from Scenario Planning.
        -   \[Security Bug\] Table ACL Bypass via GlideAggregate/GlideRecord Encoded Query - DIRS0000179.
-   **Version 2.3.3 - September 2023**

    Fixed: When approving and overriding the working changes of a project that was converted from a demand, the demand's state moves from completed to approved.

-   **Version 2.3.1 - April 2023**
    -   New: Added report-view ACLs for all scenario tables.
    -   Fixed:
        -   Rank changes in draft scenario should not update the confirm scenario ranking.
        -   Order of Rank by Score.
-   **Version 2.3.0 - August 2022**

    Changed: Supporting the integration with the Investment Funding store application and note that if the Investment Funding family plugin is installed and not upgraded to the store version, integration might fail to work.

-   **Version 2.2.0 - March 2022**
    -   Changed: Upgraded Angular and JQuery versions
    -   Fixed: Functional and accessibility issues
-   **Version 2.1.1 - October 2021**
    -   Fixed:
        -   Operation resource plans for resource utilization in the portfolio planning workbench
        -   Populating the resource tab console for the demand resource plan when a Heat Map box is selected
        -   Selected-items filter is removed after refreshing
        -   Upgrade issue in Quebec and others
-   **Version 2.1.0 - January 2021**

    Fixed: Fixes to support for teamspace portfolios.

-   **Version 2.0.1 - November 2020**
    -   New:
        -   Plan your portfolio based on resource capacity for a single year or multiple years.
        -   Break down your multiple year portfolio planning in smaller planning windows for continuous tracking and planning adjustment.
        -   Allocate budget to demands and projects in your portfolio from Investment Funding.
        -   Apply filters to refine your list of selected demands and projects in your portfolio.
        -   View details of demands and projects that are not aligned with your strategic goals.
        -   View demands and projects with over-allocated resources.
        -   Paginated view is added to easily view the selected demands and projects.
    -   Changed:
        -   Resources tab is moved to next to Timeline View.
        -   Resource utilization view is now based on the calendar year and can be viewed monthly or quarterly.
        -   Additional widgets on the tracking page.
    -   Fixed: Performance improvement.
-   **Version 1.1.0 - July 2020**
    -   New: Updated for Paris support.
    -   Fixed:
        -   Incorrect Overallocated Group number when a resource plan contains planned hours while comparing scenarios.
        -   Icons in the Track tab and Create new scenario pop-up.
        -   Loading of Scenario Planning Timeline view.
        -   Autoranking when rank is edited manually.
        -   404 error when clicking the Portfolio Planning Workbench module for the first time.
        -   Proposed capex and opex budget columns while selecting projects and loading of percent utilisation in the Resource tab.
-   **Version 1.0.1 - May 2020**
    -   Scenario Planning for PPM enables Portfolio Managers to plan their portfolio investment, work and resources using multiple “what-if” scenarios. Scenarios may include different project or demand selections, as well as a different way of funding them. The apps also includes a variety of tools to analyze financials investments and benefits, resource utilization, strategic alignment of the selected projects and demands, as well as a comparison module for side-by-side scenario comparison.
    -   This app also helps track performance of the portfolio plan, and if modification are needed to accommodate business changes, replanning can also be done using scenarios.

