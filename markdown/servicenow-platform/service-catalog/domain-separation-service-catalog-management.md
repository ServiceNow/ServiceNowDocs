---
title: Domain separation and Service Catalog
description: Domain separation is supported in Service Catalog. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Service Catalog

Domain separation is supported in Service Catalog. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see Application support for domain separation.

## Activation information

You should activate the Service Catalog - Domain Separation plugin \(com.glideapp.servicecatalog.domain\_separation\) to enable domain separation for Service Catalog. For information on how you can request for the plugin activation, see [Request for domain separation in Service Catalog](../task/activate-domain-sep-catalog.md).

This plugin should only be activated if there is a need for the following scenarios:

-   Isolate items to requesters in a specific domain.
-   Make items unavailable for request in any other domain irrespective of the domain hierarchy.

If Service Catalog has already been domain separated as a custom solution, activating this plugin may override the existing behavior to enforce the plugin-specific isolation.

## How domain separation works in Service Catalog

Service providers supporting multiple customers in a single ServiceNow instance can ensure data privacy across domains using domain separation. Service providers can ensure that items created or published in a specific domain can only be requested by users in that domain without adding additional user criteria to the individual catalog items.

In Service Catalog, catalog items \(catalog items, record producers, content items, and order guides\) are domain-separated as data. Catalogs, categories, and variables are not domain-separated, and belong to the global domain. Also, items that need to be shared across multiple domains must be published in the global domain and restricted by user criteria.

Domain separation in Service Catalog is applicable to all requester views in the ServiceNow AI Platform, Service Portal, Agent Workspace, mobile application, as well as to all API calls requesting for items.

## Domain-separated tables

The **Domain** \(sys\_domain\) and **Domain Path** \(sys\_domain\_path\) columns are added to the following tables that are domain-separated:

-   sc\_cat\_item
-   sc\_item\_option
-   sc\_multi\_row\_question\_answer
-   question\_answer

## Effective domain for a user

For users with visibility to a single domain, the effective domain is the user’s domain. For users with visibility to multiple domains, the effective domain is the domain selected in the domain picker.

## Visibility of catalog items - Item creation and maintenance

A catalog item can be created or published in any domain in the hierarchy. For information on creating a catalog item, see [Create or edit a catalog item](../task/t_DefineACatalogItem.md#).The item is created in the effective domain of the user. For information on enabling the domain picker, see Enable domain selection menus in Core UI. Once the item is created in a specific domain, all future edits to the item are done in that domain itself.

If a catalog item is published using Item Designer, the domain of the item is the domain selected in the domain picker while publishing the item. Once the item is published, it can only be modified and re-published in the domain it was originally published in.

Catalog items are domain separated as data. Only for maintenance and administration, the visibility of the catalog items follows the data domain hierarchy rules. For information on domain separation hierarchies, see Domain separation hierarchies.

User criteria associated with a catalog item must be visible in the domain of the catalog item. If not visible, catalog item is considered to be not associated with that user criteria.

## Visibility of catalog items - Item request flow

The catalog item created in a specific domain is available in the browse, search, and request experience only in that domain and not available in the peer domains, child domains, and parent domains irrespective of the hierarchy and visibility of the domains. So, requesters can only request for items in their domain as well as in the global domain.

For users with access to multiple domains \(for example, IT fulfiller\), the items are available for request based on the domain selected in the domain picker. To view or request an item of a specific domain, the user should switch to that domain. For information on enabling the domain picker, see Enable domain selection menus in Core UI.

When a requester submits a request using an order guide which has items from multiple domains, only the items in the effective domain and the global domain are ordered.

The target records such as requests, requested items, or records created by record producers are created in the effective domain.

## Request fulfilment flow and reporting for a domain-separated catalog item

The target records such as requests, requested items, or records created by record producers can be accessed by a fulfiller who has visibility to the domain that the record has been generated in. For information on visibility in domain hierarchies, see Visibility domains and Contains domains. Even when the fulfiller modifies the requested item from a domain other than the requested item’s domain, the modifications are recorded in the target record’s domain. Since the target records are separated as data, the reports retrieve data based on the effective domain of the user requesting the report.

## Request flow by a fulfiller from a different domain

When a fulfiller creates a request from a parent record such as an incident in Agent Workspace or in ServiceNow AI Platform, the fulfiller can only request for an item from the parent record’s domain or from the global domain. Also, the corresponding target records are created in the parent record’s domain.

**Note:** Items from multiple domains cannot be added to the cart.

## Catalog client scripts and catalog UI policies

Since the catalog client scripts and catalog UI policies are domain-separated as processes, scripts and policies in the parent domain can be overridden in the child domains. However, these scripts and policies are applicable based on the domain of the catalog item or the domain of the target record.

For example, consider that A is the parent domain and B is its child domain. A catalog item in domain B is associated with a catalog client script defined in domain A. If this catalog client script is overridden in the child domain B, the overridden script in domain B is applicable while fulfilling the requested item in domain B. Even when a fulfiller from the parent domain A fulfills the requested item in the child domain B, the overridden script in domain B is applicable.

**Note:** It is recommended to not override catalog client scripts and catalog UI policies.

## Catalog builder

An item can only be edited in the domain that it has been created. Catalog UI policies and actions added in catalog builder are created in the same domain as that of the item.

-   **[Request for domain separation in Service Catalog](../task/activate-domain-sep-catalog.md)**  
Enable domain separation in Service Catalog by requesting for the activation of the Service Catalog - Domain Separation plugin \(com.glideapp.servicecatalog.domain\_separation\).

**Parent Topic:**[Service Catalog Reference](service-catalog-reference.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

