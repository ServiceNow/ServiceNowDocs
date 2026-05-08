---
title: Server-side localization
description: Server-side localization works the same way as desktop web localization, using either the server system language or user preferences set on the server. Localized components on the server include things like field labels, web content, and other data stored on the server in a translated field.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Localization, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Server-side localization

Server-side localization works the same way as desktop web localization, using either the server system language or user preferences set on the server. Localized components on the server include things like field labels, web content, and other data stored on the server in a translated field.

You can customize translations that use server-side localization the same way you do on the desktop. Translate these elements using the translated name/field table on your instance. For more details on this table, see Translated Name/Fields table

This series of screenshots shows a mobile app on a mobile device with Spanish set as its native language. The device is connected to a ServiceNow instance where the instance language is set to English. The user's mobile device translates the Spanish portions of the text according to the device's user preferences.

The English portions aren't translated by the mobile device. The English text can be translated using your instances localization settings. As an admin you have control over how these elements are translated.

![Mobile screens showing English as the instance language and Spanish as the native device language.](../image/localization-detail-1.png)

-   **[Create translation records for mobile](../task/mobile-translation.md)**  
Create records on the Translated Name / Field table to translate elements of your mobile app that aren't natively translated.
-   **[Translation values for mobile element](../reference/mobile-translation-reference.md)**  
Use this reference to find which values to use to translate your mobile elements.

**Parent Topic:**[Localization on mobile devices](localization-mobile-device.md)

