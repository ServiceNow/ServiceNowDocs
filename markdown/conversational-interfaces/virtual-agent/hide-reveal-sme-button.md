---
title: Hide or reveal the Show me everything button
description: Set properties to hide or reveal the Show me everything button in Virtual Agent conversations that use LLM \(large language model\) and NLU/Keyword \(Natural Language Understanding\) topic discovery.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with setup topics, Customizing a chat experience, Configure, Virtual Agent, Conversational Interfaces]
---

# Hide or reveal the Show me everything button

Set properties to hide or reveal the **Show me everything** button in Virtual Agent conversations that use LLM \(large language model\) and NLU/Keyword \(Natural Language Understanding\) topic discovery.

## Before you begin

Role required: vitual\_agent\_admin or admin

## About this task

By default, the greeting portion of a Virtual Agent conversation includes a **Show me everything** button, which brings up the entire list of available Virtual Agent topics and a search filter. Use the following steps to toggle the **Show me everything** button for LLM and NLU/Keyword topic discovery, respectively.

## Procedure

1.  Use either of the following methods, depending on whether you are working with LLM or NLU topics.

<table id="choicetable_dwk_ccn_b1c"><thead><tr><th align="left" id="d147486e87">

Topic discovery type

</th><th align="left" id="d147486e90">

Method

</th></tr></thead><tbody><tr><td id="d147486e96">

**LLM**

</td><td>

1.  Navigate to **All** &gt; **Virtual agent** &gt; **Designer**.
2.  Select one of the default greeting topics used in LLM topic discovery such as **Now Assist - Greeting** or **Now Assist Panel - Greeting**.
3.  On the **flow** tab, select the **Send skill picker** Script action utility node.
4.  In the **Action expression** property, open the script field.
5.  Input the following script.

    ```
var hideShowMeEverything = String(vaInputs.now_assist_topics_skill_active_value.value) === "false";
    ```

6.  In the script window, select **Save**.
7.  On the Flow tab, select **Save**.


</td></tr><tr><td id="d147486e168">

**NLU**

</td><td>

1.  Navigate to **All** &gt; **__sys\_properties.list__**.
2.  Under **glide.cs.disable.show\_me\_everything**, set the value to `TRUE`.


</td></tr></tbody>
</table>
## Result

The **Show me everything** button is removed from the greeting messages in your Virtual Agent conversations.

**Parent Topic:**[Working with setup topics](../concept/working-setup-topics.md)

