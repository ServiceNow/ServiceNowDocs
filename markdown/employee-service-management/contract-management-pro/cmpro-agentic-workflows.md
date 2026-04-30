---
title: Using agentic workflows in Now Assist in Contract Management
description: Use agentic workflows for Contract Management Pro to set contract renewal or termination reminders autonomously.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-03-28"
reading_time_minutes: 1
breadcrumb: [Now Assist in Contract Management, Contract Management Pro, Employee Service Management]
---

# Using agentic workflows in Now Assist in Contract Management

Use agentic workflows for Contract Management Pro to set contract renewal or termination reminders autonomously.

<table id="table_dxr_mb1_v2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Manage contract repository

</td><td>

Uses AI agents to retrieve contract details such as renewal notice period, termination notice period, or auto-renewal clause information, and determine the average lead time for similar contracts to create milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.**Note:** The agentic workflow is triggered in the Now Assist panel. It is not supported in the Virtual Agent panel.

</td><td>

-   Extract contract metadata AI agent
-   Set contract milestone reminder AI agent
-   Calculate contract lead time AI agent
-   Contract record handler AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

To modify an agentic workflow, you must first duplicate it, and then update it. For more information see:

-   [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)
-   [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

**Note:** When you modify an agentic workflow, AI agents, or tools, make sure that you update all instructions accordingly.

If you have customized the Manage contract repository agentic workflow, [update the script include to run it autonomously.](../task/cmpro-script-includ-agenticAI.md)

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

