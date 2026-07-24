---
title: Set up catalog portal pages
description: The Catalog Portal Page \[sc\_catalog\_view\_mtom\] table links catalogs to CMS portal pages and defines the default catalog to portal page combination used by URLs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/c\_SettingCatalogPortalPages.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using the content management system with the service catalog, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up catalog portal pages

The Catalog Portal Page `[sc_catalog_view_mtom]` table links catalogs to CMS portal pages and defines the default catalog to portal page combination used by URLs.

For example, the default portal page for the service catalog is the catalog\_default page.

Catalog portal page records appear in the Catalog Portal Pages related list on the Catalog form. The Catalog Portal Page table generates two values in a URL: **sysparm\_catalog\_view** and **sysparam\_catalog**. Use the [Catalog Portal Page form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_MultipleServiceCatalogs.md) to enter a custom link, if required.

## Resolve missing catalog portal pages

If a catalog record is not associated to a catalog portal page record, ServiceNow attempts to present a view based on a set prefix of: **catalog\_&lt;catalog name&gt;**.

For example, if the default service catalog has no catalog portal page record, the system sets **sysparm\_view** to **catalog\_Service\_Catalog**. With this setting, when you navigate to **Self-Service** &gt; **Service Catalog**, you view a new and apparently blank **catalog\_Service\_Catalog** portal page, instead of the existing and populated **catalog\_default** portal page.

To correct, go to the Sites related list on the Catalog form and [add a new catalog portal page record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_MultipleServiceCatalogs.md) manually.

For example, for the default service catalog, add a record with the following values:

-   Catalog: Service Catalog
-   Portal Page: Catalog \(catalog\_default\)
-   Default: true

**Parent Topic:**[Using the content management system with the service catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/p_ConfigureContentManagementSystem.md)

**Related topics**  


[Manage catalogs in CMS sites]()

[Manage catalog portal pages]()

