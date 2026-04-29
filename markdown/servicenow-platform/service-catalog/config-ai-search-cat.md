---
title: Configure AI-based catalog search experience
description: Improve employee engagement with an AI-based catalog search experience in Service Portal and Now Mobile. Intelligent query features enable users to quickly and easily find the answers they need.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure search and navigation, Service catalog home page configuration, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure AI-based catalog search experience

Improve employee engagement with an AI-based catalog search experience in Service Portal and Now Mobile. Intelligent query features enable users to quickly and easily find the answers they need.

## Before you begin

Role required: admin

## About this task

You can configure AI-based catalog search experience in portals and Now Mobile. Following are the default search application configurations for Service Portal and Now Mobile:

-   Service Portal Default Search Application. For information about AI Search in Service Portal, see [AI Search in Service Portal](https://www.servicenow.com/docs/access?context=ai-search&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).
-   NowMobile App Search Configurations. For information about AI Search in Now Mobile, see [AI Search in mobile](https://www.servicenow.com/docs/access?context=text-search-advanced-now&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

Each of these search application configurations have an associated search profile based on which the search results are filtered and displayed.

**Note:** If the AI Search is enabled for Now Mobile, the **Experience for items not available in NOW Mobile** \(**glide.sc.mobile.unsupported\_discover**\) property is not applicable. For information on Now Mobile properties, see [Service Catalog properties](../reference/r_ServiceCatalogProperties.md).

Following are a few limitations for AI-based catalog search experience:

-   The facets in Service Portal always show the primary category of the catalog item \(even if the user does not have access to the primary category and the accessible path to the item is via another category that the item is associated with\).
-   If the user does not have read permissions for the category record and its fields, the search results cards in Now Mobile do not show the category of the item.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  To edit the searchable catalogs in a portal or Now Mobile, perform the following steps.

    **Note:** Items are searched for only in the catalogs configured in the search source, irrespective of the catalogs associated with the portal. For information on associating a catalog with a portal, see [Configure a catalog in Service Portal](https://www.servicenow.com/docs/access?context=associate-portal-catalog&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    1.  In the Search Application Configurations list, select the search application configuration associated with the portal.

        For example, **Service Portal Default Search Application** for Service Portal.

    2.  On the Search Application Configuration form, open the search profile.

        For example, **Service Portal Default Search Profile** specified for Service Portal.

        **Note:** To avoid conflicts with future upgrades, it is recommended that you create a search profile instead of using the search profile available in the base system.

    3.  From the Search Sources related list, select a search source.

        For example, **Service Portal Catalogs**.

    4.  In the **Conditions** field, add catalogs where you want the items to be searched for.

        ![Searchable catalogs in Service Portal.](../image/catalog_portals.png "Searchable catalogs in Service Portal")

    5.  Click **Update**.


**Parent Topic:**[Configure search and navigation](../concept/c_ConfigSrchNavUseProps.md)

**Related topics**  


[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

