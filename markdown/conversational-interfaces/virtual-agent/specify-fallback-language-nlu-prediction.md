---
title: Specify a fallback language for locale-specific languages and NLU prediction
description: Provide language locale support by specifying a fallback language for Virtual Agent to use for topics, keywords, and NLU prediction. For example, the ServiceNow platform doesn't support Mexican Spanish \(mx-es\), but it does support Spanish \(es\), which you can designate as the fallback language for a better user experience.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Fallback, language, NLU, Now Assist, Virtual Agent, sys\_language]
breadcrumb: [Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Specify a fallback language for locale-specific languages and NLU prediction

Provide language locale support by specifying a fallback language for Virtual Agent to use for topics, keywords, and NLU prediction. For example, the ServiceNow® platform doesn't support Mexican Spanish \(mx-es\), but it does support Spanish \(es\), which you can designate as the fallback language for a better user experience.

## Before you begin

**Note:** The fallback language plugin must be installed on the instance. Once installed, the language is available in the Languages \[sys\_language\] table. If Now Assist in Virtual Agent is on and you work with LLM-enabled conversations, you can only establish a fallback language in the Languages \[sys\_language\] table rather than use the following steps.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select **Virtual Agent**.

3.  On the Multi language support card, slide the **Language Detection** toggle switch to enable it.

4.  Select **View All**.

5.  Select the name of a language to open the record.

6.  Select **Edit Record** at the top of the page.

7.  In the **Fallback** field, select the Search icon \(![Search icon.](../images/icon-search.png)\) and select an available language.

    ![Languages table entry for Mexican Spanish. The Fallback line is highlighted, with Spanish entered as the fallback language.](../images/add-fallback-lang-existing.png)

8.  Select **Update**.


## Result

Custom locales appear in the Languages \[sys\_language\] table, along with their fallback language. The language code \(ID\) indicates a language that Virtual Agent can detect. In the following example, three French locales use French as the fallback language. Only French Canadian remains unconfigured.

![The Languages table with custom locales configured. Highlighted entries for Belgium, Luxembourg, and Switzerland have standard French as a fallback, while Canadian French has no Fallback.](../images/fallback-lang-new-locales.png)

**Parent Topic:**[Localization options for Virtual Agent](../concept/multi-language-options-va.md)

