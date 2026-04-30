---
title: Static translation
description: Using static translation, you can customize email notifications for recipients across multiple regions based on their preferred language.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Multilingual email notifications, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer]
---

# Static translation

Using static translation, you can customize email notifications for recipients across multiple regions based on their preferred language.

## About static translation for email notifications

Author localized content for the various content fields on notifications, email templates, and email layout forms using static translation after activating the [translation plugin](../task/activate-translation-plugin.md).

For static translation, the translation request goes to a translator. The translator provides translations for notification content in different languages.

Not all of the fields on the notification forms are translatable.

|Table name|Translatable fields|
|----------|-------------------|
|Email Notification|Subject, message, message\_html, and message\_text|
|Email Template|Subject, message, message\_html, and message\_text|
|Email Layout|Layout|

**Note:**

-   The static content that needs to be translated in mail scripts must be present inside **gs.getMessage\(\)** and translations for the strings must be available in the Message \[sys\_ui\_message\] table​.

-   You can stop the translation of tokens by creating the **glide.email.outbound.static\_translation.session.language.change.enabled** system property and setting it to false.


## Localization Framework

Use the [Localization Framework settings](../../localization-framework/concept/localization-settings.md) to request translations for the following artifact configurations:

-   Email Layout Configuration
-   Email Notification Configuration
-   Email Template Configuration

-   **[Enable static translation](../task/enable-static-translation.md)**  
Enable static translation of notifications for the global application.
-   **[Request a translation for an email notification, template or layout](../task/request-translation-and-send-email-notification.md)**  
Request a translation to send an email in the recipient’s preferred language.

**Parent Topic:**[Email and SMS notifications](c_EmailNotifications.md)

**Related topics**  


[Dynamic translation](dynamic-translation.md)

[Request a translation for an email notification, template or layout](../task/request-translation-and-send-email-notification.md)

