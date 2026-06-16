---
title: Order Management release notes
description: Version history for the Order Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-order-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Telecommunications Service Management release notes, ServiceNow Store release notes]
---

# Order Management release notes

Version history for the Order Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 18.0.1 - June 2026 \(Australia\)**

    New: Support order header and top order line tasks to track and coordinate activities throughout the order life cycle.

-   **Version 17.0.2 - June 2026 \(Zurich\)**

    New: Support order header and top order line tasks to track and coordinate activities throughout the order life cycle.

-   **Version 16.7.0 - May 2026**

    New: Enables involved parties creation on order and order lines with distinct roles such as Bill-To, Ship-To, Partner, Reseller and supports complex relationships across direct and indirect deal types and routes to market.

-   **Version 16.5.2 - April 2026 \(Yokohama\)**
    -   Enhancement to derived pricing in Order Management: Surface an informational message whenever pricing for a derived pricing product offer is updated on transaction lines.
    -   Support for zero quantity on order lines: Enable a quantity value of 0 for an order line item during order amendment or renewal processes.
-   **Version 16.3.0 - March 2026 \(Zurich\)**
    -   New:
        -   Delta Pricing on Order:Supports pricing and quantity calculations during MACD activities and renewals by deriving changes from existing products, contracts, or purchases.
        -   Contract Consolidation on Order: Ensures that orders created from consolidated quotes retain traceability to all originating contract lines, maintaining accurate relationships between source and consolidated lines. Additional calculated fields on order lines support visibility into uplift values derived from consolidation rules.
        -   Enhancements to price and quantity ramps on order line items: Enable agents to create and manage custom ramp structures with flexible segment durations. These enhancements support ramp changes across the order lifecycle, including amendments and renewals, while ensuring pricing and quantity consistency across ramp segment
        -   Catalog driven task plan template: Provide customers with the option to configure product workflows using catalog-driven task plan templates to define tasks and their dependencies required to orchestrate the product fulfillment journey. This standardizes fulfillment processes across products and serves as an alternative to Flow Designer, offering greater flexibility in implementing product configurations.
        -   Enhance the Order management \(OM\) integration with Strategic Portfolio Management \(SPM\) for in-flight orders to support projects for site and maintain program project and sub-project hierarchy.
-   **Version 15.4.0 - January 2026 \(Yokohama\)**

    New: Support move orders via the API, handling product cessation at the existing location and provisioning at the new location.

-   **Version 15.3.0 - December 2025**
    -   New:
        -   Enables order agents to quickly view, add, and edit manual price adjustments for order line items directly from the list view, making it easier to view both automatic and manual adjustments from the list view.
        -   Support to create price and quantity ramps for product offerings in orders to define incremental price and quantity changes over time. Product offerings eligible for ramps have theRamps enabled option and Recurring price method selected.
        -   Summarization for Order Management: Summarizes complex orders across products, services, and fulfillment tasks, enabling agents to quickly understand status, take the right actions, and avoid navigating fragmented views to make next steps easier and improving productivity.
-   **Version 9.0.2 - September 2024**
    -   Fixed the issue that caused long upgrade time
    -   Fixed the issue for characteristics not shown on the stepper UI when creating order lines
-   **Version 8.0.2 - May 2024**

    Changed: Adding the capability to update product inventory when product spec is updated and a new version rolled out through API.

-   **Version 7.0.0 - February 2024**
    -   New:
        -   Order enrichment process
        -   Price management
        -   Consumer order support
    -   Changed: Demo data changes
    -   Fixed: Localization related issue fixes
-   **Version 6.0.3 - January 2024**

    Security fixes.

-   **Version 6.0.1 - November 2023**
    -   New:
        -   Move telco-specific API code and demo data to new telecommunications application \(sn\_om\_tmt\).
        -   Data model changes to handle commitment term deprecation.
        -   Remove periodicity from pricing adjustments table.
        -   Build demo enrichment workflow for SD-WAN product.
    -   Fixed:
        -   Fix issue with missing order line reprice UI action.
        -   Clean up business ruless and client scripts pertaining to commitment term &amp; pricing method deprecation.
        -   Fix issue with mandatory characteristics not being populated while creating service order via workspace.
        -   For change orders, resolve the issue where all child inventories were not being populated for bundles and composed of scenarios.
        -   Fix priority choice type field on order line item.
        -   Allow multi-level bundles in Add order UI.
        -   Validate deletion of bundle child line item.
        -   Restrict order line item revision while decomposition is in progress.
        -   Fix order remaining in acknowledged state after approval.
        -   Fix UI policy to prevent Account, primary contact, and consumer fields showing together.
-   **Version 6.0.1 - November 2023**

    Order Management is a dynamic catalog-based system that captures, improves, and oversees the complete lifecycle of product and service orders. It efficiently handles order orchestration, data enrichment, and decomposition to ensure accurate and timely fulfillment.


**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

