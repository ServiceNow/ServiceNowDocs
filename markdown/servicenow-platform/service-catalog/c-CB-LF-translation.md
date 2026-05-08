---
title: Localization Framework integration with Catalog Builder
description: The Translation Status tab in the Catalog items tab on the Catalog Builder dashboard enables you to view the translation status of catalog items, and translate catalog items on the fly using manual or machine translation methods.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Localization Framework integration with Catalog Builder

The **Translation Status** tab in the Catalog items tab on the Catalog Builder dashboard enables you to view the translation status of catalog items, and translate catalog items on the fly using manual or machine translation methods.

Confirm that the following plugins are installed before you start using Localization Framework in Catalog Builder:

1.  Localization Framework Installer plugin for Service Catalog: The plugin enables the Localization Framework capabilities in Service Catalog and Catalog Builder.
2.  Dynamic Translation plugin: Enables on-the-fly machine translation capabilities.

Translate catalog items information using one of the following modes:

-   Request Translation mode
-   Self-translation \(ad hoc\) mode

## Request translation mode for new catalog items

Set the glide.sc.catalog\_builder.localization.enable\_request\_translation\_mode property to **True**, to enable the Request translations mode.

When you create item, the **Request translations** step appears in the wizard steps region. Select **Browse** to view and select the languages you want to translate the catalog item information to.

For more information, see Request translations for Service Catalog items.

## Request translation mode for existing items

Set the glide.sc.catalog\_builder.localization.enable\_request\_translation\_mode property to **True**, to enable the Request translations mode is enabled.

On the **Catalog Items** tab, select the existing item that you want translated, then select the **Translation status** tab on the right pane \(next to the **Item details** tab\). You would see the list of languages configured in the system along with the state of that language for the catalog item and a **Request translations** link to request for a translation.

Select the **Request translations** link below the language you want the translations for. A dialog appears prompting you to confirm the translation request. When you confirm the translation request on the **Translation status** tab, a localization task gets generated and its corresponding Localization item record \("LRITMXXXXXXX"\) shows up in place of the **Request translations** link. The state for that specific language changes to **Translations requested**.

When the localization task completes in Localization Framework, the **Request translations** link comes back which you can use to request for translations again. The state changes to **Translated**, **Partially translated**, or **Not translated** on the **Translation status** tab, depending on whether the translations occur for all fields, some fields, or no fields in the table.

For more information, see Request translations for Service Catalog items.

## Self-translation \(ad hoc\) mode

Set the glide.sc.catalog\_builder.localization.enable\_request\_translation\_mode property to **False** to enable self-translation mode. The default value for this property is **False**.

In the **Catalog Items** tab, select the existing item you want translated, then select the **Translation status** tab on the right pane \(next to the **Item Details** tab\). The list of languages configured in the system is displayed, along with the state of that language for the catalog item and an **Edit translations** link to edit the translation.

Select the **Edit translations** link to open another tab that contains two comparison UI regions: The left region is the source language, and the right region is the target or translated language. You can compare the language translation side by side in the page, and make changes if required.

For more information, see Request ad hoc translation for Service Catalog items.

## Translation States

|State|Mode|Description|
|-----|----|-----------|
|Not available|Request translation and Self-translation|If the Localization Framework Insights record is not available, the translation state displayed by the system is **Not Available**, and the state appears near the language name.|
|Not translated|Request translation and Self-translation|If there are no translations in the system for that specific catalog item for that language, the state **Not Translated** appears near the language name.|
|Translations requested|Request translation|If there is an active LRTIM associated with a language for the item, the state **Translations requested** appears near the language name.|
|Partially translated|Request translation and Self-translation|If there are partial translations in the system for that specific catalog item for that language, the state **Partially Translated** appears near the language name.|
|Translated|Request translation and Self-translation|If all translations for that specific catalog item for that language exist in the system, the state **Translated** appears near the language name.|

**Parent Topic:**[Creating or editing catalog item template](../task/create-cat-item-template-cat-builder.md)

