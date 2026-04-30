---
title: Dynamic translation
description: Using dynamic translation, you can customize email notifications automatically for users across multiple regions based on their preferred language.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multilingual email notifications, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Dynamic translation

Using dynamic translation, you can customize email notifications automatically for users across multiple regions based on their preferred language.

## About dynamic translation for email notifications

Dynamic content notifications are user-specific. You can use dynamic translation to translate notifications automatically based on the language selected by the recipient.

For example, a requester whose language is set to French will automatically receive notification emails in French, while a Spanish requester would be notified in Spanish.

Using dynamic translation involves the following tasks:

1.  [Activate Dynamic Translation](../../dynamic-translation/task/activate-dynamic-translation.md)
2.  [Set system property for dynamic translation](../task/enable-email-notification-translation.md)
3.  [Enable dynamic translation](../task/enable-dynamic-translation.md)

After dynamic translation is enabled, you can send emails and view or preview the translated email in the preferred languages of the recipients by accessing the **Translated Email Contents** tab.

**Note:** The language preference of users mentioned in **cc** and **bcc** fields is not considered.

-   **[Enable dynamic translation](../task/enable-email-notification-translation.md)**  
Enable dynamic translation of notifications for the instance.
-   **[Configure the note banner for translated emails](../task/config-email-notification-banner.md)**  
Configure the content for a translated email note banner displayed at the top of the page to display a customized message to the recipient.
-   **[Enable dynamic translation for email notifications](../task/enable-dynamic-translation.md)**  
Enable dynamic translation for a notification to send dynamically translated emails to recipients in their preferred language.

**Parent Topic:**[Email and SMS notifications](c_EmailNotifications.md)

**Related topics**  


[Static translation](static-translation.md)

