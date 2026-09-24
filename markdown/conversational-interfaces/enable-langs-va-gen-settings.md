---
title: \(Legacy\) Enable NLU languages in Virtual Agent settings
description: If you plan to use language-specific NLU models, you must enable the installed languages in the Supported NLU Languages list. A language is enabled if the Enabled column displays true. English language is enabled by default.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/enable-langs-va-gen-settings.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Localizing NLU conversations, Localization options for NLU conversations, Build and deploy NLU conversations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Enable NLU languages in Virtual Agent settings

If you plan to use language-specific NLU models, you must enable the installed languages in the Supported NLU Languages list. A language is enabled if the **Enabled** column displays true. English language is enabled by default.

## Before you begin

Activate the ServiceNow plugin for each language you want to support. For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateALanguage.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Click **Virtual Agent**.

3.  Under Natural Language Understanding \(NLU\), click **View settings**.

4.  Find the languages in the Supported NLU Languages list.

5.  If the Enabled column displays **false** for a language, select the link to open the language NLU properties.

    For example, in the following image, German, Portuguese, and Japanese are not enabled.

    \[Omitted image "nlu-settings-example.png"\] Alt text: For each language, the Enabled column shows either true or false.

6.  Select the **Enabled** check box.

7.  Click **Save**.


**Parent Topic:**[\(Legacy\) Localizing Virtual Agent NLU conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/localize-va-topic.md)

