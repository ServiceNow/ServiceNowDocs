---
title: Manage catalogs in CMS sites
description: When your organization uses the content management system \(CMS\) as well as Service Catalog, you can select which catalogs are supported within the CMS sites.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using the content management system with the Service Catalog, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Manage catalogs in CMS sites

When your organization uses the content management system \(CMS\) as well as Service Catalog, you can select which catalogs are supported within the CMS sites.

## Before you begin

Role required: catalog\_admin or admin

## About this task

Associating catalogs with sites ensures that users can always access an appropriate catalog.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Catalogs** and open the catalog to associate with a site.

2.  In the Sites related list, click **Edit**, select the site to associate with the catalog, and then click **Save**.

3.  Click the reference icon beside the site name, and then click **Open Record**.

    ![Screenshot for service catalog details](../image/ServiceCatalogDetailsCatalogSitesDetails.png "Service catalog details - catalog sites details")

4.  Enter values in the fields, as appropriate.

    |Field|Description|
    |-----|-----------|
    |CMS homepage|The homepage for this site.|
    |CMS search page|The location of the search page for the site.|
    |CMS 'Continue Shopping' page|The location to direct end users to when they click the **Continue Shopping** button in that CMS site. This field is designed to reference a content page URL suffix.|

5.  Click **Update**.


**Parent Topic:**[Using the content management system with the Service Catalog](../topic/p_ConfigureContentManagementSystem.md)

**Related topics**  


[Set up catalog portal pages](../concept/c_SettingCatalogPortalPages.md)

[Manage catalog portal pages](../concept/c_MultipleServiceCatalogs.md#)

