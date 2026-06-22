---
title: Preview and test ITSM Virtual Agent Lite topics
description: Run a pre-built IT Service Management \(ITSM\) Virtual Agent Lite topic to decide whether you want to deploy it to your end users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/test-valite-topic.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Virtual Agent, ITSM, IT Service Management, Lite, Conversation Topics]
breadcrumb: [Virtual Agent Lite, Explore, Virtual Agent, Conversational Interfaces]
---

# Preview and test ITSM Virtual Agent Lite topics

Run a pre-built IT Service Management \(ITSM\) Virtual Agent Lite topic to decide whether you want to deploy it to your end users.

## Before you begin

Activate the plugin. For more information, see [ITSM Virtual Agent Conversation Topics Lite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-virtual-agent/setup-itsm-virtual-agent-lite.md) \(com.snc.itsm.virtualagent.lite\).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  On the home page, select the filter icon \[Omitted image "filter-icon.png"\] Alt text: Filter icon., and build a condition with the field **Category**, and **ITSM Self Service Lite** as the type to show only ITSM Virtual Agent Lite conversations.

    Two pre-built topics are available: Check IT Ticket Status and Report IT Issue.

3.  Select the topic that you want to preview.

    In the **Flow** tab, the Virtual Agent Designer canvas opens with a read-only view of the topic flow. You can resize the canvas to see the nodes in the flow, but you can't add or change controls and their related property sheets.

    \[Omitted image "va-lite-check-status-flow.png"\] Alt text: Flow tab of the predefined Check IT Ticket Status topic showing the Virtual Agent Designer canvas in a read-only mode.

4.  Select **Test** to run the conversation in a test chat window.

    For example, if you're testing the Check Ticket Status topic, the test chat window runs the conversation and lets you respond to the prompts displayed. You can also view the test logs to see the messages logged and conversation tasks performed during the conversation, as well as the variables used in the conversation.

    \[Omitted image "valite-logs-example.png"\] Alt text: Example Chat test window with Logs tab displayed.


## What to do next

If you'd like to deploy a topic, [duplicate and publish the topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/duplicate-publish-valite-topic.md) so that it's available to your users.

