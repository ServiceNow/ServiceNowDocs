---
title: Control topic discovery and visibility
description: Admins and topic authors can enable Virtual Agent to discover topics for use in chats, include a topic in the list users see, or both. The topics can be setup topics and small talk topics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/conversational-interfaces/virtual-agent/manage-topics-task.html
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a Virtual Agent topic, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Control topic discovery and visibility

Admins and topic authors can enable Virtual Agent to discover topics for use in chats, include a topic in the list users see, or both. The topics can be setup topics and small talk topics.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Virtual Agent Designer includes two options in the **Active** option of the header bar.

\[Omitted image "va-active-toggles.png"\] Alt text: Options for managing active topics: included in topic discovery, and included in list of topics.

Admins or topic authors can use these options to manage the active topics as follows:

-   Include the topic in topic discovery.

    By selecting **Included in topic discovery**, admins or topic authors can enable Virtual Agent to discover the topic by using keyword or Natural Language Understanding \(NLU\) discovery.

    **Note:** If these methods don't generate search results, or Virtual Agent can't determine the appropriate conversation to display, use [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/va-ai-search.md) as a fall-back method.

-   Include the topic in the list of topics available for use.

    By selecting **Included in list of topics**, admins or topic authors can include the topic in the **All Topics** menu. The **All Topics** menu lists all of the topics available for use.

    To see the **All Topics** menu, first select **Show all my options** in the chat window.

    \[Omitted image "show-all-topics.png"\] Alt text: Virtual Agent chat window with Show all my options button.

    You should then see the **All Topics** menu.


\[Omitted image "all-topics-menu-2.png"\] Alt text: All Topics menu in the chat window.

The options you select automatically update the corresponding property in the Topics \[sys\_cs\_topic\] table. For example, if you've enabled **Included in topic discovery**, the **Is Topic Discoverable** property in the Topics \[sys\_cs\_topic\] table is set to true.

\[Omitted image "active-props-table.png"\] Alt text: Topics table view with Is Topic Discoverable and Is Topic Visible values highlighted.

**Note:** If the fields are not visible, you can configure the form layout to show them.

## Procedure

1.  [Create a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md).

2.  Select the **Active** option in the header bar.

    **Note:** Selecting this option also publishes the topic.

3.  Select the options you want to use, or accept the default settings.

    Some options are enabled or disabled by default, based on the type of topic.

    | |Options|
| |Included in Topic Discovery|Included in the list of topics|
    |---|-------|
    |---|---------------------------|------------------------------|
    |Topics|Enabled|Enabled|
    |Setup topics|Disabled|Enabled|
    |Small talk topics|Disabled|Enabled|

4.  Select **Save**.

5.  Select **Test** to test the topic.


## Result

Depending on the options enabled, Virtual Agent can discover the topic, the topic is included in the **All Topics** menu in the chat window, or both.

**Parent Topic:**[Create a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md)

