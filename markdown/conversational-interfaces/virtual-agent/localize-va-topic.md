---
title: Localizing Virtual Agent conversations
description: The ServiceNow platform provides several methods for localizing Virtual Agent conversations, depending on your needs. Use the Localization Framework to manage all aspects of the translation process, whether you are using machine translation, a third-party provider, or both.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Localizing Virtual Agent conversations

The ServiceNow platform provides several methods for localizing Virtual Agent conversations, depending on your needs. Use the Localization Framework to manage all aspects of the translation process, whether you are using machine translation, a third-party provider, or both.

Use the ServiceNow Localization Framework to standardize and track the translation process for Virtual Agent topics. The framework enables you to define the business process for translating your conversations. Use it to configure the following:

-   How localization requests are fulfilled.

    Options include machine translation, a translation management system \(TMS\), and exporting and importing files.

-   Who is responsible for each step in the process.

    Virtual Agent uses the following roles:

    -   Localization requestor
    -   Localization fulfiller
    -   Localization editor
-   Business rules for the process:
    -   Auto translation and publication
    -   Approval required for translation and publication

To learn more, see [Localization Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/localization-framework-landing.md). To learn more about localization roles, see [Localization roles for Virtual Agent](../reference/localization-roles-va.md#).

## Localizing topics

The localization process flow depends on the method of topic discovery that you are using for your topics. The following types of topic discovery are supported using the Localization Framework.

-   Keyword topic discovery

    When you use the Localization Framework, the chat conversation and the keywords associated with the topic are translated.

-   Natural Language Understanding \(NLU\) topic discovery

    If your topics use NLU, both the topic and the model group must be localized. When you request a translation from Virtual Agent Designer, the topic and any optional keywords are translated. You must request translation for model groups from NLU Workbench. For more information about that process, see [Translate a multilingual model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nlu-service/translate-multilingual-model.md).

    Once the topic and secondary models are localized, you may need to [map the models to the topic](../task/map-nlu-language-model.md) before publishing them.


## Prerequisites

**Important:** Currently, translatable strings such as topic text and bot responses cannot contain embedded quotes. Strings that contain embedded quotes cannot be localized.

Do the following before you begin managing translations:

-   Activate the ServiceNow plugin for each language you want to support.

    The Localization Framework is also installed by default. For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_ActivateALanguage.md).

-   Configure the translation mode that you want to use in the Localization Framework.

    You can configure machine translation, a translation management system \(TMS\), or send via email. For more information, see [Translation modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/translation-modes.md).

-   If you are using Natural Language Understanding \(NLU\), enable languages in Virtual Agent settings.

    For more information, see [Enable NLU languages in Virtual Agent settings](../task/enable-langs-va-gen-settings.md).

-   If necessary, add secondary languages to your NLU model group. For more information, see [Multilingual model management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nlu-service/multilingual-model-managent.md).
-   Assign localization roles to team member groups.

    Users are assigned different roles based on their responsibilities for the translation process. For more information, see [Localization roles for Virtual Agent](../reference/localization-roles-va.md#).


## Manage languages by model

If NLU is enabled for your instance, you can view and manage translations by model and language. Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**, and then click **Manage languages**. Choose a model and a language, and then you can do the following:

-   View translation status
-   Request translations
-   View or edit translations
-   Test translations

Click **Manage NLU translations** for easy access to the model management page in NLU Workbench.

For more information, see [Localize Virtual Agent topics that use NLU topic discovery](../task/use-lf-translate-va-nlu.md).

-   **[Enable NLU languages in Virtual Agent settings](../task/enable-langs-va-gen-settings.md)**  
If you plan to use language-specific NLU models, you must enable the installed languages in the Supported NLU Languages list. A language is enabled if the **Enabled** column displays true. English language is enabled by default.
-   **[Localize Virtual Agent topics that use keyword topic discovery](../task/use-lf-translate-va.md)**  
Use the ServiceNow Localization Framework to manage the process of localizing Virtual Agent conversations and keywords.
-   **[Localize Virtual Agent topics that use NLU topic discovery](../task/use-lf-translate-va-nlu.md)**  
Use the ServiceNow Localization Framework to manage the process of localizing Virtual Agent conversations that use Natural Language Understanding \(NLU\).
-   **[Edit translations for Virtual Agent topics](../task/edit-translations-va-topics.md)**  
A Virtual Agent admin user can edit and publish translations directly in Virtual Agent Designer.
-   **[Request bulk translations for multiple topics](../task/request-bulk-translations-va.md)**  
If you need to translate many Virtual Agent topics across multiple models at one time, you can use the \[sys\_cs\_topic\] table list view to request translations.
-   **[Authoring Virtual Agent conversations for localization](authoring-va-l18n.md)**  
Use localization methods in your Virtual Agent scripts to ensure that the content can be translated. Localization methods are designed to show the original text when no translation is found. These methods can be applied to your code before you have created translations.
-   **[Language support for NLU services](../reference/language-support-nlu-services.md)**  
Entity extraction is supported on ServiceNow® NLU models for specific languages only. The remaining languages support intent matching only. If you are using IBM Watson Assistant, supported languages vary.
-   **[Localization roles for Virtual Agent](../reference/localization-roles-va.md#)**  
Assign localization roles according to a user's scope in the localization process. Users may request translations, fulfill translation requests, and edit translations, based on their role.
-   **[Virtual Agent translation tables](../reference/va-translation-tables.md)**  
Virtual Agent uses the \[sys\_translated\_text\] and \[sys\_ui\_message\] tables to store translated text.

**Parent Topic:**[Localization options for Virtual Agent](multi-language-options-va.md)

