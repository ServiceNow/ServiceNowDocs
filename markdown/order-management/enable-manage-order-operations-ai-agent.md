---
title: Enable the manage order operations agent on the Business Portal
description: Activate and associate the manage order operations agent on the Business Portal so that your customers can use this agent to submit order cases autonomously using Now Assist.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for Order Management]
---

# Enable the manage order operations agent on the Business Portal

Activate and associate the manage order operations agent on the Business Portal so that your customers can use this agent to submit order cases autonomously using Now Assist.

## Before you begin

Activate and enable a chat assistant such as Now Assist in Virtual Agent to use in the Business Portal. For more information, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md).

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md).

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  On the Manage agentic workflows and AI agents page, select the **AI agents** tab.

3.  Select the **Manage order operations** agent to start configuring it.

4.  On the Define the specialty page, select **Save and continue**.

5.  From the navigation pane, select **Select channels and status**.

6.  On the Select channels and status page, set the **Engage via Virtual Agent assistants** option to **Allow**.

7.  Specify where this AI agent is discoverable by selecting a virtual assistant from the **Choose chat assistants** field.

    For this use case, select **Now Assist in Virtual Agent \(Default\)**.

8.  Promote the agent to add it to the list of promoted topics.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

    2.  On the Assistant Designer, select the **AI agents** tab.

    3.  Select **Promoted** from the More actions icon ![](../../../reuse/icons/product-icons/ellipsis-vertical-fill-24.svg) for the manage order operations agent.


## Result

The chat assistant is activated in the Business Portal.

**Parent Topic:**[Configuring Now Assist for Order Management](../concept/now-assist-for-order-management-configuring.md)

**Related topics**  


[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md)

[Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/promote-demote-va-topics.md)

[Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/vad-topics-page.md)

