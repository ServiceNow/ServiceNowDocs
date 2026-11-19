---
title: Exploring Dynamic Translation
description: Learn more about Dynamic Translation and integrating with third-party translation services so you can enable live translation of user-entered text across your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/dynamic-translation/exploring-dynamic-translation.html
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2026-04-14"
reading_time_minutes: 5
breadcrumb: [Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Exploring Dynamic Translation

Learn more about Dynamic Translation and integrating with third-party translation services so you can enable live translation of user-entered text across your instance.

## Dynamic Translation overview

Activating the Dynamic Translation plugin \(com.glide.dynamic\_translation\) enables real-time machine translation of user-entered text in form fields, activity streams, chats, and knowledge articles. You can integrate with a machine translation service provider of your choice. You can configure which tables and features offer on-demand translation for your users.

To localize your instance, including static UI elements, currency, and time displays, see [System Localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/system-localization-landing.md).

To manage and deliver multilingual content at scale, see [Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-workspace/localization-workspace.md).

## Dynamic Translation workflow

1.  Procure any ServiceNow, Inc. subscription that is Professional or above, and includes Dynamic Translation.
2.  Activate your choice of language or languages. For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/t_ActivateALanguage.md). The language plugin also activates [Localization Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/localization-framework-landing.md).
3.  Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\). For information, see [Activate Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/activate-dynamic-translation.md).
4.  Sign up and create an account with a translation service provider. By default, the following translation service providers are partially preconfigured:

    -   Microsoft. To sign up, see the Microsoft [documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/translator-text-how-to-signup). For more information, see [Microsoft Azure Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/microsoft-translation-spoke.md).
    -   Google. To sign up, see the Google [website](https://cloud.google.com/translate/pricing). For more information, see [Google Cloud Translator Service Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/google-translator-spoke.md) and [Set up Google Cloud Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/setup-google-translator.md).

        **Note:** The Google Cloud Translator Service spoke is installed from the ServiceNow Store.

    You can also configure any translation service provider of your choice. For information about custom configurations, see [Integrate with a translation service provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/integrate-translation-service-provider.md).

5.  Configure your translation service provider in Dynamic Translation.
    -   After you have signed up with a translation service provider, do the following in your instance: create a connection, specify the credential information, then activate the translator configuration.
    -   Set at least one translator configuration as the default for detection, to detect the language of the user-entered text.
    -   Set at least one translator configuration as the default for translation request calls.
    -   Dynamic Translation uses the ServiceNow® language codes and supports all the languages that the translation service providers support.

        **Note:** For languages where there is a difference in language codes, see [Create a language code mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/create-language-code-mapping.md) to create a language code mapping record and associate it with the translator configuration record.

6.  Configure your use cases as needed.
    -   To enable dynamic translation in a form field, configure the dictionary attribute. For more information, see [Enable dynamic translation for a field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/configure-field-translation.md).
    -   To enable dynamic translation in an activity stream, include the table name in the allow list property. For more information, see [Dynamic translation on forms and activity streams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dynamic-translation-forms.md).
    -   For other use cases, see the links in the Features column of the following Dynamic Translation benefits table.

## Dynamic Translation benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Live translation on forms|[Dynamic translation on forms and activity streams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dynamic-translation-forms.md)|Agent|
|Knowledge article translation|Together with Localization Framework, [enable the translation of Knowledge Base articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/localization-framework/lf-support-for-kb-articles.md).|Agent|
|Set your preferred translation services|[Dynamic Translation spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dynamic-translation-spoke.md) and integrating with third-party services|Administrator|
|Use an API and enable machine translation for multiple languages|[DynamicTranslation API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dyn-translation-apis.md)|Administrator|
|Translate text in conversations between end users and agents|[Dynamic Translation for Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/ci-dtac-overview.md)|End user, agent|
|Regulated market support|From the Zurich release, support for certain regulated markets is available. For information see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) on the Now Support portal.|Administrator, end user, agent|
|Self-hosted \(on-premise\) support|Dynamic Translation is available to self-hosted \(on-premise\) customers who permit integrations to machine translation vendors.|Administrator|
|Domain separation support|For information about domain separation with Dynamic Translation, see [Domain separation and Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/domain-sep-dynamic-translation.md)|Administrator|

