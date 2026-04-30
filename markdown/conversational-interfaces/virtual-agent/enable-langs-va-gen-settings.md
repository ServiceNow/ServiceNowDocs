---
title: Enable NLU languages in Virtual Agent settings
description: If you plan to use language-specific NLU models, you must enable the installed languages in the Supported NLU Languages list. A language is enabled if the Enabled column displays true. English language is enabled by default.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Localizing Virtual Agent conversations, Localization options for Virtual Agent, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Enable NLU languages in Virtual Agent settings

If you plan to use language-specific NLU models, you must enable the installed languages in the Supported NLU Languages list. A language is enabled if the **Enabled** column displays true. English language is enabled by default.

## Before you begin

Activate the ServiceNow plugin for each language you want to support. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Click **Virtual Agent**.

3.  Under Natural Language Understanding \(NLU\), click **View settings**.

4.  Find the languages in the Supported NLU Languages list.

5.  If the Enabled column displays **false** for a language, select the link to open the language NLU properties.

    For example, in the following image, German, Portuguese, and Japanese are not enabled.

    ![For each language, the Enabled column shows either true or false.](../images/nlu-settings-example.png)

6.  Select the **Enabled** check box.

7.  Click **Save**.


**Parent Topic:**[Localizing Virtual Agent conversations](../concept/localize-va-topic.md)

