---
title: Test chat experiences
description: After you create or modify a Virtual Agent chat experience, you can test \(simulate\) it to verify that it works as expected.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customizing a chat experience, Configure, Virtual Agent, Conversational Interfaces]
---

# Test chat experiences

After you create or modify a Virtual Agent chat experience, you can test \(simulate\) it to verify that it works as expected.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**, and select the **Virtual Agent** tab.

2.  Under **Custom greetings and setup**, select **View All**.

3.  Select the chat experience and view the profile.

4.  In the header bar, select **Test**, which automatically opens the chat test window and the associated tabs that display processing details.

    The items that you defined for the chat experience, such as custom setup topics or promoted topics, run in the test window. The following example shows the custom greeting setup topic and promoted topics defined for the ESC portal.

5.  To specify a different context, do the following:

    1.  In the **Test this topic** window, select **Include topic discovery**.

        The **Context** tab appears.

    2.  In the **Context** tab, choose a context from the list of variables \(these context variables are defined in Chat Settings\).

        For example, you could select portal from the list of variables and enter the portal name, `IT Express`.

    3.  Select **Apply context and reload**.

    The items that you defined for the chat experience, such as custom setup topics or promoted topics, run in the test window.


**Parent Topic:**[Customizing a Virtual Agent chat experience](../concept/va-conversation-settings.md)

