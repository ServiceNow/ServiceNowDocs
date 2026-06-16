---
title: Order Management for Telecom, Media &amp; Tech release notes
description: Version history for the Telecommunications Service Management Order Management for Telecom, Media &amp; Tech application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-telecom-order-mgmt-for-telecom.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Technology Provider Service Management release notes, ServiceNow Store release notes]
---

# Order Management for Telecom, Media &amp; Tech release notes

Version history for the Telecommunications Service Management Order Management for Telecom, Media &amp; Tech application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.1.0 - June 2026**
    -   Changed:
        -   TMF 637 -  Fixed the Product Inventory Response Structure
        -   TMF 622 -  Fixed to Return Display Value Instead of Internal Value for Order Item Characteristic
-   **Version 14.0.0 - March 2026**
    -   New: Task Template driven Workflow - This feature allow the Business users an alternate to defining a workflow which was earlier defined using Flow Designer. This alternate approach of using Task plan templates will allow Business users with Limited Servicenow knowledge to use the Task Template based journey to define the workflows for a Product/Service Fulfilment.
    -   Changed: Improve OM to SPM Integration -  This feature was enhanced to support Site Project re-use for Inflight orders as well as handling the OM-SPM integration for Order Cancellation.
-   **Version 13.3.0 - January 2026**
    -   New:
        -   Support for Move orders  :Handle any move order which needs
            -   Location change
            -   Location change + change of attribute values
            -   Location change + add/delete of product
    -   Changed:
        -   SOM-SPM Integration : Below changes have been made to the SOM-SPM Integration
            -   Allow creation of Site Project at the Site level for Orders
            -   Enhanced the Project creation for Products to create a hierarchy between Program-&gt;Site Project-&gt;Project
-   **Version - December 2025**

    Includes changes to TMF catalog APIs \(TMF 620,TMF633\), Order API \( TMF 622, TMF641\) and Product Inventory API \( TMF 637\) which are detailed below:

    1.  TMF 620/633: Catalog Management- Enhanced the existing operations \(GET, LIST, DELETE and PATCH\) to support sending correct version
    2.  TMF 622/641: Order Management - Enhanced the existing POST and PATCH operations to support referencing the correct version
    3.  TMF 637: Product Inventory Management - Support PATCH and DELETE operations for Product Inventory
    4.  TMF 648: Quote Management - Enhance POST, GET, PATCH and DELETE operations to support Quote with complex characteristics and associate the correct version
-   **Version 12.2.0 - August 2025**

    Changed: includes changes to TMF catalog APIs \(TMF 620,TMF633\), Order API \( TMF 622, TMF641\) and Product Inventory API \( TMF 637\) to include support of Complex Characteristics for GET, LIST, POST, PATCH operations.

-   **Version 12.0.1 - August 2025 \(Xanadu\)**

    Refer to release notes of version 12.2.0 for latest updates. This is being done to backward compatibility with Xanadu.

-   **Version 11.2.1 - June 2025 \(Yokohama\)**
    -   Associating with latest versions of:
        -   Order Management
        -   Telecommunication Open APIs
-   **Version 11.2.0 - June 2025 \(Washington DC, Xanadu\)**
    -   Supporting the latest versions of:
        -   Order Management
        -   Telecommunication Open APIs
-   **Version 11.1.0 - February 2025**

    Changed: v11.0.0 includes TMF product catalog API \(TMF 620\) to include the creation of the product offering price list and price line, new API changes includes, POST, PATCH, DELETE, GET and LIST APIs.

-   **Version 9.2.0 - November 2024**

    Changed: Location-based ordering​, defaulting sales agreement on order, Case Management for Order Operations​, support jeopardy management for business hours when scheduling tasks​.

-   **Version 9.0.1 - August 2024**
    -   Changed: Along with the existing features on order, we have included the following features this time:
        -   Move order: Enable customers to seamlessly change their service from one location to another location through a change order.
        -   Silent batch update: Allow change inventory specification version through a batch update of product inventory records.
        -   Covered product support on order: Allow agents to add contracts or entitlements coverage to product on the order lines.
        -   Support offer to spec mapping: Enable product offering-to-specification mapping that lets agents add specification to existing products.
-   **Version 9.0.0 - August 2024**

    New: added extension points to inbound queue.

-   **Version 8.0.3 - June 2024**

    Changed: Fixes and other improvements.

-   **Version 8.0.1 - May 2024**

    Changed: Adding the capability to update product inventory when product spec is updated and a new version rolled out through API.

