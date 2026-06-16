---
title: Procurement Specialist Workspace release notes
description: Version history for the Procurement Specialist Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-procurement-specialist-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Procurement Specialist Workspace release notes

Version history for the Procurement Specialist Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 17.0.1 - June 2026 \(Zurich\)**
    -   New:
        -   AI‑powered Savings Opportunity Discovery in Source‑to‑Pay Workspace: Savings opportunities are now surfaced in two locations within the Source‑to‑Pay Workspace:
            -   A unified Potential Savings Opportunities page that lists all opportunities accessible to the signed‑in user
            -   A Category Management tab scoped to the relevant spend categoryFrom either location, users can select Learn more to open the Now Assist panel for a specific opportunity. The panel provides supporting insights, enables follow‑up questions, allows users to run simulations, and supports taking action or dismissing the opportunity.
-   **Version 16.1.0 - May 2026 \(Zurich\)**

    Minor UI enhancements.

-   **Version 19.0.1 - April 2026 \(Australia\)**

    Changed: Fixed the Now Assist summarization banner for Emails and Cases.

-   **Version 14.0.2 - March 2026**
    -   New:
        -   Assess supplier performance at scale powered by the Smart Assessment Engine:
            -   Bulk distribution via segmentation rules: Associates assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one‑off outreach.
            -   Internal stakeholder completion: Lets sourcing and procurement teams complete assessments directly in the Source‑to‑Pay Workspace, keeping evaluations centralized and auditable.
-   **Version 15.0.2 - December 2025 \(Zurich\)**
    -   New:
        -   A new Pipeline management tab has been added to the Source-to-Pay workspace. Access to this tab is controlled by the sn\_spend\_pipeline.sourcing\_pipeline\_user role. This tab provides sourcing managers with:
            -   Personalized savings performance
            -   Action cards to quickly navigate to time-sensitive projects
            -   Visualizations of active work
            -   Direct access to all assigned pipeline projects
        -   A new Category analytics module is available in the Source-to-Pay workspace. Selecting this module loads the Savings dashboard, powered entirely by pipeline project data. This dashboard helps users analyze category performance, track potential and realized savings, and monitor project progress from opportunity identification to savings realization. Users with the sn\_spend\_mgmt.sourcing\_category\_manager role can view and access the Savings dashboard in the Category Analytics module.
        -   A new Category management tab has been added within the Source-to-Pay workspace. This tab includes the following components:
            -   Workspace-level global filters
            -   Overview section
            -   Action-focused insight tabs
            -   Pipeline project creation from insights across all three sub-tabs
            -   Supplier record enhancements
-   **Version 5.0.0 - February 2023**
    -   Changed: Modified the data source for case records to render in the Procurement Workspace, such that a fulfiller working on both supplier and procurement cases would be able to view both in the same list.
        -   **Note:** Existing customers will be impacted by these changes in the data model source, allowing them to create both supplier and procurement cases.

-   **Version 4.0.2 - December 2022**

    Minor fixes.

-   **Version 4.0.1 - November 2022**

    Minor fixes.

-   **Version 3.0.1 - August 2022**
    -   Changed:
        -   Updated the sourcing request experience in workspace to be able to create new or add to existing negotiation events directly in a sourcing request record.
        -   Updated the experience to discover and find:
            -   Related cases and tasks to procurement cases within the contextual sidebar in procurement case records.
            -   Related child cases and tasks to negotiation events and negotiations within the contextual sidebar in negotiation events and negotiation records.
        -   Updated the supplier profile page to improve your configuration experience.
-   **Version 2.0.2 - May 2022**
    -   New:
        -   New procurement workspace landing page for procurement fulfillers to seamlessly launch into their day, by rendering the following:
            -   Work which needs their attention
            -   Overdue, new, and upcoming work
            -   Quick actions into internal and external links
            -   A distribution of their workload
            -   Recently updated work
            -   Followed suppliers
        -   Visually see work that is prioritized as high, critical, moderate, and low.
        -   New and visual way to manage multiple supplier negotiations.
        -   Enriched supplier profile view in the procurement workspace with the Supplier Lifecycle Management plugin.
-   **Version 1.2.1- February 2022**
    -   New: Introduced a new procurement workspace experience for procurement fulfillers to easily view all open tasks within a work record \(sourcing requests and purchase requisitions\).
    -   Changed:
        -   Delivery address task types have changed to additionally show related purchases using the same delivery address. This helps procurement fulfillers to complete delivery address approvals faster.
        -   Delivery address task form layouts have changed to support the work to be done.

