---
title: Enable localized product catalogs and product offerings
description: Make product catalogs and offerings available in multiple languages so sales agents can view catalog content in their preferred locale.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/enable-multi-locale-catalogs.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Enable localized product catalogs and product offerings

Make product catalogs and offerings available in multiple languages so sales agents can view catalog content in their preferred locale.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin, admin

## Procedure

1.  Log in to your ServiceNow instance.

2.  Install and activate the languages you want to support.

    For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateALanguage.md).

    The language you want to activate must have the value of the Active field as true in the Languages \[sys\_language\] table.

3.  Add languages in the sn\_prd\_pm.supported\_language\_translations system property that you want to enable.

    The base locale is specified in the glide.sys.language property and the default value is en \(English\).

    1.  In the **All** navigation filter, enter `sys_properties.LIST`.

    2.  In the **Name** field, search and select the **sn\_prd\_pm.supported\_language\_translations** property.

    3.  Enter comma-separated language codes in the **Value** field.

        `en,fr,de`

    4.  Select **Update**.

4.  Populate the translated text for the product offering or product catalog content in the Translated Text \[sys\_translated\_text\] table.

    For a list of Product Catalog Management entities that support translation, see [Multilingual product catalog entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-multilingual-support.md).

    For more information about the Translated Text \[sys\_translated\_text\] table, see [Translating text fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_UseTranslatedText.md) and [Translated text table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_TranslatedText.md).

5.  Translate the existing product offering or catalog entries.

    1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

    2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

    3.  Navigate to the respective module and select a record you want to translate.

        -   **Offerings** &gt; **Product Offerings**.
        -   **Offerings** &gt; **Product Offering Catalog**.
    4.  Regenerate the cache by selecting an option from the More Actions icon \[Omitted image "ellipsis-horizontal-fill-24.svg"\] Alt text: depending on the record type.

        |Record type|Option|
        |-----------|------|
        |Product Offering|**Regenerate Product Offering Cache**|
        |Product Offering Catalog|**Regenerate Catalog Hierarchy Cache**|

        **Note:** You must regenerate the cache if you're adding translations for a published product offering or catalog.


## Result

A Configuration JSON record is created in the Product Offering Translation \[sn\_prd\_pm\_product\_offering\_translation\] and Product Offering Catalog Translation \[sn\_prd\_pm\_product\_offering\_catalog\_translation\] tables in the specified language respectively. Each row corresponds to a product offering or product catalog per locale.

The products in the product configurator UIs are displayed in the language set in the user preferences, from the list of available languages.

**Related topics**  


[ServiceNow AI Platform translation and localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/translation-and-localization.md)

