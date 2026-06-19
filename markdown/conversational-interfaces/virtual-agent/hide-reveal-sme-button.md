---
title: Hide or reveal the Show me everything button
description: Set properties to hide or reveal the Show me everything button in Virtual Agent LLM \(large language model\) conversations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/hide-reveal-sme-button.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 2
keywords: [Show me everything button, Virtual Agent, LLM, Large Language Model, Now Assist, greeting Setup topic, Asset]
breadcrumb: [Working with setup topics, Customizing a chat experience, Configure, Virtual Agent, Conversational Interfaces]
---

# Hide or reveal the Show me everything button

Set properties to hide or reveal the Show me everything button in Virtual Agent LLM \(large language model\) conversations.

## Before you begin

Role required: virtual\_agent\_admin or admin

Duplicate the Virtual Agent greeting Setup topic you want to use for your conversation. For example, **Now Assist - Greeting**. For more information, see [Duplicating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/duplicate-virtual-agent-topic.md).

## About this task

The greeting topic of a Virtual Agent includes a **Show me everything** button by default. This button displays the full list of available Virtual Agent topics, and a search filter. Use the following instructions to hide the **Show me everything** button in your Virtual Agent conversations.

## Procedure

1.  Navigate to **All** &gt; **Virtual Agent** &gt; **Designer**.

2.  In the Asset Library, open the greeting Setup topic you've duplicated.

    The topic opens in Virtual Agent Designer.

3.  In the Flow tab, select the **Send skill picker** node.\[Omitted image "sme-button-greeting-topic-flow.png"\] Alt text: Topic flow tab with Send skill picker node highlighted on canvas.

    The **Script action utility** control for the **Send skill picker** node opens in the property sheet.

4.  In the property sheet, select the **Script that defines the operation of the node** button \[Omitted image "icon-script.png"\] Alt text:.

    The **Action expression** script window opens.

5.  In Line 3 of the script, set the `"hideShowMeEverything"` value from `false` to true.\[Omitted image "sme-button-action-expression-window.png"\] Alt text: Send skill picker node Action Expression window with hideShowMeEverything value set to true.

6.  Select **Save**, then select **Publish**.

    The greeting Setup topic activates, and the **Show me everything** button disappears from the Virtual Agent chat where the topic is used.


## What to do next

To reveal the **Show me everything** button again, set the `"hideShowMeEverything"` value from `true` to false.

The duplicated greeting Setup topic is associated with the LLM assistant as the original topic. You can associate the duplicate with another LLM assistant. For more information, see [Customizing a Virtual Agent chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-conversation-settings.md).

**Parent Topic:**[Working with setup topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/working-setup-topics.md)