-   **Version 7.0.0 - February 2024**
    -   New:
        -   Order enrichment process
        -   Price Management
        -   Consumer order support
        -   In Configurable Workspace, we updated order capture experience, Order Record Page, and introduced Order timeline view
    -   Fixed: External ID related issues fixed
    -   Removed: Demo data moved to base Order Management plugin
-   **Version 6.0.2 - January 2024**

    Security fixes.

-   **Version 6.0.0 - November 2023**

    New: Added demo data related to the telecom-specific offerings, specifications, decision tables, flows, and ordering and inventory.

-   **Version 5.2.0 - August 2023**
    -   New:
        -   Support network slicing for 5G service \(Connected Navigation\)
        -   TMF641 Service Order Spoke \(Southbound Actions\)
        -   Jeopardy Management
        -   Integrate OM TMT with Strategic Portfolio Management
        -   Integrate OM TMT with Field Service Management
        -   Support External inventory ID in order
        -   Telemetry - create KPIs for OM TMT
        -   Support suspend and restore actions for product and service orders
        -   Capture, benchmark, assess large amount of OM TMT performance during E2E SLA processing of jeopardy events
        -   Cancel child domain orders when parent domain order is cancelled manually
    -   Fixed:
        -   Validation for change orders with Add/Disconnect order line combinations at approval time
        -   Support version tracking on domain order
-   **Version 4.0.1 - April 2023**

    -   Fixed:
        -   Attribute Mapping Characteristic Update is not persisted if Product Inventory has characteristic value populated.
        -   State is reverting back from Qualified to Draft.
    Removed: Cycling dependency of Workspace and ORM Utah release. We removed the ORM dependency mentioned in Workspace.

-   **Version 4.0.0 - February 2023**

    New: Calculate and assign order priority for order line items, domain order, customer order and order tasks

-   **Version 3.1.0 - November 2022**
    -   New: Enabled an integration between Order Management for Telecom, Media, &amp; Tech and Telecommunication Network Inventory \(TNI\), when TNI is installed.
    -   Changed: Added a new index to improve query optimization.
    -   Fixed: Resolved various issues
-   **Version 3.0.1 - August 2022**
    -   New:
        -   Supports Horizontal Relationship between product, service and resource
        -   Updated APIs to support catalog versioning and make these APIs TMF conformant
        -   Supports Orchestration Plan UI for order fulfillers
        -   Supports UI based ordering for change and disconnect orders
        -   Updated account information view
    -   Changed: Updated Account - Address mapping
-   **Version 2.0.2 - June 2022**

    Changed: Updated to account for address relationship change by horizontal OM team

-   **Version 2.0.1 - May 2022 \(San Diego\)**

    Fixed: Two way sync issue between order characteristics and order task characteristics

-   **Version 1.6.1 - May 2022 \(Rome\)**
    -   Fixed:
        -   Editable attribute value on order characteristics
        -   Add-cancel order decomposition
-   **Version 2.0.0 - February 2022**
    -   New:
        -   Staggered Decomposition
        -   Provides a phased approach to decomposition
        -   Allows decomposition rules to be driven based on characteristics options captured during the tasks fulfilment.
        -   Add order quantity support
        -   Provides an approach to use quantity while ordering
        -   Allows decomposition to be driven based on quantity
        -   Support for Patch/Cancel in Product Order Open API
        -   Provides a single standards-based approach for maintaining the complete lifecycle of Product Order.
        -   Order Management Data Model Re architecture
-   **Version 1.6.0 - December 2021**

    New: Added functionality to support the new Order Capture user interface

-   **Version 1.5.1 - October 2021**

    Removed: files related to order capture

-   **Version 1.4.0 - August 2021**

    Changed: This version includes changes associated to the optimization of product model generation based on the product offerings

-   **Version 1.3.0 - July 2021**
    -   Changed:
        -   Added support for Service Order Management
        -   Added support for Inflight change order management
        -   Added support for Attribute propagation
        -   Added support for Fallout management
-   **Version 1.1.1 - March 2021**

    Changed: Moved plugin dependencies to Financial Services Operations Core

-   **Version 1.0.0 - December 2020**

    The ServiceNow® Order Management for Telecommunications application enables telecom service providers to capture, manage, and fulfill orders from enterprise customers.


**Parent Topic:**[ServiceNow Store - Technology Provider Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-tech-highlights.md)

**Parent Topic:**[ServiceNow Store - Telecommunications Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-telecom-highlight.md)

