---
title: Localization on mobile devices
description: ServiceNow mobile apps are localized in many languages, including both left-to-right and right-to-left languages.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Localization on mobile devices

ServiceNow mobile apps are localized in many languages, including both left-to-right and right-to-left languages.

![Mobile language selector](../image/mobile-language-selector.png)

The native mobile applications are localized in two different ways, which means that there is a blending of localization visible inside native applications.

## Native localization

Native \(on device\) localization: Controlled by the device's language preference, which means that many components are localized with the language preference for the user's device. These components can include local screen titles \(such as Settings\) and local button titles \(such as the Clear All button on the filters screen\).

The on-device localization supports the following languages:

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

These translations can't be customized since they ship with the application binary and translated natively on the device according to the language settings for the device.

## Server-side localization

Server-side localization: Controlled the same way as desktop web localization \(server system language / user preference on server\). Localized components on the server include things like field labels, web content, and other data stored on the server in a translated field.

You can customize translations that use server-side localization the same way you do on the desktop. Translated these elements using the translated name/field table on your instance. For more details on this table, see [Translated Name / Field table](https://www.servicenow.com/docs/access?context=r_TranslatedNameFieldTable&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

This series of screenshots shows a mobile app on a mobile device with Spanish set as its native language. The device is connected to a ServiceNow instance where the instance language is set to English. The user's mobile device translates the Spanish portions the text according to the device's user preferences. These elements cannot be changed with your instance localization settings.

The English portions are not translated by the mobile device. The English text can be translated using your instances localization settings. As a admin you have control over how these elements are translated.

![Mobile screens showing English as the instance language and Spanish as the native device language.](../image/localization-detail-1.png)

-   **[Create translation records for mobile](../task/mobile-translation.md)**  
Create records on the Translated Name / Field table to translate elements of your mobile app that are not natively translated.
-   **[Translation values for mobile element](../reference/mobile-translation-reference.md)**  
Use this reference to find which values to use to translate your mobile elements

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

