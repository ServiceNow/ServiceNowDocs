---
title: Pricing Matrix Management release notes
description: Version history for the Pricing Matrix Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-pricing-matrix-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management release notes, ServiceNow Store release notes]
---

# Pricing Matrix Management release notes

Version history for the Pricing Matrix Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.3.0 - June 2026**
    -   Fixed:
        -   Performance enhancements
        -   Security fixes
-   **Version 10.2.0 - May 2026**
    -   New:
        -   External ID field added to Context Variable, CostBook, and CostBook Line tables, read-only after initial save.
        -   Rule matrices now automatically reflect new matrix type field choices without manual reconfiguration.
    -   Fixed:
        -   Rule matrix versioning hangs or fails on large decision tables.
        -   Matrix type field not enforced as mandatory during rule matrix creation.
        -   Discounts silently skipped when product offering and product offering family context variables used together.
        -   Performance: Deprecated generateNewCode\(\)replaced in context rule management plugin.
        -   Performance: Pricing engine log slow to open with large number of sys log records.
-   **Version 10.1.0 - April 2026**
    -   Fixed:
        1.  Issue with published matrix not updating on published pricing plan.
        2.  Issue with manual Pricing adjustments are not returned when pricing is called during MACD add.
-   **Version 10.0.0 - March 2026**
    -   New:
        -   Added Price Increase Defaulting Matrix for Ramp API &amp; Renewal API
        -   Validation added for "Derived Pricing Matrix" rules
-   **Version 9.1.0 - January 2026**
    -   Fixed:
        -   Apply List Price or Base Price based on pricing plan price point.
        -   Incorrect pricing adjustments where multiplelist price adjustments are created with the same values.
-   **Version 9.0.0 - December 2025**

    New: Support for granular admin roles.

-   **Version 2.0.1 - May 2024**

    New: Performance improvements made in adjustment calculations. Display of adjustments in the configuration UI. Support for characteristics based adjustments in standard pricing adjustment matrix.

-   **Version 1.0.0 - February 2024**

    Pricing matrix is a structured framework based on decision tables that specify how list prices are adjusted for products or services based on multiple criteria or attributes. These criteria can include factors such as quantity, customer types, regions, or any other relevant dimensions. These dimensions can be defined using context variables. Pricing matrix can be extended to other simple pricing rules.


**Parent Topic:**[ServiceNow Store - Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-sales-order-management-highlights.md)

