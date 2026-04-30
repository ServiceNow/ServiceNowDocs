---
title: Resolve friendly fraud by using agentic AI
description: Resolve friendly fraud by using the friendly fraud AI agent to determine the actions to take for the disputed amount, the customer relationship, and assessing the outcome of the detection logic to evaluate the results.
locale: en-US
release: yokohama
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2025-03-28"
reading_time_minutes: 2
breadcrumb: [Using agentic workflows, Now Assist for Financial Services Operations \(FSO\)]
---

# Resolve friendly fraud by using agentic AI

Resolve friendly fraud by using the friendly fraud AI agent to determine the actions to take for the disputed amount, the customer relationship, and assessing the outcome of the detection logic to evaluate the results.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent .

## About this task

When a friendly fraud task is identified, the Friendly fraud AI agent is displayed on the Now Assist panel.

-   **Tools**: The agent has access to various tools, including:
    -   Knowledge base \(KB\) articles
    -   Friendly fraud task details
    -   Previous cases of disputes
-   **Decision Making**: The human agent can follow a generated recommendation of the AI agent or make a different decision. If the human decides to deviate from the generated suggestion, they must provide a reason for their decision. The process includes declining requests, issuing credits, or proceeding with chargebacks, and communication templates for customer interaction.

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace** and open a card dispute.

    If friendly fraud is detected based on the defined rules, the **Detect friendly fraud** activity appears in the **Investigate** stage. The transaction details along with the evidence are displayed. When the AI agent is displayed, a notification appears in the Now Assist panel and an active chat is initiated.

2.  Select the Now Assist panel icon \(![now assist panel icon](../../../common/image/icon-ai-sparkle.png)\) and open the active chat for the disputed transaction.

    In the chat, the AI agent generates a recommendation for the dispute with a valid reason.

    After the AI agent generates the recommendation, a new section appears with the AI-driven recommendation in the **Resolve friendly fraud** activity.

3.  In the chat, enter the number corresponding to your decision.

4.  Interact with the AI agent to continue resolving the case.

    You can continue working in the playbook activities as you interact with the AI agent.

    For information about how to resolve friendly fraud, see [Detect friendly fraud](../../fso-card-operations/task/resolve-friendly-fraud.md) and [Customer communication](../../fso-card-operations/task/resolve-fraud-customer-communication.md).

    ![Detect friendly fraud activity showing AI-driven recommendation to decline transaction for Anu Raj's $24.00 dispute, with final action and resolution reason fields displayed.](../image/friendly-fraud-ai.png)


## Result

Based on the resolution steps that the dispute agent selects, the friendly fraud is resolved with the help of the Now Assist AI agent.

