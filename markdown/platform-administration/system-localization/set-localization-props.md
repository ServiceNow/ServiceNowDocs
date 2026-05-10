---
title: System Localization properties
description: System Localization properties configure translation, currency, and locale settings on the instance for users from multiple countries.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [System Localization reference, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# System Localization properties

System Localization properties configure translation, currency, and locale settings on the instance for users from multiple countries.

Some localization properties only appear after the I18N: Internationalization plugin is activated. Some properties are available on the System Localization properties page, but some lesser-used properties are available only from the System Properties \[sys\_properties\] table.

Access the following properties by navigating to **All** &gt; **System Properties** &gt; **System Localization**.

<table id="table_uv2_n34_jz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable sorting \(for lists\) in the user's session language when the language is other than English

 **com.glide.db.session\_language\_collation\_feature**

</td><td>

Enable sorting string values in a column according to the rules of the user's session language. If this option isn’t selected, field values are sorted according to the English alphabet.-   Options: Yes \| No
-   Default value: No
-   Learn more: [Sorting according to the session language](../task/sorting-session-language.md#)

</td></tr><tr><td>

Show the language select box on the login page to allow the user to specify the language they would like to be logged in with.

 **glide.ui.login.language.select**

</td><td>

Enables language selection upon login. -   Options: Yes \| No
-   Default value: Yes
-   Dependency: The I18N: Internationalization plugin must be active

</td></tr><tr><td>

Text Search stemming language.

 **glide.ts.stemming\_language**

</td><td>

Selects the language to match derived words in text search.-   Options: English, German, and French
-   Default value: English
-   Dependency: The I18N: Internationalization plugin must be active
-   Learn more: [Zing matches derived words with stemming](../../search-administration/concept/stemming-matches-derived-words.md)

</td></tr><tr><td>

Displays translation prefix on translatable strings.

 **glide.ui.i18n\_test**

</td><td>

Adds a translation prefix on translatable fields to indicate where to find the string for translation. -   Options: Yes \| No
-   Default value: No
-   Learn more: [Debug translations](../task/t_DisplayATranslationPrefix.md)

</td></tr><tr><td>

Use a single currency model. Display all currencies in the same currency code, regardless of a user's locale, country, or language code.

 **glide.i18n.single\_currency**

</td><td>

Enable single currency mode. -   Options: Yes \| No
-   Default value: No
-   Learn more: [Currency administration](../../currency/concept/currency.md)

</td></tr><tr><td>

Default language for the system \(two character values\)

 **glide.sys.language**

</td><td>

-   Options: en, fr, es, it, de
-   Default value: en

</td></tr><tr><td>

If using the single currency model, display all currencies using this currency code. Currency codes use the ISO 4217 three letter format.

 **glide.i18n.single\_currency.code**

</td><td>

-   Options: ISO 4217 three-letter currency code
-   Default value: USD
-   Learn more: [Currency administration](../../currency/concept/currency.md)

</td></tr><tr><td>

Locale code to use for localization.

 **glide.system.locale**

</td><td>

Determines the system's default currency into which all prices are automatically converted before other sums or conversions are performed. Changing this property after any price or currency fields have been given a value may result in improper conversion or prices that sum incorrectly.-   Options: \[language code\].\[country code\] \(for example, en.GB for Britain, fr.FR for France, de.DE for Germany, or ja.JP for Japan\)
-   Default value: None
-   Learn more: [Locale settings](../../currency/concept/locales.md)

 **Note:** You have already set a value on this system property, do not change this value once a system has gone into production. If a user's locale must be changed, update the "Country code" field on the user record.

</td></tr><tr><td>

Determines whether the platform displays dates and times formatted according to the user's locale.

 **glide\_i18n.date.default\_to\_locale**

</td><td>

Determines whether the platform displays dates and times formatted according to a user's locale when no date or time format has been selected in user preferences. If this option isn't enabled, dates and times are formatted using patterns set in the **glide.sys.date\_format** and **glide.sys.time\_format** properties. -   Options: Yes \| No
-   Default value: No
-   Learn more: [Locale settings](../../currency/concept/locales.md)

</td></tr><tr><td>

For guest users, enables using their IP address to try to set the user's initial language.

 **glide\_i18n.ip\_geolocation**

</td><td>

Determines the platform's default language used from the country associated with the user's IP address if locale can't be determined from other settings. If this option isn't enabled, the platform language defaults to English for guest users whose locale can't be determined.-   Options: Yes \| No
-   Default value: No
-   Learn more: [Locale settings](../../currency/concept/locales.md)

</td></tr><tr><td>

Spell checker dictionary to use for English users.

 **glide.spell.dictionary.en**

</td><td>

Sets the spell checker dictionary used in the system for English users.-   Options: Brazilian Portuguese, Dutch, English US, English UK, French, German, Italian, Portuguese, Russian, Spanish, and Thai
-   Default value: English US
-   Learn more: [Locale settings](../../currency/concept/locales.md)

</td></tr></tbody>
</table>Access the following properties by entering `sys_properties.list` in the navigation filter to open the System Properties \[sys\_properties\] table.

<table id="table_a5f_yzb_kvb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**com.glide.db.i18n\_session\_language\_sortable\_default**

</td><td>

Option to set the default behavior of column sorting. If true, the default behavior of columns is to sort according to the user's session language. If false, the default behavior of columns is to sort according to the English alphabet.

 -   Type: true \| false
-   Default value: true
-   Dependency: The **com.glide.db.session\_language\_collation\_feature** property must be set to true.
-   Learn more: [Sorting according to the session language](../task/sorting-session-language.md#)

</td></tr><tr><td>

**glide\_i18n.language\_fallback\_enabled**

</td><td>

Option to allow setting fallback languages for the instance. Setting fallback languages creates a three-level hierarchy in which an intermediate language is used before defaulting to English when user interface text is not translated in the user's preferred language.

 -   Type: true \| false
-   Default value: true
-   Learn more: [Set a fallback language](../task/set-fallback-language.md)

</td></tr></tbody>
</table>**Parent Topic:**[System Localization reference](system-localization-reference.md)

