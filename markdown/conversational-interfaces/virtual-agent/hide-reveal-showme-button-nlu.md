---
title: Hide or reveal the Show me everything button in Natural Language Understanding conversations
description: Set properties to hide or reveal the Show me everything button in Virtual Agent conversations that use NLU/Keyword \(Natural Language Understanding\) topic discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/hide-reveal-showme-button-nlu.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure NLU in Virtual Agent, Configure, Virtual Agent, Conversational Interfaces]
---

# Hide or reveal the Show me everything button in Natural Language Understanding conversations

Set properties to hide or reveal the **Show me everything** button in Virtual Agent conversations that use NLU/Keyword \(Natural Language Understanding\) topic discovery.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

By default, the greeting portion of a Virtual Agent conversation includes a **Show me everything** button, which brings up the entire list of available Virtual Agent topics and a search filter. Use the following steps to toggle the **Show me everything** button for NLU/Keyword topic discovery.

## Procedure

1.  Navigate to **All** &gt; **__sys\_properties.list__**.

2.  Under **glide.cs.disable.show\_me\_everything**, set the value to `TRUE`.


## Result

The **Show me everything** button is removed from the greeting messages in your Virtual Agent conversations.

**Parent Topic:**[Configure Natural Language Understanding in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/configure-nlu-settings.md)

