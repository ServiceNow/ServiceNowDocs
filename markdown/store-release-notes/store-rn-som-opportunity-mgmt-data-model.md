---
title: Opportunity Management Data Model release notes
description: Version history for the Opportunity Management Data Model application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-opportunity-mgmt-data-model.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management release notes, ServiceNow Store release notes]
---

# Opportunity Management Data Model release notes

Version history for the Opportunity Management Data Model application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.1.0 - June 2026 \(Australia\)**

    Changed: This release includes fixes for known issues to improve stability and reliability. No new features or enhancements have been introduced.

-   **Version 11.0.0 - June 2026 \(Zurich\)**

    Changed: This release includes fixes for known issues to improve stability and reliability. No new features or enhancements have been introduced.

-   **Version 10.0.7 - May 2026**

    Fixed: Minor enhancements and security fixes.

-   **Version 10.0.2 - April 2026**
    -   This release includes:
        -   Addition of new tables for supporting Opportunity Allocations and its related setup.
            -   Opportunity Allocation Type
            -   Opportunity Allocation Dimension
            -   Opportunity Allocation
        -   Introduced new fields on Opportunity to capture direct or indirect deal types to align opportunities with defined routes to market.
            -   Deal type
            -   Route to market
-   **Version 9.0.1 - March 2026**
    -   This release includes:
        -   Enhancements on Opportunity to effectively capture the primary reasons for winning or losing a given opportunity.
        -   Track Opportunity Competitors across various product offerings or product families. Additionally, keep a track of incumbent competitors, and any new or emerging entrants in the market.
        -   Gain insight into customer interactions by monitoring Opportunity Tasks in relation to CRM Touchpoints.
        -   When Opportunities are merged as part of account or contract consolidation into a single target opportunity for execution and reporting, track the Consolidated opportunity and Top consolidated Opportunity on the Opportunity and Opportunity Line.
-   **Version 8.0.2 - January 2026**

    Fixed: Resolved currency-related issues in Opportunity Pricing. Previously, the amount fields in opportunities displayed values in the default currency \(USD\) instead of reflecting the specific opportunity currency and the correct prices were not derived from the price list for the product offerings.

-   **Version 8.0.1 - December 2025**
    -   This release includes:
        -   Addition of two new tables: Opportunity Team Member and Opportunity Associated Contacts. These tables will facilitate tracking of sales team and customer contacts involved in the opportunity.
        -   Optimising opportunity for Sales Territory Management
        -   New fields on opportunity and its line items to facilitate the calculation of delta amounts relevant to contract upsells and downsells. These fields include Total Net New Amount, Total Renewal Amount, Total Upsell/Downsell Amount, Contract Start Date, and Contract End Date.
        -   Minor security fixes
-   **Version 6.1.0 - August 2025**
    -   New changes in this release:
        -   Introduced 'Short Description' field for opportunity line item.
        -   Minor security fixes
-   **Version 6.0.1 - June 2025**

    We are shipping Cobalt Raven fixes with this new version as part of the Opportunity Data Model.

-   **Version 6.0.0 - May 2025**
    -   New changes in this release:
        -   This release introduces new fields on Opportunity Line Item to support parent-child hierarchy created by the product configurator. New pricing related fields like ARR, MRR, and One-Time Price tracks the pricing of parent and child item lines.
        -   The table Opportunity Line Characteristic table tracks the product characteristics for each opportunity line item.
-   **Version 5.0.0 - February 2025**

    Provide support for clear distinction of closed opportunity stages by introducing type closed won and closed lost.

-   **Version 4.0.0 - November 2024**
    -   New:
        -   Along with the existing features on opportunity, we have included the following features this time:
            -   Subscription revenue metrics: Enabling sales agents or managers to use and view calculated metrics like ARR, MRR, ACV, TCV , Amount &amp; Weighted Amount that enable better pipeline inspection and revenue reporting, and also improved understanding of recurring revenue dynamics.
            -   Sync quote to opportunity: Enable sales agents or managers to keep the opportunity revenue up-to-date with the quote through its various stages and revisions for accurate revenue reporting at any given point in time.
            -   Location-based opportunity:Enable sales agents to filter the product catalog based on customer's service location and capture opportunities and opportunity line items across their different service locations.
-   **Version 3.0.0 - August 2024**
    -   Changed:
        -   Along with the existing features on opportunity, we have included the following features this time:
            -   Multi-select opportunity line and create quotes for them: Allowing sales agents or managers to create multiple quotes for specific line items through the 'Create New Quote' UI action available in the line items related list.
            -   Sidebar chat integration with Teams on opportunity : Facilitating collaboration among sales agents and subject matter experts within the context of an opportunity by integrating the Sidebar with Teams platform capability in Opportunity Management.
                -   Sidebar chat integration with Teams on Opportunity will require minimum platform version as Xanadu
-   **Version 2.0.2 - May 2024**

    Changed: Included pricing-related fields within Opportunity Header and Line items. Facilitated pricing requests from Opportunity to the pricing engine for retrieving prices of offerings listed in the price lists.

-   **Version 1.0.0 - February 2024**

    The Opportunity Management Data Model application gives access to the opportunity tables that allow organizations to store any opportunity-related data.


