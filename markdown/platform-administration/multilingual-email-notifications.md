---
title: Multilingual email notifications
description: Using multilingual email notifications, you can send email notifications in the recipient’s preferred language and can easily manage notification content in different languages.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Multilingual email notifications

Using multilingual email notifications, you can send email notifications in the recipient’s preferred language and can easily manage notification content in different languages.

## Email notification translation

You can customize email notifications for users across multiple regions based on their preferred language. For example, a recipient whose language is set to French will receive notification emails in French, while a German requester would be notified in German.

Two types of translations are available for email notifications:

-   [Static translation](static-translation.md)

    Customize email notifications for recipients across multiple regions based on their preferred language. With static translations, the translation request goes to a translator.

-   [Dynamic translation](dynamic-translation.md)

    Customize email notifications automatically for users across multiple regions based on their preferred language.


You can also send emails using a combination of both static and dynamic translation. For example, if an email has to be sent in English, French, Spanish, and German and the translated templates for French and Spanish already exist, then the dynamic translation will only happen for German.

## User preference for email translation

The preferred language set is honoured when the property is set to true. To set user preference for email translation:

-   Set the **glide.email.translation.honour.user\_preference** property to `true`.
-   Navigate to **User menu** &gt; **Preferences** &gt; **Language &amp; region**, select and set the preferred language.

## Groups

If there is no group email ID, a notification triggered for a group with multilingual recipients can send a group email to different people with different language preferences.

If there is a group email ID, an email is sent in a single language to all the recipients in the group. The recipient’s preferred language is not considered.

## Email notification translation plugins

Activate the [glide notification translation plugin](../task/activate-translation-plugin.md) to send multi-lingual emails based on the recipient’s preferred language. The localization framework plugin is activated by default along with the Glide notification translation plugin.

Activate the [translated email retention plugin](../task/activate-email-retention-plugin.md) to archive emails.

