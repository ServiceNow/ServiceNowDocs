---
title: Change text in the Show me everything button
description: Configure the text in the Show me everything button displayed in the chat window to control the display of the initial greetings and the Show me everything button in Virtual Agent conversations. Edit the message in the System Properties \[sys\_properties\] table, or in a copy of the Greetings setup topic.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [VIrtual Agent, show me everything, button, change, text, system properties, sys\_properties]
breadcrumb: [Working with setup topics, Customizing a chat experience, Configure, Virtual Agent, Conversational Interfaces]
---

# Change text in the Show me everything button

Configure the text in the **Show me everything** button displayed in the chat window to control the display of the initial greetings and the **Show me everything** button in Virtual Agent conversations. Edit the message in the System Properties \[sys\_properties\] table, or in a copy of the Greetings setup topic.

## Before you begin

If you’re updating the Greetings setup topic in Virtual Agent Designer, first [Create a copy](duplicate-virtual-agent-topic.md) of the Greetings setup topic, since the prebuilt Greetings setup topic is read-only.

Role required: virtual\_agent\_admin or admin

## About this task

You can change the Virtual Agent greeting message by either updating the default greeting through the System Properties \[sys\_properties\] table, or changing the message in the Greetings setup topic in Virtual Agent Designer.

If you change the message in the System Properties table, the default greetings setup topic \(and any custom greetings topics that don't override the default **Show me everything**\) all show the updated message. If you change the greeting message through Virtual Agent Designer, you can make more targeted changes, such as a message for an HR-based greeting topic.

The Greetings setup topic contains the Send Topic Picker script action, which controls the text in the **Show me everything** button. To change the text, edit the Send Topic Picker script action in the copy of the Greetings setup topic.

## Procedure

1.  Navigate to **All** and use one of the following methods.

<table id="choicetable_llf_w4t_d1c"><thead><tr><th align="left" id="d64163e132">

Method

</th><th align="left" id="d64163e135">

Description

</th></tr></thead><tbody><tr><td id="d64163e141">

**System properties**

</td><td>

1.  Input `sys_properties.list`.
2.  Under **com.glide.cs.topic\_picker\_button\_label**, set the value to a message of your choice, such as `Show me everything.`
3.  Select the Save icon ![Save icon.](../images/icon_save.png).


</td></tr><tr><td id="d64163e176">

**Virtual Agent Designer**

</td><td>

1.  Navigate to **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.
2.  Select the copy of the Greetings setup topic that you created.
3.  In the **Flow** tab, select the node for the Send Topic Picker script action.
4.  In the Script action properties sheet, select the Script icon ![Script icon.](../images/icon-script.png) to open the **Action expression** script.
5.  Change the `greetingMessage` text string as needed, and select **Save**. For example, to change the button text to **Show more**, you would change the script as follows:

    ```
(function execute() {
    var greetingMessage = vaSystem.getTopicSelectionMessage();
    vaSystem.sendTopicPickerControl(greetingMessage, "Show more");
})()
    ```

6.  Preview the change in the chat window by selecting **Test** in the header bar. The button text change displays as follows:

![Virtual Agent bot displaying the change in the text with the Show me everything option when you tested.](../images/va-showme-button-chg.png)

7.  Select **Save** in the header bar.
8.  When you're ready to make the topic active, select **Publish**.


</td></tr></tbody>
</table>
## Result

If you follow the System Properties method, your change to the greeting message is shown in all Virtual Agent conversations. If you follow the Virtual Agent Designer method, your change is shown in conversations related to the Greetings setup topic.

## What to do next

If you customized your Greetings topic, add it to the default chat experience or to a new custom chat experience that you created. For details, see [Configure a Virtual Agent chat experience](configure-default-chat-experience.md).

**Parent Topic:**[Working with setup topics](../concept/working-setup-topics.md)

