---
title: Configure multilingual service for ServiceNow Otto applications
description: Turn on multilingual service for user-entered text with native translation or Dynamic Translation in ServiceNow Otto applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/enable-dynamic-translation-for-now-assist-applications.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, application, translation, dynamic, language]
breadcrumb: [Translate conversations, Virtual Agent, Conversational Interfaces]
---

# Configure multilingual service for ServiceNow Otto applications

Turn on multilingual service for user-entered text with native translation or Dynamic Translation in ServiceNow Otto applications.

## Before you begin

To see a list of all available languages supported in ServiceNow Otto, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/translation-for-now-assist.md).

To use Dynamic Translation, you must install and activate the application and install at least one language pack. For more information, see [Activate Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/activate-dynamic-translation.md) and [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateALanguage.md). From the Zurich release, Dynamic Translation has available support in specific regulated markets. For details see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) on the Now Support portal.

Role required: sn\_generative\_ai.nsa\_admin

## About this task

There are two translation services available to translate user-generated content in ServiceNow Otto applications. For more information on the differences between the two, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/translation-for-now-assist.md). In that documentation, you can also find the steps for adding another language to your service if it is not preconfigured.

After you have enabled either Dynamic Translation or native translation, translations will be available for in-product experiences, Virtual Agent, and the ServiceNow Otto panel.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings**.

2.  On the left-hand panel, select the **Multilingual service**.

3.  In the native translation or Dynamic Translation tab, toggle the switch to **On**.

    A modal displays, confirming your choice and stating that streaming of LLM \(large language model\) responses will be unavailable when Dynamic Translation is active.

    **Note:**

    When Dynamic Translation is inactive, streaming is available. The modal message displayed will change according to the status of the Dynamic Translation.

4.  You can enable both Dynamic Translation and native translation.

    Native translation is applied first. If the language is not supported through native translation, then Dynamic Translation will be applied.

5.  To enable the preferred language from the available languages supported in the model providers selected in AI Control Tower, select **Edit** and then select the check-box next to the languages you want to use for translation.

    See [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/translation-for-now-assist.md) for more information about adding new languages for your preferred model to support.

    To update your choice, select **Save**.


## Result

Multilingual service is enabled for ServiceNow Otto applications.

