---
title: Quote Management Application release notes
description: Version history for the Quote Management Application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-quote-mgmt-app.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management release notes, ServiceNow Store release notes]
---

# Quote Management Application release notes

Version history for the Quote Management Application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.0 - June 2026 \(Australia\)**
    -   Integration Guided Setup
    -   Quote AI Agent
    -   Configuration AI Agent A2A
    -   Renewal pricing for ramped quote lines
    -   Context rules: rules engine enhancements
    -   Dynamic BOM rules authoring enhancements
    -   Translations for CPQ Admin
    -   AI context upload for CPQ Admin
    -   AI context upload for sales persona
-   **Version 10.4.1 - June 2026 \(Zurich\)**
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
    -   This release resolves the following quote defects:
        -   When creating a new contact from the Contacts tab on a quote, the Account field was incorrectly disabled, preventing users from selecting an account. The field is now editable and defaults to the account associated with the quote. Additionally, contact search results now correctly include contacts from the account and its full account hierarchy.
        -   When amending a contract by modifying all lines and increasing the quantity of a child line with an effective date via the Config UI, the resulting split line incorrectly updated the end date of the original no-change line. Since the original line represents an upsell quantity scenario with no-change, its dates should remain unaffected. This has been corrected.
        -   The Line Type for Ramps Cross Sell lines was incorrectly displaying as "Upsell + New" instead of "Upsell." This has been resolved to reflect the correct line type.
        -   When upselling ramp lines, the Line Type was incorrectly defaulting to "Amend" on the resulting quote lines. This has been corrected so that ramp upsell lines default to the appropriate line type.
-   **Version 10.1.0 - April 2026**
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
-   **Version 9.1.3 - January 2026**

    Fixed minor defects.

-   **Version 9.1.0 - December 2025**
    -   New:
        -   Enables sales agents to quickly view, add, and edit manual price adjustments for quote line items directly from the list view, making it easier to view both automatic and manual adjustments from the list view.
        -   Create price and quantity ramps for product offerings in quotes to define incremental price and quantity changes over time. Product offerings eligible for ramps have theRamps enabled option and Recurring price method selected.
-   **Version 7.0.0 - August 2025**
    -   New:
        -   Quote Header Discounts: Support percentage-based discount​s on the quote header​
        -   Quote Margins: Display aggregated margin calculations for one-time, monthly and total amounts for the quote
-   **Version 6.0.1 - August 2025**

    Fixed issue with the "New" button opening the interceptor on the Quote list bundle page.

-   **Version 6.0.0 - May 2025**
    -   New:
        -   Enable the use of sales agreements to create new customer quotes, applying the agreed prices and offerings from the agreement.
        -   Provide visibility to order agents for the price adjustments that were applied to the base price and list price of the product on quotes.
    -   Change: Deprecate subscription dates and using contract dates to calculate subscription revenue metrics on quotes.
-   **Version 5.0.0 - February 2025**
    -   New:
        -   Enable agents to create PDF documents from a quote using the ServiceNow PDF generator.
        -   Use the hierarchical list view to see the parent and child relationships between quote lines within a quote.
        -   Provide agents with offer recommendations to upsell or cross-sell products that complement products in quotes.
-   **Version 4.0.0 - November 2024**
    -   New:
        -   Location-based quoting with eligibility check support
        -   Multi-line copy with option to set an alternate service location
        -   Adding covered product support on quote to display products covered by contracts or entitlements on the quote lines ​​
        -   Create sales agreements for configurable and bundled products and services​
        -   Create a quote for modification or renewal of contracts​
-   **Version 3.0.0 - August 2024**
    -   New:
    -   1.  Single-click creation of sales agreements from a quote: Create sales agreements from quotes to capture the scope and conditions for future sales transactions between a buyer and a seller. A sales agreement contains information such as details about the buyer and seller, validity period of the agreement, and quantities and pricing of the products and services.
2.  Quote tasks: Create multiple tasks for a quote and assign them to the target group. These tasks serve as references for the agents to perform the necessary actions needed to generate a successful quote.
3.  Order creation from quote line items: Create orders by selecting multiple line items within a quote.
-   **Version 2.0.1 - May 2024**

    Changed: Cost book addition, quote action addition and performance improvements.

-   **Version 1.0.0 - February 2024**

    The Quote Management application enables the users to create and track quotes during the sales cycle. The application is integrated with product catalog, pricing, and product configurator to facilitate capturing of product and services that the customer is interested in, with the ability to customize the offering and perform dynamic pricing.


