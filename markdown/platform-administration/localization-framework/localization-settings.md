---
title: Localization Framework settings
description: You can define translation and workflow preferences for one or more languages and for one or all the available artifacts with Localization Framework settings.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Localization Framework settings

You can define translation and workflow preferences for one or more languages and for one or all the available artifacts with Localization Framework settings.

Before you define the translation and workflow preferences, ensure that you have the required artifacts to define the localization settings. For more information, see [Artifact configurations](framework-configuration.md).

**Note:** Languages with no localization settings can't be selected for translation requests.

You can enable one or more of the following translation modes to define the translation preferences. For more information, see [Translation modes](translation-modes.md).

-   Activate the required translator if you want to use machine translation.

    **Note:** Machine translation in the Localization Framework application is powered by Dynamic Translation. Therefore, activating the Dynamic Translation plugin \(com.glide.dynamic\_translation\) enables you to use the machine translation capability in Localization Framework

    .

-   Configure a TMS service of your choice if you want to send the content to a translation management system for translation. For more information, see [Translation Management System configurations](tms-configuration.md).
-   Configure an email subflow if you want to use a subflow other than the default subflow for sending the translatable content file for translation via email. For more information, see [Create a custom email subflow](../task/create-email-subflow.md).

-   **[Create a custom email subflow](../task/create-email-subflow.md)**  
Create an email subflow according to your requirements. You can then select this subflow to define translation preferences for a language.
-   **[Translation Management System configurations](tms-configuration.md)**  
The Localization Framework supports integration with a translation management system to localize the content.
-   **[Configure the Localization Framework preferences](../task/define-translation-preferences.md)**  
Configure the preferences to request the translation in the activated languages.
-   **[Localization Framework Properties: Update Set Strategies](lf-update-set-strategies.md)**  
Use update sets to migrate your translations to another instance. Configure properties for update sets according to your business requirements.

**Parent Topic:**[Configure the Localization Framework](configuring-localization-framework.md)

