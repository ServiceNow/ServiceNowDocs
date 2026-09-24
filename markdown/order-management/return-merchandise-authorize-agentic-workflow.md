---
title: RMA AI agentic workflow
description: Automate and streamline Return Merchandise Authorization \(RMA\) case handling, reducing manual intervention, improving responsiveness, and ensuring consistent decision-making.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/return-merchandise-authorize-agentic-workflow.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Order operations apps, Configure, Sales Customer Relationship Management]
---

# RMA AI agentic workflow

Automate and streamline Return Merchandise Authorization \(RMA\) case handling, reducing manual intervention, improving responsiveness, and ensuring consistent decision-making.

## RMA AI agent Overview

Use the **RMA AI** agentic workflow for:

-   **Case creation**: Initiate RMA cases through the business portal or virtual agent by providing product details and return reasons. The agent fetches install base items and validates them automatically.
-   **Case processing**: The support assistant performs entitlement and warranty checks, proposes resolutions, and communicates with the customer for approval and next steps.
-   **Proactive updates**: The agent provides updates on case status, entitlements information, and case summary ensuring customers are informed throughout the process.
-   **Customer interaction**: Customers can interact via chat, select install base items, and specify reasons for return, replacement, or repair. The AI agent guides users through the process and offers recommendations if entitlements are not available.
-   **Live agent handoff**: If required, the agent can transfer the case to a live agent for further assistance.
-   **Role-based actions**: Both the requester and fulfiller personas will have access to create and process the RMA Case using the RMA AI Assistant.

To modify the **RMA AI** agentic workflow [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements. You can activate the agentic workflow template by making triggers active and setting the display settings to include the ServiceNow Otto panel.

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

## RMA AI agents

The following table lists the **RMA** AI agents.

**Important:** In the **Define availability** screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|RMA Assistant|Manages case intake, processing, entitlement verification, customer communication, and proactive follow-ups.|

## Roles required to create a workflow

The roles required to activate and access the workflow are as follows.

|Roles|Responsibilities|
|-----|----------------|
|RMA Fulfiller|Interact with RMA AI Agent using NAP panel.|
|User|Interact with RMA AI Agent using ServiceNow Otto for Virtual Agent.|

**Related topics**  


[Activating the RMA Agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/activating-the-rma-agentic-workflows.md)

