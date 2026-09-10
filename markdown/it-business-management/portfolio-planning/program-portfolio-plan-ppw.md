---
title: Programs enhanced experience with portfolio plan view
description: Programs enhanced experience provides dedicated program planning views with zero setup. Access program-scoped planning data including Prioritization, Roadmap, and Financials views for focused program management without navigating portfolio-wide interfaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/program-portfolio-plan-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 3
breadcrumb: [Portfolio plans in Portfolio Planning, Explore, Portfolio Planning, Strategic Portfolio Management]
---

# Programs enhanced experience with portfolio plan view

Programs enhanced experience provides dedicated program planning views with zero setup. Access program-scoped planning data including Prioritization, Roadmap, and Financials views for focused program management without navigating portfolio-wide interfaces.

## What is program enhanced experience?

Program enhanced experience provides dedicated, focused planning interfaces for managing individual programs. Each program receives its own plan with instant access to planning views without requiring setup or configuration. Navigate to the new Programs menu and select any program to open its dedicated plan with program-scoped planning data and multiple visualization options.

Programs enhanced experience includes:

-   **Dedicated program plans:** Each program gets an automatic plan with zero setup
-   **Multiple planning views:** Prioritization, Roadmap, Kanban, and Financials views
-   **Program-scoped data:** View only that program's planning items and data
-   **Fiscal calendar support:** Financials tab defaults to your fiscal calendar
-   **Automatic plan creation:** New programs receive plans instantly; existing programs are backfilled automatically

## Program planning views

Each program plan includes four dedicated planning views:

|View|Purpose|Use Case|
|----|-------|--------|
|Prioritization|Organize and prioritize planning items within the program|Rank initiatives, determine delivery order, manage dependencies|
|Roadmap|Visualize program timeline and schedule across planning items|Track delivery milestones, align timelines, communicate program direction|
|Capacity|Track team resource capacity and allocation|Monitor resource utilization, manage workload, identify constraints, plan allocation|
|Financials|Track program budget, costs, and financial metrics|Monitor spend, forecast costs, manage program financial health|

## Program-scoped data

Program plans display only that program's planning items in a focused, streamlined interface. This scope isolation ensures you see relevant data without portfolio-wide noise. Program-scoped planning data includes:

-   Planning items \(demands, projects, epics, capabilities, features\) assigned to the program
-   Goals and initiatives linked to the program
-   Risks, issues, decisions, actions, and changes associated with program items
-   Financial data specific to the program
-   Program team members and stakeholders

Portfolio-level features such as making plans public and scenario planning are hidden at the program level to maintain focus on program-specific planning.

## Fiscal calendar support

The Financials tab in program plans defaults to your fiscal calendar, displaying program financial data aligned to your organization's fiscal periods. If your fiscal calendar does not span the program's date range, the system gracefully falls back to Gregorian calendar with an explanatory message. This flexibility ensures accurate financial tracking regardless of your calendar configuration.

## Programs menu

A new Programs menu has been added to the workspace as an L2 menu, positioned below Portfolio Plan. The Programs menu lists every program in your portfolio and provides single-click navigation to each program's enhanced planning view. This direct access streamlines program navigation and reduces menu navigation overhead.

## Role-based access for program planning

|Role|Access Level|Permissions|
|----|------------|-----------|
|sn\_align\_core.ap\_read\_only|Read|Can view program plans and planning data \(where they already have program-level read access\)|
|sn\_align\_core.apw\_user|Manage|Can create, update, and manage planning items within program plans|
|Program Manager|Full Access|Automatic plan owner; can manage all aspects of the program plan|

## Automatic plan creation and backfill

Program plans are created automatically with zero setup required:

-   **New programs:** Receive dedicated plans instantly upon creation
-   **Existing programs:** Automatically backfilled with plans in batches of 500 at a time, newest programs first

No manual configuration, template selection, or setup steps are needed. Programs receive full planning functionality immediately.

## Benefits of program enhanced experience

-   **Zero setup:** Program plans are created automatically without configuration
-   **Focused planning:** View only program-scoped data without portfolio-wide distractions
-   **Multiple visualizations:** Choose the planning view that fits your workflow
-   **Fiscal calendar alignment:** Financial data aligns to your organization's fiscal periods
-   **Direct navigation:** Programs menu provides single-click access to each program plan
-   **Role-based security:** Access controlled by established roles for program planning
-   **Automatic plan ownership:** Program managers are automatically assigned as plan owners

**Parent Topic:**[Portfolio plans in Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/portfolio-plans-in-portfolio-planning-ppw.md)

