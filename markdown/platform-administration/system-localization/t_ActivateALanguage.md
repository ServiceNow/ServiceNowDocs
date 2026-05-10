---
title: Activate a language
description: By default, the language supported by the platform is American English. You can activate plugins for other supported languages if you have the admin role.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate a language

By default, the language supported by the platform is American English. You can activate plugins for other supported languages if you have the admin role.

## Before you begin

Role required: admin

## About this task

The following plugins are currently available:

-   I18N: Arabic Translations
-   I18N: Brazilian Portuguese Translations
-   I18N: Czech Translations
-   I18N: Dutch Translations
-   I18N: Finnish Translations
-   I18N: French Canada Translations
-   I18N: French Translations
-   I18N: German Translations
-   I18N: Hebrew Translations
-   I18N: Hungarian Translations
-   I18N: Italian Translations
-   I18N: Japanese Translations
-   I18N: Korean Translations
-   I18N: Norwegian Translations
-   I18N: Polish Translations
-   I18N: Portuguese Translations
-   I18N: Russian Translations
-   I18N: Simplified Chinese Translations
-   I18N: Spanish Translations
-   I18N: Swedish Translations
-   I18N: Thai Translations
-   I18N: Traditional Chinese Translations
-   I18N: Turkish Translations

In addition, the I18N: Internationalization plugin \(com.glide.i18n\) provides the elements necessary for localizing an instance without any language translation preloaded. This plugin is useful for localizing an instance to a language other than those listed above. For more information on using the I18N: Internationalization plugin to translate an instance into a custom language, see [Translating to an unsupported language](self-localize.md).

**Note:**

-   Activating internationalization plugins for any of the available languages automatically activates the I18N: Knowledge Management Internationalization Plugin v2 plugin \(com.glideapp.knowledge.i18n2\).
-   Product and Application Names are kept in English in localization plugins. Feature names are translated.
-   After installation, localization plugins can't be uninstalled.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[Languages table](../reference/r_LanguagesTable.md)

[Ensure that translated choices appear for applications added by plugins](activate-translated-choices-plugins.md)

