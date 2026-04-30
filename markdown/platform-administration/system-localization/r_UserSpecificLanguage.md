---
title: User specific language
description: The user has several choices for identifying the language to be used for the instance, as described here.
locale: en-US
release: yokohama
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# User specific language

The user has several choices for identifying the language to be used for the instance, as described here.

To enable user-specific languages, first activate the I18N Translation plugins for the desired languages.

-   Language picker at login: If user-specific language is enabled, users see a choice list on the login page to select their language. To control display of the choice list on the login page, navigate to **All** &gt; **System Properties** &gt; **UI Properties** and use the property Show the language select box on the login page to allow the user to specify the language they would like to be logged in with.
-   Language picker in the user menu \(Next Experience UI\): Users can select their language from the user menu by navigating to **Preferences** &gt; **Language &amp; Region**. The user menu is located in the Next Experience Unified Navigation.
-   Language picker in the System Settings window \(Core UI\): Users can select their language in the General tab of the System settings window. Access this window by clicking the gear icon on the right edge of the banner.
-   Language setting on the user table: If you have users that require a different language in addition to the global language, you can specify a language for them in **All** &gt; **User Administration** &gt; **Users**. If the **Language** field isn't already on the form, you can [configure the form](../../form-administration/concept/configure-form-layout.md#) and add it.

The **Language** field in the User \[sys\_user\] table overrides the default global language for that user's sessions.

![Selection of languages in a User record.](../image/UserLanguage.png "User language")

**Note:** Setting the language for the system guest user sets the language for both the login page and all users without a user role.

