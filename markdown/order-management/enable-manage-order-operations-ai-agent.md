---
title: Enable the manage order operations agent on the Business Portal
description: Activate and associate the manage order operations agent on the Business Portal so that your customers can use this agent to submit order cases autonomously using Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/enable-manage-order-operations-ai-agent.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for Order Management]
---

# Enable the manage order operations agent on the Business Portal

Activate and associate the manage order operations agent on the Business Portal so that your customers can use this agent to submit order cases autonomously using Now Assist.

## Before you begin

Activate and enable a chat assistant such as Now Assist in Virtual Agent to use in the Business Portal. For more information, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md).

[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) enables users to limit the roles and privileges of AI agents during tool execution. AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aia.md).

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

    3.  Select **Promoted** from the More actions icon \[Omitted image "ellipsis-vertical-fill-24.svg"\] Alt text: for the manage order operations agent.


## Result

The chat assistant is activated in the Business Portal.

## What to do next

Customize the subject, content, or formatting of the default email templates for order cases. For more information, see [Email notifications for order cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/order-case-email-notifications.md).

**Parent Topic:**[Configuring Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/now-assist-for-order-management-configuring.md)

**Related topics**  


[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/ai-agent-studio.md)

[Promote or demote LLM conversational subflows, actions, and topics in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/virtual-agent/promote-demote-va-topics.md)

[Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/virtual-agent/vad-topics-page.md)

