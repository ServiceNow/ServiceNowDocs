---
title: Using RIDAC in Strategic Planning Workspace
description: Access and filter risks, issues, decisions, actions, and changes from a centralized RIDAC home page. Use multiple filtering levels organized by planning scope to focus on the RIDAC items most relevant to your role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/using-ridac-spw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 4
keywords: [use]
breadcrumb: [RIDAC, Strategic Planning, Strategic Portfolio Management]
---

# Using RIDAC in Strategic Planning Workspace

Access and filter risks, issues, decisions, actions, and changes from a centralized RIDAC home page. Use multiple filtering levels organized by planning scope to focus on the RIDAC items most relevant to your role.

## Roles required for using RIDAC

<table id="table_y1f_zgp_43c"><thead><tr><th>

Access level

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

Read access to RIDAC

</td><td>

sn\_align\_ws.ridac\_read\_only**Note:** The following three roles automatically include the sn\_align\_ws.ridac\_read\_only role by default. This provides read-only access to RIDAC records for their respective planning scopes.

-   sn\_align\_core.ap\_read\_only - Read-only access to RIDAC records for planning items
-   sn\_apw\_advanced.spw\_goal\_user\_read - Read-only access to RIDAC records for strategic goals
-   sn\_apw\_advanced.eap\_read\_only - Read-only access to RIDAC records for EAP iterations

</td></tr><tr><td>

Edit access to RIDAC

</td><td>

sn\_align\_ws.ridac\_user**Note:** The following three roles automatically include the sn\_align\_ws.ridac\_user role by default. This provides full access to create, edit, and manage RIDAC records for their respective planning scopes:

-   sn\_align\_core.apw\_user - Full access to manage RIDAC records for planning items
-   sn\_apw\_advanced.spw\_goal\_user - Full access to manage RIDAC records for strategic goals
-   sn\_apw\_advanced.eap\_user - Full access to manage RIDAC records for EAP iterations

</td></tr></tbody>
</table>## Overview of RIDAC home page

The RIDAC home page provides a centralized view of all risks, issues, decisions, actions, and changes across your strategic planning portfolio. The interface is organized into four filtering tabs, each designed to help different roles quickly locate and focus on the RIDAC items most relevant to their planning responsibilities.

\[Omitted image "ridac-home-page-spw.png"\] Alt text: RIDAC Home Page in Strategic Planning Workspace

The RIDAC home page offers multiple filtering tabs to accommodate different roles and planning scopes. Project managers, portfolio managers, and program managers each need focused views of planning risks and issues. By providing separate tabs for project, portfolio, and program contexts—alongside a comprehensive all-items view—the interface makes it easier to filter and analyze RIDAC items relevant to your specific planning responsibilities.

**Access and Visibility:** Each RIDAC tab displays only the items you have access to based on your user permissions and role assignments. Your visibility is determined by your access to the underlying planning items and their associated RIDAC records.

The four RIDAC filtering tabs are:

-   **All RIDAC** — Displays every risk, issue, decision, action, and change that you have access to across your entire planning portfolio. This view includes RIDAC items created on all planning item types—projects, demands, features, product areas, and more. Use this tab for a comprehensive overview of all planning uncertainties and dependencies you're responsible for, regardless of their planning scope or parent type.

-   **Project RIDAC** — Shows only RIDAC items created on project planning items. Use this tab when you want to focus on risks, issues, decisions, actions, and changes specific to projects without viewing items from other planning item types.

-   **Portfolio RIDAC** — Displays RIDAC items associated with planning items that have a top portfolio assignment. These are items that roll up to a portfolio and are scoped by portfolio context. Use this tab to analyze cross-project impacts, portfolio-level planning dependencies, and strategic risks across one or multiple portfolios.

-   **Program RIDAC** — Shows RIDAC items where a program is the top-level parent. These are items scoped at the program level. Use this tab to track risks, issues, decisions, actions, and changes across program initiatives and interdependencies within single or multiple programs.


## Using RIDAC

Using RIDAC in Strategic Planning Workspace allows you to manage planning risks, issues, decisions, actions, and changes across your entire portfolio hierarchy. You can view RIDAC items from a centralized home page with multiple filtering options, or create new RIDAC items directly from planning items \(projects, demands, epics, features, and custom planning items\), strategic goals, or EAP iterations. Whether you're tracking cross-project impacts at the portfolio level or managing iteration-level execution challenges, RIDAC helps you maintain visibility of planning uncertainties and dependencies throughout your organization.

-   [View RIDAC records for planning items, goals, or EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/view-ridac-records-spw.md)

    View different RIDAC records by planning scope \(All RIDAC, Project RIDAC, Portfolio RIDAC, or Program RIDAC\) from a single centralized view.

-   [Create RIDAC for a planning item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/create-ridac-planning-item-spw.md)

    Create and associate Risk, Issue, Decision, Action, or Change items directly with planning items \(projects, demands, epics, features, or custom planning items\) to manage planning uncertainties and dependencies.

-   [Create RIDAC for a goal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/create-ridac-goal-spw.md)

    Create and associate Risk, Issue, Decision, Action, or Change items directly with portfolio plan goals or goals on a board \(Strategy and Goals\) to manage goal-level planning challenges.

-   [Create RIDAC for an EAP iteration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/create-ridac-eap-iteration-spw.md)

    Create and associate Risk, Issue, Decision, Action, or Change items directly with Enterprise Agile Planning \(EAP\) iterations to manage iteration-level planning risks and agile execution challenges.

-   [Export RIDAC list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/export-ridac-list-spw.md)

    Export a filtered list of RIDAC records to Excel, PDF, CSV, or JSON format. You can download the file directly or send it via email to share RIDAC information with stakeholders.


