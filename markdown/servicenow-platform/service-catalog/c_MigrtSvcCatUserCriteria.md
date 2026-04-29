---
title: User criteria migration
description: Service catalog user criteria records provide access control for service catalog items and categories.Service Catalog enables you to maintain the required access controls to your service catalog while migrating from entitlements to user criteria.There are significant data structure differences between entitlements and user criteria, which you must be aware of while migrating.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set security for items and categories, Service Catalog security, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# User criteria migration

Service catalog user criteria records provide access control for service catalog items and categories.

You can migrate your access controls to use user criteria. The user criteria feature is automatically enabled for new instances. If you upgrade your instance, a script runs to determine current access control usage.

-   If your instance does not use [entitlement-based](c_LegcySrvcCatAccessCntrol.md) access controls, the user criteria feature is automatically enabled.
-   If your instance does use entitlements, the user criteria feature is not enabled. If you want to use user criteria, use the procedure described on this page to migrate your access controls from entitlements to user criteria.

Migrate to user criteria to provide more reuse, control, and flexibility compared to entitlements.

For example, you can use a single criteria record to make multiple catalog items available to only users who meet all these requirements:

-   Are located in EMEA or APAC
-   Belong to ACER
-   Are in the Training department

**Parent Topic:**[Set security for items and categories](c_ServiceCatalogAccessControls.md)

## Migrate to Service Catalog user criteria

Service Catalog enables you to maintain the required access controls to your service catalog while migrating from entitlements to user criteria.

### Before you begin

Role required: admin

### About this task

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Properties** and verify that the user criteria feature is not already enabled on your system.

    -   If the property **Use "User Criteria" to define access to catalog items and categories** \(**glide.sc.use\_user\_criteria**\) is set to **true**, you can skip the following steps. The user criteria feature is automatically enabled because entitlements were not used in your old system.
    -   If this property is set to **false**, continue with the following steps. The user criteria feature has not been enabled yet on your system.
2.  To preview the user criteria feature, set the service catalog property **Enable both "User Criteria" and "Entitlement" related lists for catalog items and categories when migrating from entitlements** \(**glide.sc.user\_criteria\_migration**\) to **true**.

    This option lets you compare user criteria records and entitlements before you fully switch to user criteria.

3.  Inspect your service catalog items and categories to identify access control sets that you can configure user criteria records for.

    Review your current entitlements and record your current design for access controls. Focus on identifying patterns where multiple items have the same combination of location, group, and so on. Each combination is a possible access control set.

4.  [Create a user criteria record](../task/t_CreateAUserCriteriaRecord.md#) for each access control set that you identified from your inspection of the service catalog.

    You have a step with a list, note, and image.

5.  [Apply these user criteria records](c_ServiceCatalogAccessControls.md) to the items and categories identified, replacing the equivalent entitlements.

6.  Enable user criteria on your system by setting the [service catalog property](../reference/r_ServiceCatalogProperties.md) **Use "User Criteria" to define access to catalog items and categories** \(**glide.sc.use\_user\_criteria**\) to **true**.

    When this property is set to **true**, any remaining entitlements are no longer used.

    **Note:** Scripts in user criteria cannot reference the category or catalog item as **current** as entitlement scripts do. For scripts in user criteria, use the **user\_id** available for the user currently being evaluated against the category or catalog item.


## Data structure differences

There are significant data structure differences between entitlements and user criteria, which you must be aware of while migrating.

Using entitlements, the following tables are loaded into memory and evaluated before rendering.

For catalog items:

![entitlements data structure - catalog items](../image/ServiceCatalogEntitlementsDataStructureCatItems.png "Entitlements Data Structure - Catalog Items")

For categories:

![entitlements data structure - categories](../image/ServiceCatalogEntitlementsDataStructureCategories.png "Entitlements Data Structure - Categories")

The user criteria architecture collects all user attributes in the User Criteria \[user\_criteria\] table.

User criteria records can link to items and categories, as follows.

For catalog items:

-   Catalog Item Available for \[sc\_cat\_item\_user\_criteria\_mtom\]
-   Catalog Item Not Available for \[sc\_cat\_item\_user\_criteria\_no\_mtom\]

![user criteria data structure - catalog items](../image/ServiceCatalogUserCriteriaCatItemMtom.png "User Criteria Data Structure - Catalog Items")

For categories:

-   Category Available for \[sc\_category\_user\_criteria\_mtom\]
-   Category Not Available for \[sc\_category\_user\_criteria\_no\_mtom\]

![Screenshot for user criteria data structure - categories](../image/ServiceCatalogUserCriteriaCategoryMtom.png "User Criteria Data Structure - Categories")

