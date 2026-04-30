---
title: ACH dispute AI agents overview
description: Agentic AI streamlines ACH dispute resolution by automating merchant analysis, Nacha eligibility checks, ACH dispute return recommendations, and communications with customers or ODFI \(Originating Depository Financial Institution\). This solution enhances efficiency, accuracy, and conformance, enabling financial institutions to resolve ACH disputes faster, reduce errors, and improve customer satisfaction.
locale: en-US
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2025-10-19"
reading_time_minutes: 3
breadcrumb: [AI agents in FSO, Use agentic AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# ACH dispute AI agents overview

Agentic AI streamlines ACH dispute resolution by automating merchant analysis, Nacha eligibility checks, ACH dispute return recommendations, and communications with customers or ODFI \(Originating Depository Financial Institution\). This solution enhances efficiency, accuracy, and conformance, enabling financial institutions to resolve ACH disputes faster, reduce errors, and improve customer satisfaction.

The key features of agentic AI in ACH dispute resolution are:

-   Investigate merchant credibility: Agentic AI can evaluate merchants by checking their web credibility and past dispute history in the context of the disputed transaction reason, providing a comprehensive view of their reliability.
-   Determine eligibility: AI agents can determine eligibility according to Nacha operating guidelines for relevant ACH return codes, ensuring conformance and reducing errors.
-   Recommend action: By analyzing the outcomes of AI agents and similar past disputes, agentic AI can recommend the best course of action for resolving disputes.
-   Automated communication: Agentic AI can communicate with customers or merchants' banks depending on the action taken, streamlining the dispute resolution process.

The key agents for ACH dispute resolution are.

-   **Merchant analysis for disputes AI agent**: Assesses merchant credibility in the context of the disputed transaction's reason, using web intelligence and internal dispute history, eliminating manual research.
-   **Nacha operating guidelines check AI agent**: Verifies chargeback eligibility of transactions against Nacha operating guidelines without relying on complex system rules.
-   **ACH dispute return recommendation AI agent**: Combines merchant risk analysis and Nacha eligibility checks to provide clear, consistent recommendations, whether to file a return, deny the claim, or request more documentations. Thus helping dispute agents to make faster, more accurate, and conforming decisions.
-   **Dispute communication AI agent**: Automates and streamlines communication with customers and ODFIs throughout the ACH dispute life cycle. The agent generates and sends timely, conforming, and personalized notifications for all dispute outcomes: returns, denials, or documentation requests, thus ensuring clarity, conformance, and faster resolution.

## ACH disputes workflow with AI agents

The following diagram illustrates the workflow in ACH disputes with the AI agents.![ACH disputes workflow](../image/now-assist-ach-disputeworkflw.png)

For information about the workflow in ACH disputes, see [Processing an ACH dispute](../../fso-card-operations/concept/process-dispute-ach.md).

## Access the AI agents

To access the agents:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **AI Agents** and then select appropriate agent.

    The **Define the specialty** screen is displayed.

3.  Select **Add tools and information** to review the AI agent's capabilities by adding tools and information sources, configuring flow actions, and setting up record operations.
4.  The **Define trigger** option enables you to define triggers for the AI agent. By default, the trigger is deactivated and must be enabled.

    **Note:** When a dispute agent is assigned to a case, all related tasks are automatically assigned to that agent, and the AI agents are invoked to assist. If this configuration isn’t enabled, the dispute agent must manually assign each task to themselves by selecting **Assigned to Me** on a specific task, to invoke the AI agent.

5.  In the **Define availability** screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

## Role masking

Required roles: sn\_bom\_credit\_card.dispute\_agent\_connector, sn\_bom\_credit\_card.dispute\_agent, and now\_assist\_panel\_user.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of AI agents during tool execution. AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

In the data access settings, you must also add the necessary roles to the following FSO AI agents:

-   Merchant analysis for disputes AI agent
-   Nacha operating guidelines check AI agent
-   ACH dispute return recommendation AI agent
-   Dispute communication AI agent

**Parent Topic:**[Standalone AI agents in FSO](ai-agents-fso.md)

