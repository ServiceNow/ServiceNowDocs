---
title: Localization Framework support for catalog builder in Service Catalog
description: Localization Framework enables translation of Service Catalog items directly from the catalog builder dashboard in Service Catalog.
locale: en-US
release: xanadu
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Localization Framework support for Service Catalog items, Explore Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Localization Framework support for catalog builder in Service Catalog

Localization Framework enables translation of Service Catalog items directly from the catalog builder dashboard in Service Catalog.

You can do the following tasks on the Catalog Builder dashboard in Service Catalog when the Localization Framework installer plugin \(**com.glide.localization\_framework.installer**\) is installed:

-   Use the **Translation status** tab that is displayed when a Service Catalog item is selected, to perform the following tasks:
    -   View the list of all active languages.
    -   Request the translation of the Service Catalog items directly using the **Request Translation** option if the **glide.sc.catalog\_builder.localization.enable\_request\_translation\_mode** property is set to true.

        **Note:** You can request translations for the items in the active languages only if the Localization Framework setting is available for the particular language.

    -   View the translation status of the Service Catalog items.

        **Note:** The translation status of the Service Catalog items is based on the status and completion of the Localization Framework scheduler jobs.

    -   Use the **Edit Translation** option in case the **glide.sc.catalog\_builder.localization.enable\_request\_translation\_mode** property is set to false, so that you can machine translate and publish the translations on the ad hoc UI.

        **Note:** Machine translate option is only available if the Localization Framework setting is available for that particular language.

-   Request the translations of the Service Catalog items when creating the items.

For more information on the Localization Framework integration with catalog builder, see [Localization Framework integration with Catalog Builder](https://www.servicenow.com/docs/access?context=c-CB-LF-translation&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Localization Framework support for Service Catalog items](lf-support-for-catalog-items.md)

