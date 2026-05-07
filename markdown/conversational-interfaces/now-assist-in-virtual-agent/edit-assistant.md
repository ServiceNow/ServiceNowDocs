---
title: Edit a chat assistant
description: Edit a chat assistant.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 7
breadcrumb: [Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Edit a chat assistant

Edit a chat assistant.

## Before you begin

See [View assistants](view-assistants.md)

Role required: virtual\_agent\_admin or admin

## About this task

When editing a chat assistant, actions may differ.

|Default assistants|Activate|Deactivate|Edit|Test|Delete|
|------------------|--------|----------|----|----|------|
|Now Assist in Virtual Agent \(default\)|Yes|Yes|Yes|Yes|No|
|Now Assist panel - Platform \(default\)|Yes|Yes|Yes \(except for name and description\)|Yes|No|
|Now Assist panel - Developer|Yes|Yes|Yes \(with limited configuration\)|Yes|No|
|Employee Slate assistant \(default\)|Yes|Yes|Yes|Yes|No|
|Now Assist Voice Deployment \(default\)|Yes|Yes|Yes|No|No|

## Procedure

1.  Navigate to **All** &gt; **Assistant Designer**.

2.  From the **Assistants** tab, select **Edit** for the assistant that you want to edit.

    If you’re only able to view an assistant and are unable to edit it, it’s because you don’t have permission to edit the assistant in a specific domain. For more information about assistants in different domains, see [View assistants](view-assistants.md).

    Edit mode opens the assistant in a sub-tab where you can manage and test your chat assistant.

    The sub-tab shows the assistant name and whether it's a chat or voice assistant.

    The Overview page shows the following components:

    -   Assistant name
    -   Assistant status: active or inactive
    -   Assistant hierarchy: primary or secondary assistant. This section only appears if an assistant is set as a primary or secondary assistant.
    -   Assistant description
    -   Display experience
    -   Additional chat features: web search mode, response streaming, document uploads, closed chats, and voice input \(for Now Assist panel Platform assistant\).
3.  From the Overview page, select the appropriate button or link to make your edits.

    ![Overview page when editing an assistant.](../image/NAinVA-edit-overview-122025.png "Overview page when editing an assistant")

    The main action buttons include:

    -   **Save**: Saves updates made to the assistant configuration.
    -   **Test assistant**: Test panel is an overlay. For more information about testing a chat assistant, see [Test a chat assistant](test-assistant.md).
    -   **Activate/Deactivate**: Turn on or off an assistant. One or more display experiences must be selected to activate an assistant.
    1.  To edit chat features, select the **Edit chat features** link. The **Settings** &gt; **Additional chat features** page is displayed. For more information about web search mode, response streaming, document uploads, closed chats and voice input, see [Enable additional chat features](additional-chat-features.md).
    2.  Customize assistant settings by selecting **Go to settings** link. For more information, see [Create a chat assistant](create-assistant.md).
    3.  To add a display experience, select the **Go to display experiences** link. For more information, see [Display your chat assistant on a portal, channel, or mobile app](display-assistant-portal-channel.md). For Now Assist panel assistants, see [Display your assistant on Platform or ServiceNow Studio](display-nap-assistant.md).
    4.  To migrate NLU topics, select the **Migrate topics** link. The Topic Migration application opens a new browser tab. For more information, see [Migrate NLU topics to LLM topics](../../virtual-agent/task/migrate-nlu-llm.md).
    5.  To manage promoted assets, select the **Manage** button. The **Information sources** &gt; **Promoted** page is displayed. All the assets that have been manually promoted for the assistant are shown.
4.  From the **Information sources** tab, select the page that needs editing.

    ![Edit information sources of your assistant.](../image/NAinVA-edit-info-sources-122025.png "Edit information sources") ![]( "Edit information sources")

    -   In **Search sources**, assign search sources to a chat assistant. Search sources are used to determine what the assistant looks at to answer user queries. If there were any search configurations that were previously done, those configurations would remain. For more information, see [Assign search sources to a chat assistant](add-info-sources-assistant.md).
    -   In **Knowledge Graphs**, edit your Knowledge Graph schema to represent semantic relationships in your data. For more information, see [Add a Knowledge Graph schema to a chat assistant](add-kg-schema-assistant.md).
    -   In **Asset types**, add assets or migrate NLU topics. For more information, see [Add assets to a chat assistant](add-assets.md).
    -   In **Asset visibility**, all assets that are assigned to the assistant are shown.
        -   Discoverable: Discoverable assets can be found and used by your assistant when they match what a user says.
        -   Visible: Visible assets appear when users select **Show me everything** in the assistant.
        -   Promoted: Promoted assets give users quick access to your most helpful options. Features up to 6 at the start of every chat.
            -   The number of manually promoted assets is shown.
            -   The assets that have been manually promoted are shown, including asset name, asset description, asset type, and the condition label.
            -   The manually promoted assets can be reordered.
            -   When a promoted asset is deleted by selecting the trash can icon, the asset is demoted from the assistant. The asset still exists within the assistant.
            -   When you select **Add Assets** you can select an **Asset Type** from the drop-down menu and then select a specific existing asset. Select **Save** to promote the asset.
5.  From the **Settings** tab, select the page that needs editing.

    ![Edit assistant settings.](../image/NAinVA-edit-settings-122025.png "Edit assistant settings")

    -   In **Basic details**, you can edit the name and description of the assistant. Names can't be duplicative of another assistant. You can set your assistant as a primary assistant and link it to secondary assistants.

        **Note:** For Now Assist panel Platform and Developer assistants, the basic details, such as name and description, can't be edited. For more information, see [Create a chat assistant](create-assistant.md).

    -   In **AI agent support**, you can prioritize AI agents during skills discovery. For more information, see [Use agentic support for a chat assistant](use-agentic-support.md).
    -   In **Display experiences**, you can select at least one portal, or integrate with your preferred messaging channels, to display your assistant. For more information, see [Display your chat assistant on a portal, channel, or mobile app](display-assistant-portal-channel.md).
    -   In **Branding**, configure branding for standard, enhanced, or premium chat experiences. For more information, see [Brand an assistant](brand-assistant.md).
    -   In **Chat features**, by default, all chat experiences except web search, are turned on. For more information, see [Enable additional chat features](additional-chat-features.md).
    -   In **Chat experience**, you can edit your greeting and closing messages, and fallback options. For more information, see [Manage an assistant chat experience](manage-assistant-chat-experience.md).
    -   In **Response feedback**, when a user rates a response, a response feedback form appears. Configure the options so that users can share feedback regarding what worked about the response, or what needs improvement. For more information, see [Manage response feedback](manage-sentiment-survey.md).

