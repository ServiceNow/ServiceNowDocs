---
title: Control topic discovery and visibility
description: Admins and topic authors can enable Virtual Agent to discover topics for use in chats, include a topic in the list users see, or both. The topics can be setup topics and small talk topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/manage-topics-task.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 2
breadcrumb: [Creating a Virtual Agent topic, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Control topic discovery and visibility

Admins and topic authors can enable Virtual Agent to discover topics for use in chats, include a topic in the list users see, or both. The topics can be setup topics and small talk topics.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Virtual Agent Designer includes discovery and visibility options when you select the Show actions for this row icon \[Omitted image "kebab-menu.png"\] Alt text: next to each topic in the Asset library.

\[Omitted image "va-active-toggles.png"\] Alt text: Options for managing active topics include discoverable and visible.

Admins or topic authors can use these options to manage the active topics as follows:

-   Include the topic in topic discovery.

    By selecting **Discoverable**, admins or topic authors can enable Virtual Agent to discover the topic by using keyword or Natural Language Understanding \(NLU\) discovery.

    **Note:** If these methods don't generate search results, or Virtual Agent can't determine the appropriate conversation to display, use [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-ai-search.md) as a fall-back method.

-   Include the topic in the list of topics available for use.

    By selecting **Visible**, admins or topic authors can include the topic in the **All Topics** menu. The **All Topics** menu lists all of the topics available for use.

    To see the **All Topics** menu, first select **Show all my options** in the chat window.

    You should then see the **All Topics** menu.


\[Omitted image "all-topics-menu-2.png"\] Alt text: All Topics menu in the chat window.

The options you select automatically update the corresponding property in the Topics \[sys\_cs\_topic\] table. For example, if you've enabled **Discoverable**, the **Visible** property in the Topics \[sys\_cs\_topic\] table is set to true.

\[Omitted image "active-props-table.png"\] Alt text: Topics table view with Is Topic Discoverable and Is Topic Visible values highlighted.

**Note:** If the fields are not visible, you can [configure the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/configure-form-layout.md) to show them.

## Procedure

1.  [Creating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md).

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


## Result

Depending on the options enabled, Virtual Agent can discover the topic, the topic is included in the **All Topics** menu in the chat window, or both.

**Parent Topic:**[Creating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md)

