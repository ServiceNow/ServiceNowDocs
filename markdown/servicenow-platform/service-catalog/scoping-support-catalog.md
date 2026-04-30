---
title: Service Catalog scoping
description: Scoping support is available to define the limits of entities in Service Catalog.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog scoping

Scoping support is available to define the limits of entities in Service Catalog.

-   A catalog can have categories from different scopes.
-   A category can only be in the same scope as its parent category.
-   You can associate a catalog item with categories of a different scope.
-   Catalog items can contain variable sets from a different scope.
-   Variables can only be in the same scope as the catalog item or variable set.
-   Catalog UI policies can only be in the same scope as the catalog item or variable set.
-   Catalog client scripts can only be in the same scope as the catalog item or variable set.
-   Catalog data lookup can only be in the same scope as the catalog item or variable set.
-   The rule base of an order guide can have items from different scopes.
-   The scope of the record producer and the target table should be the same.

-   **[Scriptable service catalog variables](../../../script/server-scripting/concept/c_ScriptableServiceCatalogVariables.md)**  
You can use scripting to reference any request item variable from a table in scoped and non-scoped environment.

**Parent Topic:**[Configuring Service Catalog](configuring-service-catalog.md)

