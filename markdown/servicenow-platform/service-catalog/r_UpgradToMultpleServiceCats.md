---
title: Tables provided with multiple service catalogs
description: Administrators and catalog administrators must consider these points before they upgrade to multiple service catalogs.Catalog site records appear in the Sites related list on the Catalog form.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service catalog setup, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Tables provided with multiple service catalogs

Administrators and catalog administrators must consider these points before they upgrade to multiple service catalogs.

Before upgrading, be aware of changes made to the underlying Service Catalog data model. These changes are made to implement multiple catalogs and do not affect a standard upgrade. However, if you have made customizations, such as changes to the data model, the changes can impact the instance.

The following tables are provided with [multiple service catalogs](../concept/c_MultipleServiceCatalogs.md#):

|Table \[name\]|Description|
|--------------|-----------|
|Catalog Site \[sc\_catalog\_site\]|Associates catalogs to sites.|
|Catalog Portal Page \[sc\_catalog\_view\_mtom\]|Links catalogs to CMS portal pages. Defines the default catalog to portal page combination used by default links.|
|Catalog Items Catalog \[sc\_cat\_item\_catalog\]|Stores the catalogs an item is available in.|
|Catalog Item Category \[sc\_cat\_item\_category\]|Stores the categories an item is available in.|

**Parent Topic:**[Service catalog setup](../topic/p_ServiceCatalogs.md)

## Catalog site records

Catalog site records appear in the **Sites** related list on the Catalog form.

The Catalog Site \[sc\_catalog\_site\] table associates catalogs with [CMS web sites](https://www.servicenow.com/docs/access?context=t_CreateANewSite&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

Several [service catalog system properties](r_ServiceCatalogProperties.md) are used to specify values for different sites used by different catalogs.

|Property|Catalog site field \[name\]|
|--------|---------------------------|
|glide.sc.home.cms\_page|CMS homepage \[cms\_home\]|
|glide.sc.search.cms\_page|CMS search page \[cms\_search\]|
|glide.sc.continue.shopping.target|CMS 'Continue Shopping' page \[cms\_continue\_shopping\]|

