---
title: Securing custom apps with the Vault agents agentic workflow
description: Use the securing custom apps with Vault agents agentic workflow to get recommended data classifications and available protections for a custom application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-23"
reading_time_minutes: 1
keywords: [Now Assist, agentic AI]
breadcrumb: [Use agentic AI, ServiceNow Vault]
---

# Securing custom apps with the Vault agents agentic workflow

Use the securing custom apps with Vault agents agentic workflow to get recommended data classifications and available protections for a custom application.

## Securing custom apps with Vault agents agentic workflow overview

When you install Now Assist for Vault, this agentic workflow is turned on by default.

To modify the agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

## Secure custom apps

Get data classification and data protection recommendations for a custom application. The workflow requires that you have the sn\_vault\_console.vault\_console\_admin role and elevate to it.

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Securing custom apps with Vault agents**.

**Note:** The securing custom apps with Vault agents agentic workflow is triggered automatically when you secure custom applications using ServiceNow Vault console dashboard. You can also invoke the agentic workflow manually in the Now Assist panel.

## AI agents used in the summarize Access Observer logs agentic workflow

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custom app recommendations agent

</td><td>

Uses various tools to perform the following:-   Analyzes the table schema and its metadata.
-   Uses the recommend column classifications skill to propose classifications for the data in the table.
-   Proposes available field encryption protection.
-   Proposes zero trust access and data privacy protection.

</td></tr></tbody>
</table>There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

**Parent Topic:**[Use agentic AI in Now Assist for Vault](use-now-assist-vault-agentic-ai.md)

