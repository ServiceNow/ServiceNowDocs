---
title: Service Catalog in Service Portal
description: Use Service Portal to configure an improved version of Catalog. You can customize Service Portal where your customers can request catalog items such as service and product offerings. You can use the Service Catalog widgets to build a catalog for your portal.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog in Service Portal

Use Service Portal to configure an improved version of Catalog. You can customize Service Portal where your customers can request catalog items such as service and product offerings. You can use the Service Catalog widgets to build a catalog for your portal.

**Note:** If you’re an existing customer using Service Portal we recommend that you migrate to the Employee Center for a better experience. For more information on Employee Center, see [Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)

The Catalog landing page provides an interface from where you can access the catalog items, requests, approvals, popular items, recent items, and saved bundles. This page is available by default for zBoot users.

**Note:** Upgrade users need to activate the Service Portal - Service Catalog v2 plugin \(com.glideapp.servicecatalog.portal\).

Overview of configurable options in the Service Catalog on the Service Portal and explains how to perform those configurations.

You can access the Catalog landing page in Service Portal using the **Catalog** option from the main menu header of Service Portal.

The landing page has:

-   A search bar to search within all configured catalogs in Service Portal. When you search for a specific item, the search results page displays results based on the configured catalogs and categories.

    Only the items associated with a catalog and category are searchable. The primary category of the item is displayed under the **Category** filter. The catalog where the primary category is defined for the item is displayed under the **Catalog** filter.

-   The **Browse by Categories** option to navigate to the list of categories in Service Catalog and the items within. Click this option to navigate to the categories landing page.
-   The Requests and Approvals widget to display the list of requests and approvals associated with the user. The list is based on the configurations available in the **My Request Filter** module in Platform. For information about the **My Request Filter** module, see [Define filters for My Requests](../task/configure-my-requests.md).
-   The My Saved Bundles widget to display the saved bundles associated with the user. You can remove a bundle, or open a bundle to add or replace the cart with the items in the bundle.
-   The My Recent Items widget to display catalog items, record producers, or order guides that are most recently viewed or requested by the user. An instance option on the widget allows you to display either the viewed or requested items. This widget is not displayed when it has no data.
-   The Popular Items widget to display the most popular catalog items ordered across the organization by other users. These items are displayed based on the **Top Requests** dynamic category. This widget is not displayed when there is no data.

**Note:**

-   In the order status page of a request, stage renderer displays the current stage in a collapsed view. You can expand this view for all stages.
-   These pages have dynamic titles to display the name of the selected entity.
    -   Catalog Item \[sc\_cat\_item\]
    -   Catalog Categories \[sc\_category\]
    -   Order Guide \[sc\_cat\_item\_guide\]

-   **[Access Service Catalog categories in Service Portal](../task/access-categories-portal.md)**  
Access Service Catalog categories to access the catalog items within.
-   **[Add an item to the wish list in Service Portal](../task/add-to-wishlist-portal.md)**  
Add catalog items or record producers to the wish list to review them when required.
-   **[Add a catalog item to the shopping cart](../task/add-to-cart-portal.md)**  
Add a catalog item or order guide to the shopping cart to store at one place and checkout.
-   **[Request a catalog item from Service Portal](../task/request-cat-item-portal.md)**  
Use the SC Catalog Item widget in Service Portal to request a catalog item.
-   **[Request an order guide from Service Portal](../task/request-order-guide-portal.md)**  
Use the SC Order Guide widget on Service Portal to request an order guide with several catalog items for a specific purpose.
-   **[Standard ticket page for a requested item](stpage-req-item.md)**  
In Service Portal, you can configure the ticket page of a requested item to display the related information, while still having a consistent layout that is similar to other request types. This configuration ensures a consistent experience when viewing submitted requests in Service Portal.

**Parent Topic:**[Integrating Service Catalog](integrating-service-catalog.md)

**Related topics**  


[Service Catalog widgets](https://www.servicenow.com/docs/access?context=sc-widgets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

[Content Management and Service Portal](https://www.servicenow.com/docs/access?context=c_CMSAndSP&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

