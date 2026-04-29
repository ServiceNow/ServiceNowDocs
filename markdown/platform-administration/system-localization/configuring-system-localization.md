---
title: Configuring System Localization
description: Configure the locales, languages, regions, and locations needed to accommodate your users.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring System Localization

Configure the locales, languages, regions, and locations needed to accommodate your users.

## Configuration overview

The following list is a high-level overview of the workflow to get started localizing an instance. However, there may be use cases where performing these steps in a different order is preferred.

1.  [Set the instance locale](c_DefineLocales.md#)

    By default, the instance locale is the United States \(en.US\). You should set the instance locale before a system has gone into production and not change it after.

2.  [Activate a language](../task/t_ActivateALanguage.md)

    Activate any of the ServiceNow® internationalization \(I18N\) language plugins to get translations of base system UI strings in the languages your users need. American English is the default language and doesn't need to be activated.

3.  [Set the default language for an instance](../reference/r_GlobalLanguage.md)

    Select a default language for an instance if it should be a language other than American English.

4.  [Set a fallback language](../task/set-fallback-language.md)

    Specify the fallback language for another language so that if UI text isn’t translated in a language, the text displays in the fallback language instead. By default, if a UI string isn’t translated in the preferred language of an instance session, it displays in English.

5.  [Set up locations](../task/t_LocationSetup.md)

    Configure the locations that your organization supports to help identify users, assets, incidents, and more by location.

6.  [Create regions for language selection in portals](../../localization-framework/task/create-regions.md)

    Map languages to regions to organize the language selector for guest users.

7.  [Ensure that translated choices appear for applications added by plugins](../task/activate-translated-choices-plugins.md)

    If you activate other application plugins after having activated language plugins, translated choices in lists might not appear for the applications or features installed by their plugins. Ensure that translated choices appear for those applications by activating translated choice records after corresponding English choice records have been added by plugins.


After you configure your instance using the localization options and supported languages, you might need to translate custom content or translate the instance to an unsupported language. For more information, see [Translating custom content](translating-applications.md) and [Translating to an unsupported language](../task/self-localize.md).

