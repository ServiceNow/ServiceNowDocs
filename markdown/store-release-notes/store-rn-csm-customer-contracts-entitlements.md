---
title: Customer Contracts and Entitlements release notes
description: Version history for the Customer Contracts and Entitlements application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-customer-contracts-entitlements.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Customer Service Management version history release notes, ServiceNow Store version history release notes]
---

# Customer Contracts and Entitlements release notes

Version history for the Customer Contracts and Entitlements application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 15.0.1 - September 2026**

    Fixed minor defects.

-   **Version 14.3.3 - August 2026**

    Fixed: Duplicate contract lines are not created after an order revision. The system now prevents duplicate contract line items when a revised order line item is approved, ensuring accurate contract records and entitlements. Null checks have been added and unit test failures have been resolved.

-   **Version 14.3.0 - June 2026**

    ACL related fixes

-   **Version 14.2.0 - May 2026**

    Minor Defect Fixes

-   **Version 14.1.0 - April 2026**

    Change: Hierarchical display for Customer Contract Lines for better experience while using the contracts and initiating different actions.

-   **Version 14.0.0 - March 2026**
    -   New:
        -   View ramp details for contract lines that are a part of a quantity or price ramp deal.
        -   View the contributing contract lines to derived price products in contract line price adjustments.
        -   View consolidation history on contract lines and contracts.
-   **Version 13.1.0 - February 2026**

    New: Defect fixes to read only fields in tables.

-   **Version 13.0.0 - December 2025 \(Yokohama, Zurich\)**
    -   New:
        -   Enhancements for enabling calculation of delta amount on quote and line traceability, during contract line upsells and downsells.
        -   Capture contract lines for deals with price and quantity ramps and view ramp details from contract lines.
        -   Introduced granular admin roles on customer contracts for enhanced security.
-   **Version 11.0.0 - August 2025 \(Yokohama, Zurich\)**

    New: Data model improvements to support advanced lifecycle change management workflows.

-   **Version 10.0.0 - August 2025 \(Xanadu\)**

    New: Data model improvements to support advanced lifecycle change management workflows.

-   **Version 9.0.0 - May 2025 \(Yokohama\)**

    New: Added new fields to capture renewal pricing information.

-   **Version 8.0.0 - May 2025 \(Xanadu, Washington DC\)**

    New: Added new fields to capture renewal pricing information.

-   **Version 7.0.0 - February 2025**
    -   New:
        -   Added subscription pricing and location information on contract lines and entitlements
        -   Added a new workspace view for service contracts and entitlements in Customer Service Management workspace
-   **Version 4.0.0 - November 2024**

    New: Minor updates including support for product specification on contract lines.

-   **Version 3.0.0 - August 2024**

    New: Includes minor updates to support covered products related workflows.

-   **Version 2.0.2 - May 2024**
    -   New:
        -   Ability to create parent-child relationship in service contract lines
        -   Corresponding updates to APIs
-   **Version 1.0.1 - February 2024**

    Customer Contracts and Entitlements application provides data model to store contracts, contract lines, and entitlements. Contracts from external systems can be imported using specifically designed APIs.


**Parent Topic:**[ServiceNow Store - Customer Service Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-csm.md)

