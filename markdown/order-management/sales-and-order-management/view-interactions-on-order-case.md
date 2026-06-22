---
title: View customer context for an order exception chat
description: View the customer's account and contact details on the interaction record and the AI-generated chat summary in the Active Chat panel when the order exception AI agent hands off a chat to a live agent in the CSM/FSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/view-interactions-on-order-case.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Now Assist for Order Management, Sales Customer Relationship Management]
---

# View customer context for an order exception chat

View the customer's account and contact details on the interaction record and the AI-generated chat summary in the Active Chat panel when the order exception AI agent hands off a chat to a live agent in the CSM/FSM Configurable Workspace.

## Before you begin

Chat Summarization must be configured by your admin to enable the AI summarization and recommendation features in Active Chat. For more information, see [Configure chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/configure-chat-summarization-in-now-assist_0.md).

Role required: sn\_order\_case.order\_agent, awa\_agent, and now\_assist\_panel\_user

## About this task

When a customer's chat for an order exception is escalated to a live agent, the agent can accept the chat from the CSM/FSM Configurable Workspace Inbox. After the agent accepts the chat, the Active Chat panel opens with an AI-generated summary of the conversation between the order exception AI agent and the customer, and the associated interaction record opens alongside with the customer's account and contact details already populated.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Accept the order exception chat from the Inbox.

    1.  Select the Inbox icon \[Omitted image "inbox-outline-24.svg"\] Alt text:.

    2.  Change the status to **Available** so that you can accept the live chat.

    3.  Join the chat by selecting **Accept**.

        The Active Chat panel opens with an AI-generated summary of the conversation between the order exception AI agent and the customer. The associated interaction record opens alongside, with the customer's **Account** and **Contact** fields populated from the chat that the customer initiated on the Business Portal.

3.  Review the AI-generated chat summary in the Active Chat panel to understand the customer's request and what the order exception AI agent has done so far.


**Parent Topic:**[Using Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/now-assist-order-management-using.md)

**Related topics**  


[Order Operations Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-mgmt-order-ops.md)

