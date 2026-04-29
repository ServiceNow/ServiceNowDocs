---
title: Localization on mobile devices
description: ServiceNow mobile apps are localized in many languages, including both left-to-right and right-to-left languages. Additionally, you can customize non-default languages on the client-side. These features ensure that your translations remain consistent across your mobile applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Localization on mobile devices

ServiceNow mobile apps are localized in many languages, including both left-to-right and right-to-left languages. Additionally, you can customize non-default languages on the client-side. These features ensure that your translations remain consistent across your mobile applications.

![Mobile language selector](../image/mobile-language-selector.png)

ServiceNow mobile applications draw localized texts from multiple sources, which means that native apps may display a mix of localization methods.

-   **Native localization**

    Native localization uses the device’s language settings to automatically localize built-in elements such as screen titles and button labels. For more information, see [Native localization](../reference/localization-native.md).

-   **Server-side localization**

    Server-side localization is controlled in a similar way to desktop web localization, using the server system language or user preference. This option enables you to customize translations for components like field labels and web content. For more information, see [Server-side localization](localization-server-side.md).

-   **Client-side localization**

    Client-side localization uses the device’s UI to localize app-rendered elements such as screens, lists, and buttons. You can include languages beyond those natively supported by the ServiceNow AI Platform base system. For more information, see [Client-side localization](localization-client.md).


-   **[Native localization](../reference/localization-native.md)**  
Native \(on device\) localization is controlled by the device's language preference, which means that many components are localized with the language preference for the user's device. These components can include local screen titles, such as Settings, and local button titles, such as the Clear All button on the filter screen.
-   **[Server-side localization](localization-server-side.md)**  
Server-side localization works the same way as desktop web localization, using either the server system language or user preferences set on the server. Localized components on the server include things like field labels, web content, and other data stored on the server in a translated field.
-   **[Client-side localization](localization-client.md)**  
Add customized client-side translations to extend language support on your mobile device. You can include languages beyond those natively supported by the ServiceNow AI Platform base system.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

