---
title: Product and pricing rules release notes
description: Version history for the Product and pricing rules application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-product-pricing-rules.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Product and pricing rules release notes

Version history for the Product and pricing rules application on the ServiceNow Store.

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

-   **Version 7.0.0 - August 2025**

    New: Support for product attribute-based costing.

-   **Version 6.0.0 - May 2025**

    Fixed: Few minor bug fixes.

-   **Version 5.0.0 - February 2025**
    -   New: Performance improvement of pricing calls
    -   Fixed:
        -   How sequence is derived for Price Adjustments from Pricing Plan
        -   The price override adjustment calculation
-   **Version 4.0.2 - January 2025**
    -   Changed:
        -   When adjustments records are created for price override, the pricing engine will always consider the rolling list price as the base price for adjustment calculations.
        -   Sequencing of adjustments within a pricing plan step and across pricing plan steps will be followed strictly per the pricing plan sequence and matrix priority, with no exceptions to price overrides.
-   **Version 4.0.0 - November 2024**
    1.  Pricing Plan implementation
    2.  Service location context variables are added to matrix inputs.
    3.  Supported context types value changed to transaction header and transaction line in matrix type records, for Eligibility rules.
    4.  Eligibility rules to support line level variables like shipping location.
    5.  SA linked order to support location based eligibility
-   **Version 3.0.1 - August 2024**

    Product and pricing rules is a structured framework based on decision tables to define business rules related to pricing and product. They include rules such as price adjustments rules and product offer eligibility rules. The rules are defined based on multiple criteria or attributes. These criteria can include dimensions such as sales channel, customer types, regions, and so on. These dimensions can be defined using context variables.


**Parent Topic:**[ServiceNow Store - Technology Provider Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-tech-highlights.md)

