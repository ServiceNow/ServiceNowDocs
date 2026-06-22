---
title: Set case and accent sensitivity on a per-column basis
description: Set locale text match to provide case and accent sensitivity when searching the text of table columns. The default behavior for text searching in table columns is insensitive to case and accent \(diacritic\) variations, but you can enforce sensitivity using locale text match.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/system-localization/sl-locale-text-match.html
release: australia
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 3
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Set case and accent sensitivity on a per-column basis

Set locale text match to provide case and accent sensitivity when searching the text of table columns. The default behavior for text searching in table columns is insensitive to case and accent \(diacritic\) variations, but you can enforce sensitivity using locale text match.

## Overview of locale text match

By default, text searching in table columns is insensitive to case \(example: A vs. a\) and accent or diacritic \(example: A vs. Å\).

As an admin, you can modify this behavior for the fields you specify by setting the column attribute **i18n\_locale\_text\_match** and a sys property **com.glide.db.ui\_i18n\_locale\_text\_match**. When set to true, text search on the column retrieves only exact matches for case and accent.

Locale text match is available from Zurich Patch 9 and Australia Patch 2.

Consider the following points when using the locale text match feature.

-   Setting locale text match overrides the collation of SQL queries for the specific column.
-   You can't set the **i18n\_locale\_text\_match** column attribute when the following attribute is set on the same column: **i18n\_session\_language\_sortable** or if property **com.glide.db.session\_language\_collation\_feature**=true. For more information see [Sorting according to the session language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/sorting-session-language.md).
-   Test the case and accent sensitive behavior thoroughly. When the **i18n\_locale\_text\_match** column attribute is set, the behavior is applied to all queries including ACLs, business rules, and so forth.

## Setting the column attribute i18n\_locale\_text\_match

The default behavior is i18n\_locale\_text\_match=false. Set the column attribute to true as follows.

**Note:** For text searches in tables in the product UI, both the column attribute and the sys property **com.glide.db.ui\_i18n\_locale\_text\_match**are required. See the Global property step in the [Other methods for locale text match](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/sl-locale-text-match.md) section of this page.

1.  With the admin role, navigate to sys\_dictionary.list.
2.  Search for the name of your table and the name of the column to which you want to add this attribute.
3.  Open the dictionary entry, and confirm the column's Type. This attribute can be added to **String**, **Translated Text**, or **Translated Field** types.
4.  In the Attributes field of the column, add `i18n_locale_text_match=true`. Use a comma separator without spaces. \(You may need to switch to the Advanced view of the record to see the Attributes field\).

    \[Omitted image "sl-locale-text-match-advanced-view.png"\] Alt text: An example Dictionary Entry in Advanced view, showing the Short description column of the Task table. The Attributes field contains several values including i18n\_locale\_text\_match=true.

5.  As an alternative to the previous step, open the Attributes tab in Related Links, then select New. In the Attributes field search for `locale text match`, then set the Value field to True.

    \[Omitted image "sl-locale-text-match-column-attribute.png"\] Alt text: The form for a Dictionary Attribute new record. In this example, the Attribute field displays "Locale text match" and the Value field displays "true".

6.  Select Update or Submit.

## Other methods for locale text match

There are several methods for controlling locale text matching in specific situations, as follows.

**Note:** These methods can be applied only to a field which has the column attribute i18n\_locale\_text\_match set to true.

1.  GlideRecord: setLocaleTextMatch \(Boolean isLocaleTextMatch\)
    -   Where: Used in scripts, such as for background transactions.
    -   Use case: Temporarily activate or deactivate locale text match \(case and accent sensitivity\) for a specific GlideRecord query
2.  URL parameter: sysparm\_locale\_txt\_match
    -   Where:
        -   Add `sysparm_locale_txt_match=true` or `sysparm_locale_txt_match=false` as an extra parameter in a URL.
        -   Table API. For information see [Explore the REST API for a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/explore-rest-api-for-table.md).
    -   Use case: When the parameter is added, activate or deactivate locale text match \(case and accent sensitivity\) for queries that display data in platform lists.
3.  Global property: com.glide.db.ui\_i18n\_locale\_text\_match
    -   Where: Create a property in sys\_properties, if it doesn't exist already.

        Name: com.glide.db.ui\_i18n\_locale\_text\_match.

        Type: true \| false.

        Value: either true or false according to your business requirements. For text searches in tables in the product UI, both this property and the column attribute should be set to true.

    -   Default: false
    -   Use case: Activate or deactivate locale text match \(case and accent sensitivity\) for queries that display data in the platform lists.

The following order determines how locale text match settings are applied. Higher priority settings override lower ones.

1.  URL parameter: sysparm\_locale\_txt\_match \(highest priority\).
2.  Global property: com.glide.db.ui\_i18n\_locale\_text\_match \(lowest priority\).

