---
title: Control topic discovery and visibility
description: Administrators and topic authors can enable Virtual Agent to discover topics for use in chats, include a topic in the list users see, or both. The topics can be setup topics and small talk topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/manage-topics-task.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Creating a Virtual Agent topic, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Control topic discovery and visibility

Administrators and topic authors can enable Virtual Agent to discover topics for use in chats, include a topic in the list users see, or both. The topics can be setup topics and small talk topics.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Assistant Designer Asset library includes discovery and visibility options when you select the Show actions for this row icon \[Omitted image "kebab-menu.png"\] Alt text: next to each asset in the Asset library. You must select an assistant first.

\[Omitted image "va-active-toggles.png"\] Alt text: Options for managing active topics include discoverable and visible.

Use these options to manage the active topics as follows:

-   Include the topic in topic discovery.

    If an asset is selected as **Discoverable**, it’s invoked when matched with the user's utterance.

    **Note:** If these methods don't generate search results, or Virtual Agent can't determine the appropriate conversation to display, use [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-ai-search.md) as a fall-back method.

-   Include the topic in the list of topics available for use.

    If an asset is selected as **Visible**, it appears whenever the **Show me everything** option is selected in the conversation.


The options you select automatically update the corresponding property in the Topics \[sys\_cs\_topic\] table. For example, if you have enabled **Discoverable**, the **Visible** property in the Topics \[sys\_cs\_topic\] table is set to true.

\[Omitted image "active-props-table.png"\] Alt text: Topics table view with Is Topic Discoverable and Is Topic Visible values highlighted.

**Note:** If the fields aren't visible, you can [configure the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/configure-form-layout.md) to show them.

## Procedure

1.  [Create a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md).

2.  Set the topic to **Active** either in the topic properties header bar, or in the Show actions for this row icon \(\[Omitted image "kebab-menu.png"\] Alt text:\) next to your topic in the Asset library.

    **Note:** Selecting this option also publishes the topic.

3.  Select the options you want to use, or accept the default settings.

    Some options are enabled or disabled by default, based on the type of topic.

    | |Options|
| |Discoverable|Visible|
    |---|-------|
    |---|------------|-------|
    |Topics|Enabled|Enabled|
    |Setup topics|Disabled|Enabled|
    |Small talk topics|Disabled|Enabled|

4.  Test the topic by selecting **Test** in the topic header bar, or using the **Test assistant** drop-down menu in the Asset library after associating your topic with an assistant.

    **Note:** Associate your topic with one or more assistants before testing, under the **Conversational settings** option.


**Parent Topic:**[Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

**Related topics**  


[Conversational settings for assets in the Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/asset-lib-conv-settings.md)

