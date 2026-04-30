---
title: How L2 punchout works
description: Level 2 \(L2\) PunchOut enables buying organizations to search for and discover PunchOut items directly within their procurement application, eliminating the need to search each supplier’s site individually.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Understanding Punchout, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# How L2 punchout works

Level 2 \(L2\) PunchOut enables buying organizations to search for and discover PunchOut items directly within their procurement application, eliminating the need to search each supplier’s site individually.

## Key APIs used in L2 punchout

-   Search API: Enables SPO to query multiple PunchOut systems and display product listings within the application.
-   Product API: If supported by the PunchOut system, this API allows SPO to retrieve detailed product information.
-   Order API: If supported by the PunchOut system, this API enables users to complete the checkout process within SPO itself.

## Multi-supplier support

You can configure SPO with multiple PunchOut endpoints. For more information, see [Punchout configuration in SPO](punchout-configuration-spo.md).

When a search is initiated, SPO queries all configured systems and presents a consolidated set of results to the user.

## Search and checkout flow

-   Users can search for items and view a consolidated list of products returned from all configured PunchOut systems.

    ![Search products.](../image/punchout-level-two-search-products.png)

-   Selected products are added to the cart, and checkout is completed within SPO. Upon checkout, a Purchase Requisition \(PR\) is created. Once approved, a Purchase Order \(PO\) is generated and synced to the corresponding PunchOut system.

    ![Products added to cart.](../image/punchout-level-two-cart.png)


## L2 punchOut flow

The Level 2 PunchOut flow includes the following steps:

-   When a search term is entered, SPO’s backend queries all configured search endpoints, and the resulting product list is displayed in ShoppingHub.
-   If any of the returned payloads lack required mandatory fields, the corresponding results are excluded from further processing.
-   If the PunchOut system supports the Product API, detailed product information can be retrieved from the supplier.
-   After products are added to the cart and the user checks out, SPO creates a Purchase Requisition and, upon approval, a Purchase Order.
-   The PO is then synced with the PunchOut system using either of the following:
    -   cXML payloads, if the supplier supports a cXML order endpoint.
    -   Order API, if the supplier supports API-based order submission.
-   The target PunchOut system is determined based on the supplier information in the PO. SPO retrieves the relevant third-party configuration from the Third-Party Registration table.
-   An extension point, sn\_spend\_intg.ThirdPartySystemApiExtension, is available to support integration with various PunchOut systems:
    -   Users must configure PunchOut system details in the Third-Party Registration table.
    -   Users must also implement the above extension point to enable integration with specific PunchOut systems.

The following figure illustrates the L2 PunchOut flow.![L2 punchout flow.](../image/punchout-level-two-flow.png)

**Parent Topic:**[Understanding Punchout](punchout-overview.md)

