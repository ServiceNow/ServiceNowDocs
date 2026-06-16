---
title: Source-to-Pay Workspace release notes
description: Version history for the Source-to-Pay Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-source-to-pay-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Source-to-Pay Workspace release notes

Version history for the Source-to-Pay Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 20.0.1 - June 2026 \(Australia\)**
    -   New:
        -   AI‑powered Savings Opportunity Discovery in Source‑to‑Pay Workspace: Savings opportunities are now surfaced in two locations within the Source‑to‑Pay Workspace:
            -   A unified Potential Savings Opportunities page that lists all opportunities accessible to the signed‑in user
            -   A Category Management tab scoped to the relevant spend categoryFrom either location, users can select Learn more to open the Now Assist panel for a specific opportunity. The panel provides supporting insights, enables follow‑up questions, allows users to run simulations, and supports taking action or dismissing the opportunity.
-   **Version 17.0.1 - June 2026 \(Zurich\)**
    -   New:
        -   AI‑powered Savings Opportunity Discovery in Source‑to‑Pay Workspace: Savings opportunities are now surfaced in two locations within the Source‑to‑Pay Workspace:
            -   A unified Potential Savings Opportunities page that lists all opportunities accessible to the signed‑in user
            -   A Category Management tab scoped to the relevant spend categoryFrom either location, users can select Learn more to open the Now Assist panel for a specific opportunity. The panel provides supporting insights, enables follow‑up questions, allows users to run simulations, and supports taking action or dismissing the opportunity.
-   **Version 14.2.1 - June 2026**
    -   Compliance:
        -   Performed WCAG 2.2 accessibility \(A11y\) visual regression testing on the Source‑to‑Pay workspace to ensure compliance with accessibility standards.
    -   Defect Fixes:
        -   Fixed a security vulnerability that allowed ACL bypass through the “Get suppliers” Data Broker.
        -   Resolved multiple workspace UX issues, including:
            -   Templates not attaching for non‑admin users
            -   Explore with AI button not appearing for Suppliers
            -   Scorecard display truncation on the landing page
-   **Version 19.1.0 - May 2026**

    Minor UI enhancements

-   **Version 16.1.0 - May 2026 \(Zurich\)**

    Minor UI enhancements.

-   **Version 19.0.1 - April 2026 \(Australia\)**

    Changed: Fixed the Now Assist summarization banner for Emails and Cases.

-   **Version 16.0.1 - April 2026 \(Zurich\)**

    Changed: Fixed the Now Assist summarization banner for Emails and Cases.

-   **Version 19.0.0 - March 2026 \(Australia\)**
    -   New:
        -   Assess supplier performance at scale powered by the Smart Assessment Engine:
            -   Bulk distribution via segmentation rules: Associates assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one‑off outreach.
            -   Internal stakeholder completion: Lets sourcing and procurement teams complete assessments directly in the Source‑to‑Pay Workspace, keeping evaluations centralized and auditable.
        -   Tracks a granular admin role warning in the UXF GRD configuration for future resolution.
        -   Adds PO spend and POE creation history by supplier to the Exception Intelligence tab for improved analysis.
        -   Expands the New Activities Today section on the landing page.
    -   Changed:
        -   Enables reassignment and priority updates for PO Exceptions by the POE assignee.
        -   Enhances the Exception Intelligence tab by displaying POL quantity data in the Exception Impact chart.
        -   Updates the Exception Record code to display phased delivery details in a card.
        -   Improves Purchase Order Exception creation through Universal Request.
