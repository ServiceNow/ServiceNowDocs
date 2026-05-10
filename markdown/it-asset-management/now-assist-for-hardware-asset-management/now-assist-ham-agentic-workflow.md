---
title: Using agentic workflows in Now Assist for HAM
description: Use the Now Assist for HAM AI agent collection to complete hardware asset sourcing tasks autonomously and optimize the asset repair workflow. These AI agents help resolve hardware requests quickly, improve the productivity of asset managers, and speed up repairs.
locale: en-US
release: australia
product: Now Assist for Hardware Asset Management
classification: now-assist-for-hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
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

</th><th>

Introduced inNow Assist for HAM version

</th></tr></thead><tbody><tr><td>

Help manage hardware asset requests

</td><td>

Automatically fulfills hardware asset requests by either using the available local stock, or by generating transfer orders to move assets from other stockrooms, or purchase orders to acquire assets from vendors.

</td><td>

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

</td><td>

Now Assist for Hardware Asset Management \(HAM\) v1.0

</td></tr><tr><td>

Help repair hardware assets

</td><td>

Automates and optimizes the repair workflow for hardware assets by validating repair tasks, guiding inventory users and technicians through troubleshooting steps, suggesting suitable repair actions, and closing relevant tasks with details.

</td><td>

-   Asset next best action AI agent
-   Evaluate asset AI agent
-   Repair asset AI agent

</td><td>

Now Assist for Hardware Asset Management \(HAM\) v2.0

</td></tr></tbody>
</table>**Important:** If the agentic workflows and AI agent records are inactive, follow the steps below to activate them

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

By default, all agentic workflows and AI agent records are read-only. To customize them, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and then activate the duplicated workflow.

After you duplicate the agentic workflow, you can test it in the AI Agent Studio to analyze its performance as it executes the instructions that you have defined. For details on testing your agentic workflow, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

You can implement security in AI agents and the agentic workflow using Access Control Lists \(ACLs\) that specify which users can discover and invoke an agentic workflow or an AI agent. For more details on configuring ACLs, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md).

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

