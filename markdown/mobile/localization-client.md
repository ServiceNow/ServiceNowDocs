---
title: Client-side localization
description: Add customized client-side translations to extend language support on your mobile device. You can include languages beyond those natively supported by the ServiceNow AI Platform base system.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Localization, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Client-side localization

Add customized client-side translations to extend language support on your mobile device. You can include languages beyond those natively supported by the ServiceNow AI Platform base system.

The ServiceNow AI Platform provides translations for multiple languages on your mobile device. These supported languages are listed in the topic [Native localization](../reference/localization-native.md). You can add and customize additional client-side languages using the Mobile Custom Localization ServiceNow Store app.

**Note:** The Mobile Custom Localization app is available from the 20.6.0 mobile client release.

To implement client-side translations for custom languages, you need the Mobile Custom Localization ServiceNow Store app. The ServiceNow Store app contains a set of mobile strings that automatically populates the instance with translatable strings required for localization. Access is granted to the Mobile Translated UI Elements \[sys\_sg\_translated\] table, which automatically populates the Translated Names/Fields table \[sys\_translated.list\]. Translated values can then be displayed on your users' mobile devices.

Translations are provided by the administrators who must configure the required artifacts and use the ServiceNow Localization Framework.

For more information, refer to the following topics:

-   [Client-side translations within your mobile app](https://www.servicenow.com/community/international-localization/need-to-translate-the-mobile-app-check-this/ta-p/3433635) \(ServiceNow Community article\)
-   [System Localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/system-localization-landing.md)
-   [Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/localization-workspace.md)
-   [Translated Name / Field table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslatedNameFieldTable.md)
-   [Artifact configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/framework-configuration.md)
-   [Create and configure a custom artifact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/create-configure-custom-artifact.md)
-   [Localization Framework artifact examples](https://www.servicenow.com/community/international-localization/need-to-translate-a-par-dashboard-check-this/ta-p/2839751) \(ServiceNow Community article\)

## Licensing

The Mobile Custom Localization app is available from the  ServiceNow Store and can be added to your  ServiceNow  subscription. Navigate to the  [ServiceNow Store](https://store.servicenow.com/store), log in with your credentials, and then search for  Mobile Custom Localization.

For more information, refer to the following topics:

-   [ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/servicenow-store.md)
-   [Get a free application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/get-free-app.md)

## General Guidelines for client-side localization

Consider these general guidelines when customizing client-side translations.

-   ** Custom language support**
    -   Custom languages are supported only if the language is recognized by the mobile operating system.
    -   If a custom language isn't supported by the operating system, certain elements, such as days of the week, calendars or text direction, may display incorrectly or default to English.
    -   If the operating system can't render the characters of the custom language, for example, if a required font is missing, translated text may not display correctly.
-   **Switch instance language**
    -   The translated values only apply to the instance that you're configuring.
    -   For Single sign-on \(SSO\) users, the instance language can't be selected during login. To access the full app translation, users must log in with the app language. They can then switch the instance language in the settings, provided they have the necessary permissions to select an alternative language.
-   **Initial user login**

    Client-side custom translations aren't applied before the user's first login, for example, during the initial setup or authentication processes. However, if a user is using custom language translations when they log out, the language setting persists until they log in to a different instance.

-   **Translation accuracy**

    Verify that all strings are accurately translated and present in the custom translation. If any strings are missing or contain incorrect placeholders, the app may fall back to the default language, potentially resulting in a mixed-language display.

-   **Plural support**

    When creating custom translations, keep in mind that plural variants aren't supported. To accommodate this scenario, provide generic translations that make sense for all cases, such as "events: \{number\}" instead of "\{number\} event". 

-   **Screen readers**
    -   VoiceOver feature for iOS
        -   VoiceOver for iOS pronounces on-screen text using the device's preferred language. For more accurate VoiceOver pronunciation, match the application's language with the device's preferred language.
        -   For languages not supported by the operating system, VoiceOver may pronounce strings inaccurately or not at all, depending on the user's device language settings.
        -   The way UI translated elements, like buttons and links, are pronounced is determined by the operating system and follows the device’s language.
    -   TalkBack feature for Android: For an effective TalkBack experience, set both the system default language and "TalkBack text-to-speech" language to match the app language.
-   **System and permission dialogs**

    System and permission dialogs are controlled by the operating system and may be displayed in various languages, including the device language, preferred language, or instance language.

-   **Operating system specific**
    -   For iOS: Certain areas such as the app name, App Intents, shortcuts, and Siri rely on translations contained within the bundle and can't be translated at runtime.
    -   For Android: Languages included in the device’s base setup use their own date and time formats. For custom languages, the app falls back to a default format.

**Parent Topic:**[Localization on mobile devices](localization-mobile-device.md)