-   **Version 16.0.0 - March 2026 \(Zurich\)**
    -   New:
        -   Assess supplier performance at scale powered by the Smart Assessment Engine:
            -   Bulk distribution via segmentation rules: Associates assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one‑off outreach.
            -   Internal stakeholder completion: Lets sourcing and procurement teams complete assessments directly in the Source‑to‑Pay Workspace, keeping evaluations centralized and auditable.
        -   Adds PO spend and POE creation history by supplier to the Exception Intelligence tab for improved analysis.
        -   Expands the New Activities Today section on the landing page.
    -   Changed:
        -   Enables reassignment and priority updates for PO Exceptions by the POE assignee.
        -   Enhances the Exception Intelligence tab by displaying POL quantity data in the Exception Impact chart.
        -   Updates the Exception Record code to display phased delivery details in a card.
        -   Improves Purchase Order Exception creation through Universal Request.
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
-   **Version 13.3.2 - December 2025 \(Yokohama\)**
    -   New:
        -   A new Pipeline management tab has been added to the Source-to-Pay workspace. Access to this tab is controlled by the sn\_spend\_pipeline.sourcing\_pipeline\_user role. This tab provides sourcing managers with:
            -   Personalized savings performance
            -   Action cards to quickly navigate to time-sensitive projects
            -   Visualizations of active work
            -   Direct access to all assigned pipeline projects
        -   A new Category analytics module is available in the Source-to-Pay workspace. Selecting this module loads the Savings dashboard, powered entirely by pipeline project data. Users with the sn\_spend\_mgmt.sourcing\_category\_manager role can view and access the Savings dashboard in the Category Analytics module.
        -   A new Category management tab has been added within the Source-to-Pay workspace. This tab includes the following components:
            -   Workspace-level global filters
            -   Overview section
            -   Action-focused insight tabs
            -   Pipeline project creation from insights across all three sub-tabs
            -   Supplier record enhancements
-   **Version 14.0.1 - August 2025**

    Minor fixes.

-   **Version 13.2.0 - May 2025**

    Minor fixes.

-   **Version 11.0.8 - October 2024**

    Enabled retry for Purchase Order and Goods Receipt in workspace.

-   **Version 11.0.1 - August 2024**
    -   New:
        -   AP specialists can now view invoice images on invoice line forms.
        -   A task owner can now view and handle invoice tasks more efficiently using task filters, widgets, and bar charts in the Accounts Payable Operations workspace.
    -   Fixed: Fixed an issue that was causing the DocIntel page to open up in a new workspace tab, instead of a sub-tab under the invoice processing case.
-   **Version 10.0.3 - June 2024**

    Defect fixes.

-   **Version 10.0.2 - May 2024**
    -   New: A new related list tab for emails is now available to capture all business correspondence done over emails. This tab will display both sent and draft emails.
    -   Changed:
    -   -   Simplified the case form for fulfillers to view only relevant fields. These will be rendered automatically depending on the type of the record. For example, if a related purchase requisition is populated, then the fulfiller will see the Order dependent on casefield, and not the Sourcing decision dependent on case and Qualification dependent on case fields. Simialrly, fields like Created date will no longer be visible because they are not adding any value to the case form and are just making it crowded.
-   Simplified the purchase line form for fulfillers to view contextual details within the sourcing and negotiation workflows, and the purchasing workflows. Existing customers will see a change in their form layout in both workspace and Platform views.
-   Simplified the sourcing request form for fulfillers to easily navigate and discover fields that matter, to make sourcing decisions. Existing customers will see a change in their form layout in both workspace and Platform views.
-   **Version 9.2.1 - March 2024**

    New: Introduced a new due diligence playbook case for procurement specialists to perform risk assessment for suppliers.

-   **Version 9.0.1 - February 2024**
    -   Changed:
        -   Customers with the entire Source-to-Pay \(S2P\) product suite, or any of the individual products within the S2P suite, now share the same workspace, where content within the workspace is role-based. Fulfillers will see multiple or single landing pages, and have access to different lists based on their roles. Existing customers who built their own workspace landing pages for SPO, SLO, or APO will see their landing pages within the single workspace.
        -   Fulfillers can now create procurement tasks with actions types E-sign, Upload a document, and Submit a form, from Source-to-Pay workspace pages.
-   **Version 8.0.5 - December 2023**

    Minor fixes.

-   **Version 8.0.2 - November 2023**
    -   New:
        -   Ability to add additional existing suppliers and additional sourcing requests to a negotiation event, where negotiation activities are in progress. Note: Existing and new customers will have the capability to manage three bids and a buy, or competitive bidding within the sourcing workflow.
        -   New experience in Source-to-Pay Workspace for purchase requisitions and procurement case records to have more purposeful contextually grouped related tabs, to reduce clustering and improve organizing of contract agreement records. Note: Existing customers will find these new changes in effect with this upgrade.
        -   New supplier card in the contextual tab for all objects like purchase requisitions, sourcing requests, negotiation events, negotiations, and case records. This card provides a quick overview of all the suppliers that are relevant for that record. Note: Existing customers will find these new changes in effect with this upgrade.
-   **Version 7.0.0 - August 2023**

    Provides a single environment for Procurement Specialists to work on purchase requisitions, sourcing requests, negotiations, procurement requests, and more.


