---
title: Configure a Virtual Agent chat experience
description: Change the preconfigured Virtual Agent default chat experience or create a custom chat experience for your users. You can configure setup topics, specify promoted topics, and if needed, change the search profile.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Customizing a chat experience, Configure, Virtual Agent, Conversational Interfaces]
---

# Configure a Virtual Agent chat experience

Change the preconfigured Virtual Agent default chat experience or create a custom chat experience for your users. You can configure setup topics, specify promoted topics, and if needed, change the search profile.

## Before you begin

If you want to specify custom setup topics or promoted topics that are displayed to your users in the chat window, make those topics active \(published\) so that they're available for configuration in the chat experience.

Role required: virtual\_agent\_admin or admin

## About this task

The default chat experience provides the default settings for the setup topics and the Virtual Agent search configurations in your instance. A custom chat experience uses the default settings from the default chat experience, but you can override them as needed. Defining a chat experience includes the following steps:

1.  Configure setup topics.
    -   Activate setup topics that are not initially enabled, such as the Anything else, Survey topic, and AI Search Fallback topic types.

        **Note:** If you upgraded from the Quebec release, the AI Search Fallback topic is deactivated by default. Enable it to return AI Search results as a fallback when Virtual Agent can't determine intents, topics, or keywords.

    -   If you want setup topics to be included in topic discovery and listed in the All topics menu, be sure to include those setup topics in the default or a custom chat experience.
    -   Deactivate setup topics if you don't want them to run in your conversations.
2.  Promote up to six topics that are initially displayed to your users, above the **Show me everything** button in the chat window. Promoted topics are supported only on the web and mobile clients.
3.  Change the Search Application configuration in the Search Profile, if needed.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select **Virtual Agent** and under Custom Greetings and Setup, select **View All**.

3.  Define the chat experience.

    Do one of the following:

    -   To change the setup topics, promoted topics, or AI Search setting in the default chat experience, proceed to Step 5 or 6, depending on what you want to change.

        **Note:** The settings for the default chat experience are preconfigured \(read-only\).

    -   To define a new experience, select **New** and complete the fields in Custom Greetings and Setup. Then proceed to Step 4.
    -   To edit a custom experience, select the custom experience record and select **Edit** to update Custom Greetings and Setup.
<table id="table_h2k_tyr_5nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the chat experience.

</td></tr><tr><td>

Description

</td><td>

Brief description \(purpose\) of the chat experience, for example ESC portal.

</td></tr><tr><td>

Active

</td><td>

Option that activates or deactivates the chat experience. The chat experience is active \(enabled\) by default. To deactivate the chat experience, clear this option.

</td></tr><tr><td>

Order

</td><td>

Order value that Virtual Agent uses to determine which chat experience to apply. The default chat experience has an Order value of 1000. Virtual Agent checks all the chat experiences, and if there is more than one match, the experience with the lowest order value \(&lt;1000\) is applied.

</td></tr><tr><td class="sub-head" colspan="2">

Provide the context

</td></tr><tr><td>

Condition Mode

</td><td>

Options for specifying the chat experience context:-   **Simple**: A no-code condition builder to specify the context. This is the mode for the default chat experience.
-   **Advanced**: A JavaScript scripted condition that specifies the context. The condition must evaluate to true.


</td></tr><tr><td>

Condition

</td><td>

Condition builder for specifying the experience context. See the list of the [available context variables](../reference/live-agent-chat-context-vars.md) that can be specified.For example, a Simple, no-code condition might specify the devicetype \(ios or android\) and the portal to which it applies. In this case, the condition applies to the Service Portal \(sp\). ![Simple condition builder for a custom chat experience, showing devicetype is iOS, or devicetype is android, and portal is SP conditions.](../images/va-custom-chat-condition-bldr.png)

</td></tr><tr><td>

Script

</td><td>

Script editor for specifying the condition in a script, if you selected Advanced as the **Condition Mode**.

</td></tr></tbody>
</table>4.  Select **Create custom experience** if this is a new custom chat experience.

    -   The settings for the setup and promoted topics are empty. The setup topics and promoted topics specified for the default chat experience are used automatically, unless you override them by adding new topics or changing them in your custom experience.
    -   To change the setup topics, promoted topics, or AI search settings in the default experience, proceed to the next steps.
5.  Select the **Setup Topics** tab.

    The default experience for new instances automatically includes most of the pre-built setup topics in your conversations, except for the Anything else and Survey topics. If you upgraded from the Quebec or Rome release, the AI Search fallback topic type is also not active.

    **Note:** the Live Agent and Virtual Agent Feedback topics are not listed in the Virtual Agent topic picker \(All Topics\) menu by default. You must associate a setup topic type to a setup topic as part of the default or custom chat experience.

<table id="choicetable_c2f_2g2_3xb"><thead><tr><th align="left" id="d109859e340">

I want to...

</th><th align="left" id="d109859e343">

Procedure

</th></tr></thead><tbody><tr><td id="d109859e349">

**Activate a setup topic, such as the Anything Else or Virtual Agent Feedback topic**

</td><td>

1.  Double-click the **Setup topic** field for the associated **Setup topic type** record.

For example, double-click **Anything Else topic**.

2.  In the **Setup topic** field, choose the setup topic to be used.

For example, **Anything Else topic**.

3.  Select **Save**.


</td></tr><tr><td id="d109859e392">

**Remove a setup topic from a chat experience**

</td><td>

1.  Select the **Setup topic type** field for the setup topic.
2.  In the Setup Topics form, clear the **Setup topic** field.
3.  Select **Update**.


</td></tr><tr><td id="d109859e422">

**Add a new setup topic**

</td><td>

1.  Select **Add topic**. In the Setup Topics form, select the **Setup topic type** and the **Setup topic**.
2.  Select **Submit**.


</td></tr></tbody>
</table>    Select **Update** to apply your changes.

6.  Select the **Promoted Topics** tab to configure promoted topics.

    Specify up to six Virtual Agent topics to be initially displayed in the chat window.

    **Note:** Promoted topics are supported only on the web and mobile clients.

    1.  For each topic to be promoted, select **Add topic**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Topic|The topic to be promoted.|
        |Order|A number that indicates the order in which the topic is listed in the chat window.|

    3.  Select **Submit**.

    4.  If needed, select **Test** to see how the promoted topics are displayed in the chat window.

    ![Custom chat experience list of promoted topics.](../images/custom-chat-promoted-topics.png)

7.  Select the **Search Mapping** tab to change the search application for the chat experience.

    The default mapping consists of the Search Application Configuration and the Search UI \(EVAM\) Configuration for Virtual Agent.

    **Note:** The Virtual Agent Default Search Application Configuration is tied to a search profile that does not provide Person card results.

    1.  Select the value in the **Active** column to open the Search Profile record.

        ![Default chat experience dialog box set to Search Mapping tab, with Boolean value of true highlighted in Active column.](../images/open-search-profile-record.png)

    2.  To change the **Search Application Configuration**, select a configuration from the list of available Search Application Configurations.

        ![Search Profile form displaying the Search Application Configurations for the default chat experience.](../images/va-search-profile-default.png)

    3.  Select **Update**.

    **Note:** Although you can change the **Search UI \(EVAM\) Configuration**, the Virtual Agent Search \(EVAM\) configuration provides the appropriate card views and lists of Virtual Agent search results. If you want to create your own EVAM configuration for use, see [Create an EVAM definition](https://www.servicenow.com/docs/access?context=define-composite-dataset&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).


**Parent Topic:**[Customizing a Virtual Agent chat experience](../concept/va-conversation-settings.md)

