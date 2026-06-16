---
title: Quote Management Data Model release notes
description: Version history for the Quote Management Data Model on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-quote-mgmt-data-model.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management release notes, ServiceNow Store release notes]
---

# Quote Management Data Model release notes

Version history for the Quote Management Data Model on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 12.0.2 - June 2026 \(Australia\)**
    -   Integration Guided Setup
    -   Quote AI Agent
    -   Configuration AI Agent A2A
    -   Renewal pricing for ramped quote lines
    -   Context rules: rules engine enhancements
    -   Dynamic BOM rules authoring enhancements
    -   Translations for CPQ Admin
    -   AI context upload for CPQ Admin
    -   AI context upload for sales persona
-   **Version 11.0.2 - June 2026 \(Zurich\)**
    -   Integration Guided Setup
    -   Quote AI Agent
    -   Configuration AI Agent A2A
    -   Renewal pricing for ramped quote lines
    -   Context rules: rules engine enhancements
    -   Dynamic BOM rules authoring enhancements
    -   Translations for CPQ Admin
    -   AI context upload for CPQ Admin
    -   AI context upload for sales persona
-   **Version 10.3.0 - May 2026**
    -   Fixed:
        -   When creating a quote with ramps applied to child lines only, quote header rollup fields were not updating to reflect the ramped values. Header rollups now correctly aggregate values from ramped child lines.
        -   The Clear Ramps action was not fully resetting the primary ramp designation or ramp sequence on affected lines. Both fields are now properly cleared when the action is invoked.
        -   During child upsell and downsell sync in consolidation scenarios, quantities were being double counted across all lines. The sync logic has been corrected to ensure quantities are counted once per line.
        -   For quotes containing approximately 1,000 lines, the business rule responsible for setting quote line state to match quote state was causing save operations to take up to 90 seconds. The business rule has been optimized to significantly reduce save time on large quotes.
-   **Version 10.1.3 - April 2026**
    -   Ability to modify ramp segments during the amendment process
    -   Ability to support zeroing out quantities during amendments or renewals
    -   Validation to ensure peak quantity for ramped products aligns with configured quantities
-   **Version 10.0.0 - March 2026**
    -   Delta Pricing on Quote
        -   Supports pricing and quantity calculations during MACD activities and renewals by deriving changes from existing products, contracts, or purchases.
    -   Contract Consolidation on Quotes
        -   Ensures that orders created from consolidated quotes retain traceability to all originating contract lines, maintaining accurate relationships between source and consolidated lines. Additional calculated fields on order lines support visibility into uplift values derived from consolidation rules.
    -   Enhancements to price and quantity ramps on quote line items
        -   Enable agents to create and manage custom ramp structures with flexible segment durations. These enhancements support ramp changes across the quote lifecycle, including amendments and renewals, while ensuring pricing and quantity consistency across ramp segments.
    -   Quote Approvals
        -   Supports end‑to‑end visibility and control of quote approvals by allowing sales reps, approvers, and managers to track approval status, steps, sequencing, approvers, comments, and timestamps in real time. The approval lifecycle automatically manages quote states and edit permissions as quotes move through Draft, In Review, Approved, and Rejected states.
-   **Version 9.0.3 - January 2026**

    Fixed minor defects.

-   **Version 9.0.0 - December 2025**

    New: Support to create price and quantity ramps for product offerings in quotes to define incremental price and quantity changes over time. Product offerings eligible for ramps have theRamps enabled option and Recurring price method selected.

-   **Version 7.1.0 - August 2025**
    -   New:
        -   Quote header discounts: Support percentage-based discount​s on the quote header​
        -   Quote margins​: Display aggregated margin calculations for one-time, monthly and total amounts for the quote
-   **Version 6.0.0 - May 2025**
    -   New:
        -   Enable the use of sales agreements to create new customer quotes, applying the agreed prices and offerings from the agreement.
        -   Provide visibility to order agents for the price adjustments that were applied to the base price and list price of the product on quotes.
    -   Change: Deprecate subscription dates and using contract dates to calculate subscription revenue metrics on quotes.
-   **Version 5.0.0 - February 2025**
    -   New:
        -   Generate PDF documents from a quote using a pre-set template and send the document for signatures via DocuSign integration.
        -   View the parent and child relationships between quote lines within a quote with the hierarchical list.
        -   View offer recommendations to upsell or cross-sell products that complement products in quotes.
-   **Version 4.0.2 - November 2024**
    -   New:
        -   Location-based quoting with eligibility check support
        -   Multi-line copy with option to set an alternate service location
        -   Adding covered product support on quote to display products covered by contracts or entitlements on the quote lines ​​
        -   Create sales agreements for configurable and bundled products and services​
        -   Create a quote for modification or renewal of contracts​
-   **Version 3.0.1 - August 2024**

    Change: Included Quote tasks table on quote: Create multiple tasks for a quote and assign them to the target group. These tasks serve as references for the agents to perform the necessary actions needed to generate a successful quote.

-   **Version 2.0.1 - May 2024**

    Changed: Cost book addition, quote action addition and performance improvements.

-   **Version 1.0.1 - February 2024**

    The Quote Management Data Model application provides access to the tables that will store all the quote-related data. The tables include Quote, Quote Line Item, Quote Line Characteristics, and Quote Pricing Adjustment. When you create a quote, the data related to quote will be stored in these tables.


