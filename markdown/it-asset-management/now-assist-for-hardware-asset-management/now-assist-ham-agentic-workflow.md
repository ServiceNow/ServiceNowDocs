---
title: Using agentic workflows in Now Assist for HAM
description: Use the Now Assist for HAM AI agent collection to complete hardware asset sourcing tasks autonomously and optimize the asset repair workflow. These AI agents help resolve hardware requests quickly, improve the productivity of asset managers, and speed up repairs.
locale: en-US
release: yokohama
product: Now Assist for Hardware Asset Management
classification: now-assist-for-hardware-asset-management
topic_type: concept
last_updated: "2025-04-02"
reading_time_minutes: 2
keywords: [AI Agents, agentic AI]
breadcrumb: [Now Assist for Hardware Asset Management \(HAM\), Hardware Asset Management, IT Asset Management]
---

# Using agentic workflows in Now Assist for HAM

Use the Now Assist for HAM AI agent collection to complete hardware asset sourcing tasks autonomously and optimize the asset repair workflow. These AI agents help resolve hardware requests quickly, improve the productivity of asset managers, and speed up repairs.

<table id="table_gfn_c1l_w2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help manage hardware asset requests

</td><td>

Automatically fulfills hardware asset requests by either using the available local stock, or by generating transfer orders to move assets from other stockrooms, or purchase orders to acquire assets from vendors.

</td><td>

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

</td></tr><tr><td>

Help repair hardware assets

</td><td>

Automates and optimizes the repair workflow for hardware assets by validating repair tasks, guiding inventory users and technicians through troubleshooting steps, suggesting suitable repair actions, and closing relevant tasks with details.

</td><td>

-   Asset next best action AI agent
-   Evaluate asset AI agent
-   Repair asset AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are inactive. To use the agentic workflows and AI agents, follow these steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

By default, all agentic workflows and AI agent records are read only. To customize them, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and then activate the duplicated workflow.

After you duplicate the agentic workflow, you can test it in the AI Agent Studio to analyze its performance as it executes the instructions that you have defined. For details on testing your agentic workflow, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

You can implement security in AI agents and the agentic workflow using access control lists \(ACLs\) that specify which users can discover and invoke an agentic workflow or an AI agent. For more details on configuring ACLs, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

-   **[Now Assist for Hardware Asset Management \(HAM\) AI agent collection Help manage hardware asset requests agentic workflow](now-assist-ham-fulfill-req-agent-workflow.md)**  
Use the Help manage hardware asset requests agentic workflow, driven by AI agents, to handle your employees' hardware asset requests automatically. The AI agents fulfill requests by either consuming the available local stock, or by generating transfer orders or purchase orders.
-   **[Now Assist for Hardware Asset Management \(HAM\) AI agent collection Help repair hardware assets agentic workflow](now-assist-ham-repair-agent-workflow.md)**  
Use the Help repair hardware assets agentic workflow, driven by AI agents, to handle the repair requests of defective and out-of-warranty hardware assets automatically. These AI agents validate the repair tasks, provide detailed troubleshooting and repair steps, and finally close the relevant tasks after receiving user confirmation.

**Parent Topic:**[IT Asset Management](../../software-asset-management2/concept/it-asset-management.md)

