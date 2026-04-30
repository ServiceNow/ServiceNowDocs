---
title: RMA AI agentic workflow
description: Automate and streamline Return Material Authorization \(RMA\) case handling, reducing manual intervention, improving responsiveness, and ensuring consistent decision-making.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-02-16"
reading_time_minutes: 2
breadcrumb: [Use, Now Assist for Order Management]
---

# RMA AI agentic workflow

Automate and streamline Return Material Authorization \(RMA\) case handling, reducing manual intervention, improving responsiveness, and ensuring consistent decision-making.

## RMA AI Agent Overview

Install the Customer Service RMA AI Agents plugin \(app-csm-rma-case-ai-agent\) to use the **RMA AI** agentic workflow.

-   **Case creation**: Initiate RMA cases through the business portal or virtual agent by providing product details and return reasons. The agent fetches install base items and validates them automatically.
-   **Case processing**: The support assistant performs entitlement and warranty checks, proposes resolutions, and communicates with the customer for approval and next steps.
-   **Proactive updates**: The agent provides updates on case status, entitlements information, case summary, ensuring customers are informed throughout the process.
-   **Customer interaction**: Customers can interact via chat, select install base items, and specify reasons for return, replacement, or repair. The AI agent guides users through the process and offers recommendations if entitlements are not available.
-   **Live agent handoff**: If required, the agent can transfer the case to a live agent for further assistance.
-   **Role-based actions**: Both the requester persona and the Fullfiller persona will have access to create and process the RMA Case using the RMA AI Assistant.

To modify the **RMA AI** agentic workflow [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements. You can activate the agentic workflow template by making triggers active and setting the display settings to include the Now Assist panel.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## RMA AI agents

The following table lists the **RMA** AI agents.

**Important:** In the **Define availability** screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|RMA Support Assistant|Manages case processing, entitlement verification, customer communication, and proactive follow-ups.|

## Roles required to create a workflow

The roles required to activate and access the workflow are as follows.

|Roles|Responsibilities|
|-----|----------------|
|RMA Fulfiller|Interact with RMA AI Agent using the NAP panel.|
|User|Interact with RMA AI Agent using Now Assist in Virtual Agent. \(NAVA\)|

## Activating the agentic workflow and triggers

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **RMA AI Agentic workflow**.

The workflow is active by default. To enable it in different channels:

1.  In the RMA AI Agentic workflow, select **Define trigger**.
2.  Select the agentic workflow trigger in the list.
3.  On the Edit trigger form, set **Active** to true.

