---
title: Enable translation for Now Assist applications
description: Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/intelligent-experiences/enable-ai-experiences/enable-dynamic-translation-for-now-assist-applications.html
release: xanadu
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2024-11-18"
reading_time_minutes: 2
keywords: [Now Assist, application, translation, dynamic, language]
breadcrumb: [Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Enable translation for Now Assist applications

Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications.

## Before you begin

You must have installed and activated the Dynamic Translation application and installed at least one language pack. For more information, see [Activate Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/dynamic-translation/activate-dynamic-translation.md) and [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/system-localization/t_ActivateALanguage.md).

If you don't see a language and region section of your Now Assist Admin console, make sure that you have installed at least one Now Assist application. This installs or updates the required dependencies to the latest version.

Role required: sn\_generative\_ai.nsa\_admin

## About this task

There are two translation services available to translate user-generated content in Now Assist applications. For more information on the differences between the two, see [Translation for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/translation-for-now-assist.md).

After you have enabled either Dynamic Translation or native translation, translations will be available for in-product experiences, Virtual Agent, and the Now Assist panel.

Because the language detection relies on the user's session language, all languages available as language packs are supported for Now Assist applications. If you want to add additional language support, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/system-localization/t_ActivateALanguage.md) for a list of the available languages and instructions for installation.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  On the left-hand panel, select the **Language and region** page.

3.  In the Dynamic Translation or native translation card, toggle the switch to **On**.

    You can enable both Dynamic Translation and native translation. Native translation is applied first. If the language is not supported through native translation, then Dynamic Translation will be applied.

4.  To change the available languages for Now Assist translation, select **Edit** and then select the checkbox next to the languages you want to support.

    When you're done, press **Save**.


## Result

Translation is enabled for Now Assist applications on your instance.

## What to do next

To change the supported languages, select **Edit** and select which languages you want enabled. You can only select languages that you have already installed and activated on your instance.

-   **[Microsoft Azure OEM for Dynamic Translation in Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/dynamic-translation-na-ms-azure-oem.md)**  
Support multi-language input in Now Assist applications with the Microsoft Azure OEM translator service included in Generative AI Controller.

**Parent Topic:**[Configuring Now Assist settings and features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/configuring-na-landing.md)

