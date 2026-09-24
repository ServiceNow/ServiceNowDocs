---
title: Specify a fallback language for locale-specific languages and LLM prediction
description: Provide language locale support by specifying a fallback language for Virtual Agent to use for topics, keywords, and LLM prediction. For example, the ServiceNow platform doesn't support Mexican Spanish \(mx-es\), but you can designate Spanish \(es\) as the fallback language for a better user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/specify-fallback-lang-llm.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Fallback, language, Now Assist, Virtual Agent, sys\_language]
breadcrumb: [Translate conversations, Virtual Agent, Conversational Interfaces]
---

# Specify a fallback language for locale-specific languages and LLM prediction

Provide language locale support by specifying a fallback language for Virtual Agent to use for topics, keywords, and LLM prediction. For example, the ServiceNow® platform doesn't support Mexican Spanish \(mx-es\), but you can designate Spanish \(es\) as the fallback language for a better user experience.

## Before you begin

Role required: virtual\_agent\_admin or admin

When ServiceNow Otto for Virtual Agent is on and you work with LLM-enabled conversations, you can establish a fallback language in the Languages \[sys\_language\] table.

## Procedure

1.  Navigate to the Languages table \(sys\_language.list\).

2.  Select the language to open the record.

3.  In the **Fallback** field, select the Search icon \(\[Omitted image "icon-search.png"\] Alt text: Search icon.\) and select an available language.

    \[Omitted image "add-fallback-lang-existing.png"\] Alt text: Languages table entry for Mexican Spanish, with Spanish entered as the fallback language.

4.  Select **Update**.


