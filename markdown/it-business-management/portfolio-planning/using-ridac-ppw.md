---
title: Using RIDAC in Portfolio Planning Workspace
description: Access and filter risks, issues, decisions, actions, and changes from a centralized RIDAC home page. Use multiple filtering levels organized by planning scope to focus on the RIDAC items most relevant to your role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/using-ridac-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 3
keywords: [use]
breadcrumb: [Portfolio Planning, Strategic Portfolio Management]
---

# Using RIDAC in Portfolio Planning Workspace

Access and filter risks, issues, decisions, actions, and changes from a centralized RIDAC home page. Use multiple filtering levels organized by planning scope to focus on the RIDAC items most relevant to your role.

## Roles required for using RIDAC

<table id="table_y1f_zgp_43c"><thead><tr><th>

Access level

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

Read access to RIDAC

</td><td>

sn\_align\_ws.ridac\_read\_only**Note:** The sn\_align\_core.ap\_read\_only role automatically include the sn\_align\_ws.ridac\_read\_only role by default. This provides read-only access to RIDAC records for their respective planning scopes.

</td></tr><tr><td>

Edit access to RIDAC

</td><td>

sn\_align\_ws.ridac\_user**Note:** The sn\_align\_core.apw\_user role automatically include the sn\_align\_ws.ridac\_user role by default. This provides full access to create, edit, and manage RIDAC records for their respective planning scopes:

</td></tr></tbody>
</table>## Overview of RIDAC home page

The RIDAC home page provides a centralized view of all risks, issues, decisions, actions, and changes across your portfolio planning portfolio. The interface is organized into four filtering tabs, each designed to help different roles quickly locate and focus on the RIDAC items most relevant to their planning responsibilities.

\[Omitted image "ridac-home-page-ppw.png"\] Alt text: RIDAC Home Page in Portfolio Planning Workspace

The RIDAC home page offers multiple filtering tabs to accommodate different roles and planning scopes. Project managers, portfolio managers, and program managers each need focused views of planning risks and issues. By providing separate tabs for project, portfolio, and program contexts—alongside a comprehensive all-items view—the interface makes it easier to filter and analyze RIDAC items relevant to your specific planning responsibilities.

**Access and Visibility:** Each RIDAC tab displays only the items you have access to based on your user permissions and role assignments. Your visibility is determined by your access to the underlying planning items and their associated RIDAC records.

The four RIDAC filtering tabs are:

-   **All RIDAC** — Displays every risk, issue, decision, action, and change that you have access to across your entire planning portfolio. This view includes RIDAC items created on all planning item types—projects and demands. Use this tab for a comprehensive overview of all planning uncertainties and dependencies you're responsible for, regardless of their planning scope or parent type.

-   **Project RIDAC** — Shows only RIDAC items created on project planning items. Use this tab when you want to focus on risks, issues, decisions, actions, and changes specific to projects without viewing items from other planning item types.

-   **Portfolio RIDAC** — Displays RIDAC items associated with planning items that have a top portfolio assignment. These are items that roll up to a portfolio and are scoped by portfolio context. Use this tab to analyze cross-project impacts, portfolio-level planning dependencies and risks across one or multiple portfolios.

-   **Program RIDAC** — Shows RIDAC items where a program is the top-level parent. These are items scoped at the program level. Use this tab to track risks, issues, decisions, actions, and changes across programs and portfolios within single or multiple programs.


## Using RIDAC

Using RIDAC in Portfolio Planning Workspace allows you to manage planning risks, issues, decisions, actions, and changes across your entire portfolio hierarchy. You can view RIDAC items from a centralized home page with multiple filtering options, or create new RIDAC items directly from planning items \(projects and demands\). When you're tracking cross-project impacts at the portfolio level, RIDAC helps you maintain visibility of planning uncertainties and dependencies throughout your organization.

-   [View RIDAC records for planning items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/view-ridac-records-ppw.md)

    View different RIDAC records by planning scope \(All RIDAC, Project RIDAC, Portfolio RIDAC, or Program RIDAC\) from a single centralized view.

-   [Create RIDAC for a planning item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/create-ridac-planning-item-ppw.md)

    Create and associate Risk, Issue, Decision, Action, or Change items directly with planning items \(projects and demands\) to manage planning uncertainties and dependencies.

-   [Export RIDAC list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/export-ridac-list-spw.md)

    Export a filtered list of RIDAC records to Excel, PDF, CSV, or JSON format. You can download the file directly or send it via email to share RIDAC information with stakeholders.


