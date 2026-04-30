---
title: Legacy service catalog access controls
description: Service catalog supports several ways to control access to a catalog item or category. These controls are also known as catalog entitlements.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog security, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Legacy service catalog access controls

Service catalog supports several ways to control access to a catalog item or category. These controls are also known as catalog entitlements.

Instead of access controls, use user criteria that is the supported security model for catalog item and category. For information about user criteria, see [Apply user criteria to items and categories](../task/t_AppUserCritItemsCat.md#).

A service catalog item with no specific access controls is available to all users. If access controls are specified, only users who meet all conditions have access.

The following [entitlements](../task/t_ContrlAccessByCDGUOrLoc.md#) are available:

-   Role
-   Custom script
-   Company, Department, Group, User, or Location

Access controls are checked in the following order: roles, then scripts, then Company, Department, Group, User, or Location.

**Note:** The functionality described here is superseded by access controls using user criteria. Migrate to user criteria for a more flexible and reusable way to define access controls.

-   **[Service Catalog administration](../task/t_ServiceCatalogAdministration.md)**  
Service Catalog enables an administrator to configure the service catalog.
-   **[Restrict access](../task/t_ContrlAccessByCDGUOrLoc.md#)**  
Service Catalog enables an administrator to grant or deny access to a service catalog item or category by company, department, group, user, or location.

**Parent Topic:**[Service Catalog security](../topic/p_ServiceCatalogSecurity.md)

