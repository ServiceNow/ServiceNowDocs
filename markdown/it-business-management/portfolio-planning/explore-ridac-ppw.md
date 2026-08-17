---
title: RIDAC in Portfolio Planning Workspace
description: RIDAC \(Risk, Issue, Decision, Action, Change\) in Portfolio Planning Workspace provides a holistic, portfolio-wide view of all risks, issues, decisions, actions, and changes across your entire organization—from individual projects to programs and portfolios.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-planning/explore-ridac-ppw.html
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 4
keywords: [explore]
breadcrumb: [Explore, Portfolio Planning, Strategic Portfolio Management]
---

# RIDAC in Portfolio Planning Workspace

RIDAC \(Risk, Issue, Decision, Action, Change\) in Portfolio Planning Workspace provides a holistic, portfolio-wide view of all risks, issues, decisions, actions, and changes across your entire organization—from individual projects to programs and portfolios.

## RIDAC overview

RIDAC \(Risk, Issue, Decision, Action, and Change request\) in Strategic Planning Workspace provides a unified view of all RIDAC records across your portfolio hierarchy. Portfolio Planning Workspace delivers a holistic perspective that helps teams identify and manage risks, resolve issues, document decisions, track actions, and monitor changes across all planning items \(project and demand\)—without navigating between multiple work items.

## Supported RIDAC tables

|Table|Description|
|-----|-----------|
|Planning item \(Demand\)|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your demand to manage planning uncertainties and dependencies.|
|Planning item \(Project\)|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your project to manage planning uncertainties and dependencies.|

**Note:** A RIDAC record can be linked to any of these items: a planning item, a goal, or an EAP iteration.

## RIDAC benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Unified portfolio visibility of risks, issues, decisions, actions, and changes across all projects and demands|Holistic RIDAC view in Portfolio Planning Workspace|Portfolio managers, PMO leaders, strategy leaders|
|Automatic rollup of RIDAC through portfolio hierarchy—see project risks at program and portfolio levels|RIDAC rollup mechanics|Program managers, portfolio managers|
|Track RIDAC across both alignment and execution project systems with automatic cross-system reference population|Execution and alignment integration for RIDAC|Project managers with dual project management systems|

## RIDAC integration with planning and execution Items

When integration is enabled, RIDAC items maintain a bidirectional link between planning items \(demands and projects\) and execution items \(tasks\). This means:

-   **Create a RIDAC on a planning item** - Execution details from any linked execution task automatically populate on the RIDAC record.
-   **Create a RIDAC on an execution item** - Planning item details automatically populate on the RIDAC record.

Because the link is bidirectional, a RIDAC item created from either context—planning or execution—contains both planning and execution information, giving stakeholders a complete view of risks, issues, decisions, actions, and changes across the planning and delivery lifecycle.

Example: If you add a RIDAC item to a project, you can view the same RIDAC item details in the project workspace. This ensures that planning stakeholders and execution teams see the same risk, issue, decision, action, or change data without duplicating work.

## Comparing RIDAC feature between Strategic Planning and Portfolio Planning

Strategic Planning Workspace extends RIDAC capabilities beyond what is available in Portfolio Planning. The following comparison shows the key differences in supported entities and features.

-   Portfolio Planning: Create and manage RIDAC items for projects and demands to track risks, issues, decisions, actions, and changes across your portfolio. For more information, see [Using RIDAC in Strategic Planning Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/using-ridac-spw.md).
-   Strategic Planning: Create and manage RIDAC items for all planning item types \(projects, demands, epics, capabilities, features, and custom planning items\), goals, and EAP iterations. You also gain access to AI-generated RIDAC capabilities and expanded governance controls.

<table id="table_bmt_jnf_fwb"><thead><tr><th>

Supported table for RIDAC creation

</th><th>

Portfolio Planning

</th><th>

Strategic Planning

</th></tr></thead><tbody><tr><td>

Planning items: Supported planning items

</td><td>

\[Omitted image "icon-check-mark-green.png"\] Alt text: YesProject, Demand

</td><td>

\[Omitted image "icon-check-mark-green.png"\] Alt text: YesProject, Demand, Epic, Capability, Feature, Custom planning item, Enterprise agile planning item, Initiative, Strategic program

</td></tr><tr><td>

Goal

</td><td>

\[Omitted image "icon-error-red-x.png"\] Alt text: No

</td><td>

\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes

</td></tr><tr><td>

EAP Iteration

</td><td>

\[Omitted image "icon-error-red-x.png"\] Alt text: No

</td><td>

\[Omitted image "icon-check-mark-green.png"\] Alt text: Yes

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using RIDAC Strategic Planning Workspace, see:

-   [Populate planning items on RIDAC records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/update-ridac-planning-items-ppw.md) — Run the scheduled job to populate the planning item field on RIDAC records created before the latest release. This ensures legacy RIDAC records appear correctly in related lists and reports.
-   [View RIDAC records for planning items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/view-ridac-records-ppw.md) — View different RIDAC records by planning scope \(All RIDAC, Project RIDAC, Portfolio RIDAC, or Program RIDAC\) from a single centralized view.
-   [Create RIDAC for a planning item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/create-ridac-planning-item-ppw.md) — Create and associate Risk, Issue, Decision, Action, or Change items directly with planning items \(projects and demands\) to manage planning uncertainties and dependencies.
-   [Export RIDAC list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/export-ridac-list-ppw.md) — Export a filtered list of RIDAC records to Excel, PDF, CSV, or JSON format. You can download the file directly or send it via email to share RIDAC information with stakeholders.

**Parent Topic:**[Exploring Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/exploring-portfolio-planning.md)

