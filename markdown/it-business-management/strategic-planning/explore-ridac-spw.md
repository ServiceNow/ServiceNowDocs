---
title: Exploring RIDAC in Strategic Planning Workspace
description: RIDAC \(Risk, Issue, Decision, Action, Change\) in Strategic Planning Workspace provides a holistic, portfolio-wide view of all risks, issues, decisions, actions, and changes across your entire organization—from individual projects to programs and portfolios.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/explore-ridac-spw.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 7
keywords: [explore]
breadcrumb: [RIDAC, Strategic Planning, Strategic Portfolio Management]
---

# Exploring RIDAC in Strategic Planning Workspace

RIDAC \(Risk, Issue, Decision, Action, Change\) in Strategic Planning Workspace provides a holistic, portfolio-wide view of all risks, issues, decisions, actions, and changes across your entire organization—from individual projects to programs and portfolios.

## RIDAC overview

RIDAC \(Risk, Issue, Decision, Action, and Change request\) in Strategic Planning Workspace provides a unified view of all RIDAC records across your portfolio hierarchy. Strategic Planning Workspace delivers a holistic perspective that helps teams identify and manage risks, resolve issues, document decisions, track actions, and monitor changes across all planning items, goals, and EAP \(Enterprise Agile Planning\) iterations—without navigating between multiple work items.

## RIDAC users

|User|Description|
|----|-----------|
|Portfolio manager|Portfolio managers use the holistic RIDAC view in Strategic Planning Workspace to understand all risks, issues, decisions, actions, and changes across their entire portfolio. They monitor rolled-up RIDAC records from projects and programs to identify cross-project risks, validate portfolio-level decisions, and ensure alignment between operational activities and strategic objectives.|
|Program manager / PMO leader|Program managers create and manage RIDAC records on their programs and view RIDAC that rolls up from child projects. They assess how project-level risks, issues, and changes impact program delivery and strategic goals. PMO leaders use RIDAC to enforce governance, track decision documentation, and maintain issue resolution workflows across the organization.|
|Project manager / Team lead|Project managers create and manage RIDAC records on their projects. They track risks and issues affecting project delivery, document decisions that shape project direction, maintain action item lists, and register change requests. They can optionally associate RIDAC records with planning items, goals, or EAP iterations to link operational work to strategic priorities.|
|Strategy leader / Executive sponsor|Strategy leaders and executive sponsors use the unified RIDAC view to assess portfolio-wide risks to strategic objectives, review decisions that impact multiple initiatives, and monitor action status across the organization.|

## Supported RIDAC tables

|Table|Description|
|-----|-----------|
|Planning item|Demand|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your demand to manage planning uncertainties and dependencies.|
|Project|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your project to manage planning uncertainties and dependencies.|
|Epic|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your epic to manage planning uncertainties and dependencies.|
|Capability|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your capability to manage planning uncertainties and dependencies.|
|Feature|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your feature to manage planning uncertainties and dependencies.|
|Custom planning item|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your custom planning item to manage planning uncertainties and dependencies.|
|Enterprise agile planning item|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your enterprise agile planning item to manage planning uncertainties and dependencies.|
|Initiative|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your initiative to manage planning uncertainties and dependencies.|
|Strategic program|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your strategic program to manage planning uncertainties and dependencies.|
|Goal|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your goal to manage planning uncertainties and dependencies.|
|EAP iteration|Can create and track Risks, Issues, Decisions, Actions, and Changes directly within your EAP iteration to manage planning uncertainties and dependencies.|

**Note:** A RIDAC record can be linked to any of these items: a planning item, a goal, or an EAP iteration.

## RIDAC benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Unified portfolio visibility of risks, issues, decisions, actions, and changes across all projects and programs|Holistic RIDAC view in Strategic Planning Workspace|Portfolio managers, PMO leaders, strategy leaders|
|Automatic rollup of RIDAC through portfolio hierarchy—see project risks at program and portfolio levels|RIDAC rollup mechanics|Program managers, portfolio managers|
|Connect operational RIDAC to strategic objectives by linking to planning items, goals, or EAP iterations|RIDAC entity associations \(planning items, goals, EAP iterations\)|Project managers, program managers, strategy leaders|
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

-   [Populate planning items on RIDAC records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/update-ridac-planning-items-spw.md) — Run the scheduled job to populate the planning item field on RIDAC records created before the latest release. This ensures legacy RIDAC records appear correctly in related lists and reports.
-   [View RIDAC records for planning items, goals, or EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/view-ridac-records-spw.md) — View different RIDAC records by planning scope \(All RIDAC, Project RIDAC, Portfolio RIDAC, or Program RIDAC\) from a single centralized view.
-   [Create RIDAC for a planning item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/create-ridac-planning-item-spw.md) — Create and associate Risk, Issue, Decision, Action, or Change items directly with planning items \(projects, demands, epics, features, or custom planning items\) to manage planning uncertainties and dependencies.
-   [Create RIDAC for a goal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/create-ridac-goal-spw.md) — Create and associate Risk, Issue, Decision, Action, or Change items directly with portfolio plan goals or goals on a board \(Strategy and Goals\) to manage goal-level planning challenges.
-   [Create RIDAC for an EAP iteration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/create-ridac-eap-iteration-spw.md) — Create and associate Risk, Issue, Decision, Action, or Change items directly with Enterprise Agile Planning \(EAP\) iterations to manage iteration-level planning risks and agile execution challenges.
-   [Export RIDAC list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/export-ridac-list-spw.md) — Export a filtered list of RIDAC records to Excel, PDF, CSV, or JSON format. You can download the file directly or send it via email to share RIDAC information with stakeholders.

