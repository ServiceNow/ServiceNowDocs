---
title: Using agentic workflows in Now Assist in Contract Management
description: Use agentic workflows in Contract Management Pro to extract metadata and obligations from signed contracts, and set reminders for contract renewals or termination.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [AI agents in CM Pro, AI agents in contracts, AI agents in contract management pro, agentic workflows in contract management pro, agentic workflows in contracts, agentic workflows in CM Pro]
breadcrumb: [Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Using agentic workflows in Now Assist in Contract Management

Use agentic workflows in Contract Management Pro to extract metadata and obligations from signed contracts, and set reminders for contract renewals or termination.

<table id="table_dxr_mb1_v2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Manage contract repository

</td><td>

Uses an AI agent to extract key metadata and obligations from a signed contract, and calculate the contract reminder date by analyzing the contract end date, auto-renewal clause, and notice period for contract renewal or termination. The playbook in the contract record enables users to review AI extracted metadata and obligations to update the contract repository with extracted metadata, and create obligation records, respectively. Users can also set reminders for contract renewal or termination.**Note:** The agentic workflow is triggered in the Now Assist panel. It is not supported in the Virtual Agent panel.

</td><td>

Contract repository AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

To modify an agentic workflow, you must first duplicate it, and then update it. For more information, see:

-   Duplicate an agentic workflow
-   Create an agentic workflow
-   Modify an agentic workflow

**Note:** When you modify an agentic workflow, AI agents, or tools, make sure that you update all instructions accordingly.

If you have customized the manage contract repository agentic workflow, [update the script include to run it autonomously.](../task/cmpro-script-includ-agenticAI.md)

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see Large language models on the ServiceNow AI Platform®.

