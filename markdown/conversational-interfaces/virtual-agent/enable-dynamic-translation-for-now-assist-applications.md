---
title: Configure multilingual service for Now Assist applications
description: Turn on multilingual service for user-entered text with native translation or Dynamic Translation in Now Assist applications.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Now Assist, application, translation, dynamic, language]
breadcrumb: [Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Configure multilingual service for Now Assist applications

Turn on multilingual service for user-entered text with native translation or Dynamic Translation in Now Assist applications.

## Before you begin

To see a list of all available languages supported in Now Assist, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/translation-for-now-assist.md).

To use Dynamic Translation, you must install and activate the application and install at least one language pack. For more information, see [Activate Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/activate-dynamic-translation.md) and [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_ActivateALanguage.md).

**Note:** Dynamic Translation is not supported in regulated markets.

If you don't see a language and region section of your Now Assist Admin console, make sure that you have installed at least one Now Assist application. This installs or updates the required dependencies to the latest version.

Role required: sn\_generative\_ai.nsa\_admin

## About this task

There are two translation services available to translate user-generated content in Now Assist applications. For more information on the differences between the two, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/translation-for-now-assist.md). In that documentation, you can also find the steps for adding another language to your service if it is not preconfigured.

After you have enabled either Dynamic Translation or native translation, translations will be available for in-product experiences, Virtual Agent, and the Now Assist panel.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  On the left-hand panel, select the **Multilingual service**.

3.  In the native translation or Dynamic Translation tab, toggle the switch to **On**.

    A modal displays, confirming your choice and stating that Now Assist streaming of LLM \(large language model\) responses will be unavailable when Dynamic Translation is active.

    **Note:**

    When Dynamic Translation is inactive, Now Assistant streaming is available. The modal message displayed will change according to the status of the Dynamic Translation.

4.  You can enable both Dynamic Translation and native translation.

    Native translation is applied first. If the language is not supported through native translation, then Dynamic Translation will be applied.

5.  To enable the preferred language from the available languages supported in the model providers selected in AI Control Tower, select **Edit** and then select the check-box next to the languages you want to use for translation.

    See [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/translation-for-now-assist.md) for more information about adding new languages for your preferred model to support.

    To update your choice, select **Save**.


## Result

Multilingual service is enabled for Now Assist applications.

**Parent Topic:**[Localization options for Virtual Agent](../../virtual-agent/concept/multi-language-options-va.md)

