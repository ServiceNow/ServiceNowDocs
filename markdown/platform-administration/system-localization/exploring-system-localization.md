---
title: Exploring System Localization
description: Learn about support for localizing ServiceNow instances as part of your globalization strategy.
locale: en-US
release: yokohama
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2025-04-11"
reading_time_minutes: 2
breadcrumb: [System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Exploring System Localization

Learn about support for localizing ServiceNow instances as part of your globalization strategy.

## System Localization overview

Localization is the process of making an instance specific to a given region or locale without impacting functionality.

System localization includes the language and locale settings for an instance and is a ServiceNow AI Platform feature that is active by default \(com.glide.i18n.core\). Translations for several languages are available through additional internationalization \(I18N\) language plugins \(for example, com.snc.i18n.spanish\). These language plugins install the I18N: Internationalization plugin \(com.glide.i18n\), which provides the elements necessary for translating an instance.

-   **Languages and translation**

    The I18N language plugins contain translations of the UI string content that ServiceNow provides by default in your instance. Whenever you have customized UI strings that you want to translate, you have to identify and translate these strings manually. In addition, you can create translations for languages for which ServiceNow doesn’t provide a plugin.

    **Note:** Using the Localization Framework application is recommend for translating to an unsupported language or translating large amounts of custom UI string content in a supported language.

-   **Locales, locations, and regions**

    Locale settings support displaying dates, times, and currencies properly based on your location. In addition, you can configure locations to identify users, assets, incidents, and more on the instance. Configure regions to organize languages in language selectors.


## System Localization benefits

<table id="table_of1_z4s_dzb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Display translations of base system UI string content.

</td><td>

-   [Language internationalization support](c_LangInternationalizationSupport.md)
-   [Activate a language](../task/t_ActivateALanguage.md)

</td><td rowspan="3">

Administrators

</td></tr><tr><td>

Display dates, times, and currencies in an instance based on users' locations.

</td><td>

[Configuring locales](c_DefineLocales.md#)

</td></tr><tr><td>

Translate UI string content that you create or modify.

</td><td>

[Translating custom content](translating-applications.md)

</td></tr></tbody>
</table>## Related applications

-   **[Localization Framework](../../localization-framework/concept/localization-framework-landing.md)**

    Using the Localization Framework application is recommend for translating to an unsupported language or translating large amounts of custom UI string content in a supported language. Localization Framework also supports using [Dynamic Translation](../../dynamic-translation/concept/dynamic-translation-overview.md) for live translation of form fields, translating knowledge articles, and integrating with third-party translation services.

-   **[Localization Workspace](../../localization-workspace/concept/localization-workspace.md)**

    Localization Workspace is a targeted translation management experience for content owners and translation fulfillers. With Localization Workspace you can manage and deliver multilingual content at scale.

-   **[Translation management for Knowledge Management](https://www.servicenow.com/docs/access?context=translation-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Knowledge article translation uses a separate system that relies on the I18N: Knowledge Management Internationalization plugin. If this plugin isn’t activated, knowledge article translation falls back on System Localization, with translations kept in the Translated Text \[sys\_translated\_text\] table.


