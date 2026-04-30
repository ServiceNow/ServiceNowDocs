---
title: Enable translation for Now Assist applications
description: Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-18"
reading_time_minutes: 1
keywords: [Now Assist, application, translation, dynamic, language]
breadcrumb: [Localization options for Virtual Agent, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Enable translation for Now Assist applications

Turn on multi-language support for user-entered text with Dynamic Translation in Now Assist applications.

## Before you begin

You must have installed and activated the Dynamic Translation application and installed at least one language pack. For more information, see [Activate Dynamic Translation](https://www.servicenow.com/docs/access?context=activate-dynamic-translation&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

If you don't see a language and region section of your Now Assist Admin console, make sure that you have installed at least one Now Assist application. This installs or updates the required dependencies to the latest version.

Role required: sn\_generative\_ai.nsa\_admin

## About this task

There are two translation services available to translate user-generated content in Now Assist applications. For more information on the differences between the two, see [Translation for Now Assist](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

After you have enabled either Dynamic Translation or native translation, translations will be available for in-product experiences, Virtual Agent, and the Now Assist panel.

Because the language detection relies on the user's session language, all languages available as language packs are supported for Now Assist applications. If you want to add additional language support, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for a list of the available languages and instructions for installation.

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

**Parent Topic:**[Localization options for Virtual Agent](../../virtual-agent/concept/multi-language-options-va.md)

