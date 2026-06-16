---
title: Spend and Savings Management release notes
description: Version history for the Spend and Savings Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-spend-savings-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Spend and Savings Management release notes

Version history for the Spend and Savings Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.0.2 - June 2026 \(Australia\)**
    -   New:
        -   AI‑powered Savings Opportunity Discovery:
            -   Spend and Savings Management introduces an AI‑powered Savings Opportunity Discovery workflow that helps sourcing and category managers identify potential savings across contracts, spend, and supplier data.
        -   Agentic opportunity discovery:
            -   The Savings Opportunity Discovery workflow can be enabled through the Now Assist admin experience. Once enabled, specialized AI agents analyze organizational data and generate actionable savings opportunities.
        -   Savings opportunity identification: The solution identifies opportunities across key savings levers, including:
            -   Contract optimization: Price escalation, renewal caps, and payment terms optimization
            -   Spend optimization: Off‑contract spend opportunities
            -   Supplier optimization: Non‑preferred supplier spend, unconsolidated supplier spend, and spend fragmentation
            -   Discovered opportunities are automatically created and stored as structured records in the Savings Opportunities table.
        -   Savings Opportunities data model:
            -   A new Savings Opportunities \(sn\_spend\_gen\_ai\_savings\_opportunities\) table stores AI‑generated opportunities and supports review, investigation, and action workflows.
        -   Opportunity review and investigation:
            -   You can review opportunities and select Learn More to open the Now Assist panel for detailed explanations and follow‑up questions.
        -   Take action on opportunities: You can do the following:
            -   Create pipeline projects directly from opportunities
            -   Capture AI‑generated summaries in project work notes
            -   Dismiss opportunities with an optional reason
    -   Changed:
        -   Remediated non‑Glide Cobalt Raven ACLs in product code \(DIRS0000421\).
-   **Version 2.4.3 - June 2026**
    -   New:
        -   AI‑powered Savings Opportunity Discovery:
            -   Spend and Savings Management introduces an AI‑powered Savings Opportunity Discovery workflow that helps sourcing and category managers identify potential savings across contracts, spend, and supplier data.
        -   Agentic opportunity discovery:
            -   The Savings Opportunity Discovery workflow can be enabled through the Now Assist admin experience. Once enabled, specialized AI agents analyze organizational data and generate actionable savings opportunities.
        -   Savings opportunity identification: The solution identifies opportunities across key savings levers, including:
            -   Contract optimization: Price escalation, renewal caps, and payment terms optimization
            -   Spend optimization: Off‑contract spend opportunities
            -   Supplier optimization: Non‑preferred supplier spend, unconsolidated supplier spend, and spend fragmentation
            -   Discovered opportunities are automatically created and stored as structured records in the Savings Opportunities table.
        -   Savings Opportunities data model:
            -   A new Savings Opportunities \(sn\_spend\_gen\_ai\_savings\_opportunities\) table stores AI‑generated opportunities and supports review, investigation, and action workflows.
        -   Opportunity review and investigation:
            -   You can review opportunities and select Learn More to open the Now Assist panel for detailed explanations and follow‑up questions.
        -   Take action on opportunities: You can do the following:
            -   Create pipeline projects directly from opportunities
            -   Capture AI‑generated summaries in project work notes
            -   Dismiss opportunities with an optional reason
-   **Version 2.4.0 - March 2026**

    Changed: Propagates the spend category from the PO line to the invoice line, ensuring consistent spend category data and preventing under‑reported spend in analytics for externally created invoices.

-   **Version 2.0.1 - December 2025**
    -   New:
        -   A new Category analytics module is available in the Source-to-Pay workspace. Selecting this module loads the Savings dashboard, powered entirely by pipeline project data. This dashboard helps users analyze category performance, track potential and realized savings, and monitor project progress from opportunity identification to savings realization. Users with the sn\_spend\_mgmt.sourcing\_category\_manager role can view and access the Savings dashboard in the Category Analytics module.
        -   A new Category management tab has been added within the Source-to-Pay workspace. This tab includes the following components:
            -   Workspace-level global filters
            -   Overview section
            -   Action-focused insight tabs
            -   Pipeline project creation from insights across all three sub-tabs
            -   Supplier record enhancements
-   **Version 1.0.5 - August 2025**

    Minor fixes.

-   **Version 1.0.1 - May 2025**

    Spend and Savings Management enables organizations to strategically segment and manage procurement categories to optimize sourcing and ultimately drive hard dollar savings.


**Parent Topic:**[ServiceNow Store - Sourcing and Procurement Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-psm-procurement-service-mgmt-landing.md)

