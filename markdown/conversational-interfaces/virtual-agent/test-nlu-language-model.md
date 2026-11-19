---
title: Test topic and NLU model translations
description: Test a translated Virtual Agent topic and the localized NLU model to ensure that it works as expected in a conversation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/test-nlu-language-model.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Localize Virtual Agent topics that use NLU topic discovery, Localizing Virtual Agent conversations, Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Test topic and NLU model translations

Test a translated Virtual Agent topic and the localized NLU model to ensure that it works as expected in a conversation.

## Before you begin

**Note:** An updated Assistant Designer Asset library user interface is available when you install ServiceNow Otto in Virtual Agent. This content assumes that you can see the list view. If ServiceNow Otto in Virtual Agent is not installed, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/vad-prev-topics-page.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  Set the discovery type toggle switch to **NLU/keyword**, then open the NLU topic you want to test.

4.  Under the Languages tab, select **Manage languages**.

5.  In the **Select NLU Model** list, select the model group to test.

6.  In the **View language** list, select a language.

7.  In the **Test** column for an intent, select **Test**.

8.  On the test window, run the conversation and review the results in the test tabs.

    For more information about using the chat test window, see [Testing NLU/Keyword topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-designer-testing.md).

    The following image illustrates how you can test a French translation.

9.  End the test by closing the window.


## What to do next

Use the test results to modify the topic as needed. Continue testing as you adjust your topic and the NLU language mappings.

When the topic is ready, publish the topic to make it available to users. You can publish all or some of the NLU mappings. For more information about publishing a topic, see [Publish a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/publish-virtual-agent-topic.md).

**Tip:** You can view localization insights from the **Manage languages** page and the Assistant Designer Asset library. Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**, select **Asset library**, and then select **Localization Insights** from the Resources.

**Parent Topic:**[Localize Virtual Agent topics that use NLU topic discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/use-lf-translate-va-nlu.md)

