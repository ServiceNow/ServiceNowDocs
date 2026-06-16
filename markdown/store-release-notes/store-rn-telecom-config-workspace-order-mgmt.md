---
title: Configurable Workspace for Order Management release notes
description: Version history for the Configurable Workspace for Order Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-config-workspace-order-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Configurable Workspace for Order Management release notes

Version history for the Configurable Workspace for Order Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 15.2.1 - June 2026 \(Australia\)**

    New: Support order header and top order line tasks to track and coordinate activities throughout the order life cycle.

-   **Version 15.2.0 - June 2026 \(Zurich\)**

    New: Support order header and top order line tasks to track and coordinate activities throughout the order life cycle.

-   **Version 15.1.0 - May 2026**

    New: Enables involved parties creation on order and order lines with distinct roles such as Bill-To, Ship-To, Partner, Reseller and supports complex relationships across direct and indirect deal types and routes to market.

-   **Version 15.0.0 - March 2026 \(Zurich\)**
    -   New:
        -   Delta Pricing on Order:Supports pricing and quantity calculations during MACD activities and renewals by deriving changes from existing products, contracts, or purchases.
        -   Contract Consolidation on Order: Ensures that orders created from consolidated quotes retain traceability to all originating contract lines, maintaining accurate relationships between source and consolidated lines. Additional calculated fields on order lines support visibility into uplift values derived from consolidation rules.
        -   Enhancements to price and quantity ramps on order line items: Enable agents to create and manage custom ramp structures with flexible segment durations. These enhancements support ramp changes across the order lifecycle, including amendments and renewals, while ensuring pricing and quantity consistency across ramp segment
        -   Catalog driven task plan template: Provide customers with the option to configure product workflows using catalog-driven task plan templates to define tasks and their dependencies required to orchestrate the product fulfillment journey. This standardizes fulfillment processes across products and serves as an alternative to Flow Designer, offering greater flexibility in implementing product configurations.
        -   Enhance the Order management \(OM\) integration with Strategic Portfolio Management \(SPM\) for in-flight orders to support projects for site and maintain program project and sub-project hierarchy.
-   **Version 14.1.2 - January 2026 \(Yokohama\)**

    New: Support move orders via the API, handling product cessation at the existing location and provisioning at the new location.

-   **Version 14.1.0 - December 2025 \(Zurich\)**
    -   New:
        -   Enables order agents to quickly view, add, and edit manual price adjustments for order line items directly from the list view, making it easier to view both automatic and manual adjustments from the list view.
        -   Support to create price and quantity ramps for product offerings in orders to define incremental price and quantity changes over time. Product offerings eligible for ramps have theRamps enabled option and Recurring price method selected.
        -   Summarization for Order Management: Summarizes complex orders across products, services, and fulfillment tasks, enabling agents to quickly understand status, take the right actions, and avoid navigating fragmented views to make next steps easier and improving productivity.
-   **Version 12.0.0 - August 2025**
    -   New:
        -   Support for nested objects, arrays, and custom attributes to model complex products.
        -   Support for header discounts on the order.
-   **Version 11.2.2 - July 2025**
    -   New:
        -   Provide visibility to order agents for the price adjustments that were applied to the base price and list price of the product ordered.
        -   Use the hierarchical list view to see the parent and child relationships between order lines within an order
    -   Change: Deprecate subscription dates and using contract dates to calculate subscription revenue metrics on orders.
-   **Version 11.2.0 - May 2025**
    -   New:
        -   Provide visibility to order agents for the price adjustments that were applied to the base price and list price of the product ordered.
        -   Use the hierarchical list view to see the parent and child relationships between order lines within an order.
    -   Change: Deprecate subscription dates and using contract dates to calculate subscription revenue metrics on orders.
-   **Version 10.2.0 - February 2025**

    New: Subscription Revenue Metrics ​on order: calculate and display key revenue metrics on orders.

-   **Version 10.0.0 - November 2024**

    New: Location-based ordering​, defaulting sales agreement on order, Case Management for Order Operations​, support jeopardy management for business hours when scheduling tasks.

-   **Version 9.0.1 - August 2024**

    Bug fixes.

-   **Version 8.0.2 - June 2024**

    Changed: Bug fixes and other improvements.

-   **Version 8.0.1 - May 2024**
    -   Changed: Added Contract start and end date on the order creation form view and order details page
    -   Other bug fixes
-   **Version 7.0.0 - February 2024**
    -   New:
        -   Change order capture experience and support order enrichment process in the workspace
        -   Order timeline view to show all tasks and domain orders with risk profile on a single UI
    -   Changed:
        -   Support old order capture using system property
        -   Order Record Page UI Changes
        -   Replacing Breakdown-grid with DataGrid
    -   Removed:
        -   Telco List is deprecated
        -   Telco simple list is deprecated
-   **Version 6.0.2 - January 2024**

    Security fixes.

-   **Version 6.0.0 - November 2023**
    -   New:
        -   Updated view for the order, order line, and order line characteristics.
        -   Add New button and Navigation menu access to persona roles.
-   **Version 5.0.0 - August 2023**
    -   New:
        -   Support network slicing for 5G service \(Connected Navigation\)
        -   TMF641 Service Order Spoke \(Southbound Actions\)
        -   Jeopardy Management
        -   Integrate Order Management and Strategic Portfolio Management
        -   Integrate Order Management with Field Service Management
        -   Support External Inventory ID in order
        -   Telemetry - create KPIs for Order Management KPIs
        -   Support suspend and restore action for product and service orders
        -   Capture, benchmark, and assess large amount of Order Management performance during E2E SLA processing of jeopardy events
        -   Cancel child domain orders when parent domain order is cancelled manually
    -   Fixed:
        -   Validation for the change orders with Add/Disconnect order line combinations at approval time
        -   Support version tracking on domain order
-   **Version 4.0.0 - February 2023**

    Changed: Order capture UI updated to include related items in the new order.

-   **Version 3.0.3 - November 2022**

    Changed: Internal optimization to align to NOW engineering standards

-   **Version 3.0.1 - August 2022**
    -   New:
        -   Change and disconnect product order
        -   Change and disconnect service order
    -   Changed: New UI builder page for order capture
-   **Version 2.0.1 - June 2022**

    Changed: Updated to account for address relationship change by horizontal OM team

-   **Version 2.0.0 - February 2022**

    Changed: Provides a more complete order capture capability expanding beyond the capture of new customer or service order in v1 and adds support for capturing multi-site, multi-unique product configurations,support for quantity and the ability to copy the configuration of one product at one site to one or more additional sites.

-   **Version 1.0.1 - October 2021**

    New: Net new feature for Order Management for Telecommunications &amp; Media


