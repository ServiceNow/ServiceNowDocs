---
title: Test topic and NLU model translations
description: Test a translated Virtual Agent topic and the localized NLU model to ensure that it works as expected in a conversation.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-10-23"
reading_time_minutes: 1
breadcrumb: [Localize Virtual Agent topics that use NLU topic discovery, Localizing Virtual Agent conversations, Localization options for Virtual Agent, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Test topic and NLU model translations

Test a translated Virtual Agent topic and the localized NLU model to ensure that it works as expected in a conversation.

## Before you begin

Role required: virtual\_agent\_admin or admin

**Note:** An updated Virtual Agent Designer user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not enabled, you will see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Slide the discovery type toggle switch to **NLU/keyword**, and then select the NLU topic you want to test.

3.  Select **Manage languages**.

4.  In the **View language** list, select a language.

5.  In the **Test** column for an intent, select **Test**.

6.  On the test window that appears, run the conversation and review the results in the test tabs.

    For more information about using the chat test window, see [Testing NLU/Keyword topics](../reference/va-designer-testing.md).

    The following image illustrates how you can test a French translation.

    ![The test window displays the conversation in French. The fly-out panel displays the test phrase that was entered and the matching intent.](../images/lang-test-window.png)

7.  End the test by closing the window.


## What to do next

Use the test results to modify the topic as needed. Continue testing as you adjust your topic and the NLU language mappings.

When the topic is ready, publish the topic to make it available to users. You can publish all or some of the NLU mappings. For more information about publishing a topic, see [Publish a Virtual Agent topic](publish-virtual-agent-topic.md).

**Tip:** You can view localization insights from the **Manage languages** page and the Virtual Agent Designer Topics page. Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**, and then select **Localization Insights**.

**Parent Topic:**[Localize Virtual Agent topics that use NLU topic discovery](use-lf-translate-va-nlu.md)

