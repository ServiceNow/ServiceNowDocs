---
title: Service Catalog customization
description: Service Catalog enables you to customize the catalog in various ways.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog customization

Service Catalog enables you to customize the catalog in various ways.

No updates are supported on the following internal service catalog tables, either directly or through business rules.

-   Options \[sc\_item\_option\]
-   Variable Ownership \[sc\_item\_option\_mtom\]
-   Question Answer \[question\_answer\]
-   Item Produced Record \[sc\_item\_produced\_record\]
-   Multi Row Question Answer \[sc\_multi\_row\_question\_answer\]

-   **[Cart layout](../concept/c_ConfigureCartLayout.md)**  
Service catalog enables catalog administrators to configure the layout and functionality of the service catalog cart used in your organization to place requests for catalog items.
-   **[Define item quantity choices](../task/t_ItemQuantity.md)**  
In the Service Catalog, the default quantity choices are 1–10. You can configure the quantity selector with additional choices. This configuration is also applicable in Service Portal.
-   **[Remove item restrictions](../task/t_RestrictBehaviorByItemType.md)**  
Service Catalog enables you to remove or apply restrictions on all order guides, record producers, and wizard launchers.
-   **[Using variables for price setup](../concept/c_ServiceCatalogVariablePricing.md#)**  
You can define a price for every service catalog item. The price or recurring price of a catalog item can be modified with variables, increasing the base price for that item.
-   **[Set a recurring price](../concept/c_SetARecurringPrice.md)**  
A catalog item can have a recurring price in addition to an initial price.
-   **[Extend the pricing model](../task/t_ExtendThePricingModel.md)**  
The pricing model is useful if you want the price or recurring price to be dynamically calculated based on how a user completes the ordering form. You can extend the pricing model of a catalog item by editing the item price or the recurring price.
-   **[Hiding prices in the service catalog](../concept/c_HidingPricesInTheServiceCatalog.md#)**  
Administrators can configure options to hide catalog item prices in the service catalog for listings of specific items, for specific types of items, or for all items.
-   **[Create up to ten copies of Service Catalog request](../task/t_EnablingBulkRequests.md)**  
Clone a request to create up to ten copies \(clones\) of the same Service Catalog request, for different users, without having to enter the same information multiple times. For example, you can request a new piece of equipment for several specified people, generating multiple individual requests quickly from a single initial request.
-   **[Create scripts](../reference/r_ServiceCatalogScriptingExtensn.md)**  
Service Catalog enables you to use certain scripts.
-   **[Service catalog home page configuration](../concept/c_ManagingTheHomepageForACatalog.md)**  
The home page for a service catalog provides the primary front end for ordering items within that catalog. You can configure various elements of the pages within the Service Catalog.
-   **[Configure Classic Mobile devices](../task/t_ServiceCatalogOnMobileDevices.md)**  
When you configure Service Catalog on a Classic Mobile device, you can define the layout and presentation of catalogs. You can then perform actions such as ordering products and services, submit incidents and problems using record producers.
-   **[Using the content management system with the service catalog](p_ConfigureContentManagementSystem.md)**  
Use the content management system \(CMS\) to create a custom interface for the service catalog.
-   **[Customization vs configuration](../../../reuse/digital-content-and-design/customization-vs-configuration-concepts.md)**  
There are important differences between customizing and configuring ServiceNow applications. The ServiceNow platform is built to embrace customization and configuration but how you do so can have significant impacts on ServiceNow support, upgrading to future ServiceNow platform versions, and the functionality of the ServiceNow platform.

**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

