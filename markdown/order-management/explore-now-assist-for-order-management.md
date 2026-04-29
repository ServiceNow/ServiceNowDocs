---
title: Exploring Now Assist for Order Management
description: With the Now Assist for Order Management application, you can use generative AI to summarize complex orders involving multiple products, services, and fulfillment tasks for faster, more accurate decision-making and improved customer responsiveness.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-11"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist for Order Management]
---

# Exploring Now Assist for Order Management

With the Now Assist for Order Management application, you can use generative AI to summarize complex orders involving multiple products, services, and fulfillment tasks for faster, more accurate decision-making and improved customer responsiveness.

## Now Assist for Order Management overview

AI summarization of orders provides a real-time, consolidated view of complex orders spanning multiple products, services, and fulfillment tasks. It empowers agents to:

-   Enhance the customer experience with timely updates, clear communication, and seamless handoffs that lead to better satisfaction.
-   Track changes and validate details to maintain consistency and transparency.
-   Minimize errors and improve communication across suppliers and partners.
-   Monitor tasks that are at risk of missing deadlines and take corrective action early.
-   Assign tasks to appropriate resources based on priority and skill.
-   Make rapid prioritization decisions to avoid delays.

## Now Assist for Order Management skills

The Now Assist for Order Management application includes the generative AI skill that enables:

1.  Order agent: Quickly check order status, identify issues, and resolve them without navigating to multiple tabs or line items.
2.  Fulfillment agent: Gain visibility into the fulfillment progress, spot risks early, and intervene proactively.

## Generative and agentic AI applications for enabling customer self-service

The Now Assist for Order Management includes the following applications that enable business-to-business \(B2B\) customers to submit order and invoice cases autonomously in simple conversational format from the Business Portal.

-   **Manage Order Operations**

    The Manage Order Operations application \(com.sn\_ord\_ops\_aias\) includes the following AI agents:

    -   Manage order operations AI agent: Enables B2B customers to submit order cases autonomously from the Business Portal using natural language.
    -   Order exception AI voice agent: Enables B2B customers to submit order cases using voice calls.
    Get started by performing the following tasks:

    -   [Enable the manage order operations agent on the Business Portal](../task/enable-manage-order-operations-ai-agent.md)
    -   [Configure ATP API for the manage order operations agent](../task/create-atp-api-call.md)
-   **Manage Invoice Operations**

    The Manage Invoice Operations application \(com.sn\_inv\_ops\_aias\) includes the following AI agents and agentic workflow:

    -   Invoice dispute intake assistant AI agent: Enables B2B customers to submit invoice dispute cases autonomously from the Business Portal using natural language.
    -   Invoice dispute AI voice agent: Enables customers to submit invoice dispute cases using voice calls.
    -   Invoice dispute assist agentic workflow: Enables finance agents to validate and resolve invoice disputes using a guided experience from the Now Assist panel in the CSM/FSM Configurable Workspace. Internally, it uses the invoice dispute support assistant AI agent to validate invoice information, trigger API calls to check quantity discrepancies and provide resolutions.
    Get started by performing the following tasks:

    -   [Configure AI-assisted invoice dispute intake on the Business Portal](../task/enable-manage-invoice-operations-ai-agent.md)
    -   [Configure the invoice quantity validation extension point](../task/configure-invoice-quantity-check-ep.md)
    -   [Configure the invoice dispute resolution extension point](../task/configure-invoice-case-resolution-ep.md)
    -   [Make the invoice dispute assist workflow available in the Now Assist panel](../task/enable-invoice-dispute-assist-agentic-workflow.md)

**Parent Topic:**[Now Assist for Order Management](now-assist-order-management.md)

**Related topics**  


[Configuring Now Assist for Order Management](now-assist-for-order-management-configuring.md)

[Using Now Assist for Order Management](now-assist-order-management-using.md)

