---
title: Set case and accent sensitivity on a per-column basis
description: Set locale text match to provide case and accent sensitivity when searching the text of table columns. The default behavior for text searching in table columns is insensitive to case and accent \(diacritic\) variations, but you can enforce sensitivity using locale text match.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 2
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Set case and accent sensitivity on a per-column basis

Set locale text match to provide case and accent sensitivity when searching the text of table columns. The default behavior for text searching in table columns is insensitive to case and accent \(diacritic\) variations, but you can enforce sensitivity using locale text match.

## Overview of locale text match

By default, text searching in table columns is insensitive to case \(example: A vs. a\) and accent or diacritic \(example: A vs. Å\).

As an admin, you can modify this behavior for the fields you specify by setting the column attribute **i18n\_locale\_text\_match**. When set to true, text search on the column retrieves only exact matches for case and accent.

Locale text match is available from Zurich Patch 9 and Australia Patch 2. Setting locale text match overrides the collation of SQL queries for the specific column.

**Note:**

-   You can't use the **i18n\_locale\_text\_match** column attribute when the following attribute is set on the same column: **i18n\_session\_language\_sortable**. For more information see [Sorting according to the session language](../task/sorting-session-language.md#).
-   Be sure to test the case and accent sensitive behavior thoroughly, because when the **i18n\_locale\_text\_match** column attribute is set the behavior is applied to all queries including ACLs, Business rules, and so forth.

## Setting the column attribute i18n\_locale\_text\_match

The default behavior is i18n\_locale\_text\_match=false. Set the column attribute to true as follows.

1.  With the admin role, navigate to sys\_dictionary.list.
2.  Search for the name of your table and the name of the column to which you want to add this attribute.
3.  Open the dictionary entry, and confirm that the column's Type is **String**. This attribute can also be added for the following Types: **Translated Text** or **Translated Field**.
4.  In the Attributes field of the column, add `i18n_locale_text_match=true`. Alternatively, in Related Links, open the Attributes tab, then select New.

## Other methods for locale text match

There are several methods for controlling locale text matching in specific situations, as follows.

**Note:** These methods can be applied only to a field which has the column attribute i18n\_locale\_text\_match set to true.

1.  GlideRecord: setLocaleTextMatch \(Boolean isLocaleTextMatch\)
    -   Where: Used in scripts, such as for background transactions.
    -   Use case: Temporarily activate or deactivate locale text match \(case and accent sensitivity\) for a specific GlideRecord query
2.  URL parameter: sysparm\_locale\_txt\_match
    -   Where:

        Add `sysparm_locale_txt_match=true` or `sysparm_locale_txt_match=false` as an extra parameter in a URL.

        Table API.

    -   Use case: When the parameter is added, activate or deactivate locale text match \(case and accent sensitivity\) for queries that display data in the UI including reports, dashboards, platform and workspace lists.
3.  Global property: com.glide.db.ui\_i18n\_locale\_text\_match
    -   Where: Create a property in sys\_properties, if it doesn't exist already.

        Name: com.glide.db.ui\_i18n\_locale\_text\_match.

        Type: true \| false.

        Value: either true or false according to your business requirements.

    -   Default: false
    -   Use case: Activate or deactivate locale text match \(case and accent sensitivity\) for queries that display data in the UI including reports, dashboards, platform and workspace lists.

The following order determines how locale text match settings are applied. Higher priority settings override lower ones.

1.  URL parameter: sysparm\_locale\_txt\_match \(highest priority\).
2.  Global property: com.glide.db.ui\_i18n\_locale\_text\_match \(lowest priority\).

