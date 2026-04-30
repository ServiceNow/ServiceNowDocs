---
title: Enable Dynamic Translation for an unsupported language
description: The ServiceNow platform supports several languages, but you can enable dynamic machine translation for additional languages in Virtual Agent.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Enable Dynamic Translation for an unsupported language

The ServiceNow® platform supports several languages, but you can enable dynamic machine translation for additional languages in Virtual Agent.

## Before you begin

Install and configure the plugins for Dynamic Translation, as described in [Prerequisites for using Dynamic Translation in Virtual Agent](../concept/prereq-using-dt-va.md).

Role required: virtual\_agent\_admin or admin

## About this task

You can configure Dynamic Translation for any installed language plugin on the ServiceNow® platform. Once installed, the language is available for configuration in the Multi language support card in Virtual Agent Chat Settings. But if you want to support a language that doesn't have a plugin, you can add it to the Languages \[sys\_language\] table. Once added, you can enable dynamic machine translation for that language.

For more information about multi-language support options and their tradeoffs, see [Localization options for Virtual Agent](../concept/multi-language-options-va.md). For more information about custom localizations, see [Custom translations](https://www.servicenow.com/docs/access?context=translating-applications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All**, and then enter `sys_language.list` in the filter.

2.  On the Languages page, click **New**.

3.  On the form, fill in the fields.

<table id="table_asg_jg4_mtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name and locale of the language, if applicable. For example, **Spanish \(Mexican\)**.

</td></tr><tr><td>

Active

</td><td>

Check box indicating that the language is enabled on the instance.

</td></tr><tr><td>

ID

</td><td>

The [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code for the language. For example, **es-MX**.

</td></tr><tr><td>

Text Direction

</td><td>

Direction of text for the language. Options are **Left-to-Right** or **Right-to-Left**.

</td></tr><tr><td>

Fallback

</td><td>

Language to be used if a translation is not available. The language plugin must be installed on the instance and activated for NLU, if you are using NLU topic discovery.For example, if the language is Mexican Spanish, you can specify **Spanish** as the fallback language.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  For a better user experience, translate some of the Virtual Agent system messages into the new language.

    1.  Navigate to **All**, and then enter `sys_ui_message.list` in the filter.

    2.  Translate the following Keys:

        -   Are you sure you want to end the current conversation?
        -   Click here to start a new conversation
        -   Close contact options
        -   \[language name\] \(for example, **English** or **German**\)
        -   Disable audio notifications
        -   End conversation
        -   I have detected you are typing in \{0\}. Would you like to continue the conversation in \{0\}?​
        -   Just now
        -   No
        -   No Chat Agents Currently Available
        -   Please pick an option.
        -   Please type your request
        -   Please type your response here
        -   Send
        -   Start a new conversation
        -   Start typing to filter the list of topics below...
        -   Support options
        -   Yes
        **Note:** If you specify a supported fallback language for the language you're adding, you do not need to translate Keys in the Messages table. For example, if you add Mexican Spanish as a language, you can specify Spanish as the fallback language. The Spanish language plugin already contains translations of these messages. For more information, see [Specify a fallback language for locale-specific languages and NLU prediction](specify-fallback-language-nlu-prediction.md).

6.  When the languages have been added, enable Dynamic Translation.

    For more information on enabling Dynamic Translation, see [Enable Dynamic Translation for languages in Virtual Agent](enable-dynamic-lang-detection.md) and [Configure multilingual service for Now Assist applications](../../now-assist-admin/task/enable-dynamic-translation-for-now-assist-applications.md).


**Parent Topic:**[Localization options for Virtual Agent](../concept/multi-language-options-va.md)

