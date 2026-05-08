---
title: Use agentic AI in Now Assist for Vault
description: Use the Now Assist for Vault agentic workflows to complete tasks autonomously.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-23"
reading_time_minutes: 2
keywords: [AI Agents, Agentic AI]
breadcrumb: [ServiceNow Vault]
---

# Use agentic AI in Now Assist for Vault

Use the Now Assist for Vault agentic workflows to complete tasks autonomously.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see ServiceNow product tiers.

|Agentic workflow name|Description|Available AI agents|
|---------------------|-----------|-------------------|
|Securing custom apps with Vault agents|Proposes data classifications and available protections for a custom application.|Custom app recommendations|
|Access observer configuration|Views, creates, deactivates, and deletes Access Observer settings for a particular field.|Access observer configuration manager|
|Summarize access observer logs|Reviews and summarizes access logs for a specific field, identifying access sources, users, and their roles.|Access observer log analyzer|
|Field encryption with Vault module|Encrypts specific fields and configure secure access to users with designated roles.|Vault crypto module manager|

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see Now Assist skills, agents, and agentic workflows on by default.

## AI model providers

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in AI Control Tower to define which options are available, then set the skill-level preferences in the Now Assist Admin console. For more information, see Large language models on the ServiceNow AI Platform®.

## Security

Enable security settings to run AI agents and agentic workflows using access control lists \(ACLs\) and user identities. You can configure and manage the ACLs in AI Agent Studio. See Implement access control in Now Assist AI agents for more information.

## Installed agents

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

-   **[Securing custom apps with the Vault agents agentic workflow](now-assist-vault-securing-custom-apps-agents.md)**  
Use the securing custom apps with Vault agents agentic workflow to get recommended data classifications and available protections for a custom application.
-   **[Access Observer configuration agentic workflow](now-assist-vault-access-observer-config.md)**  
Use the Access Observer configuration agentic workflow to view, create, deactivate, and delete Access Observer settings for a particular field.
-   **[Summarize Access Observer logs agentic workflow](now-assist-vault-access-observer-logs.md)**  
Use the summarize Access Observer logs agentic workflow to review and summarize access logs for a specific field, identifying access sources, users, and their roles.
-   **[Field encryption with Vault module agentic workflow](now-assist-vault-field-encryption-module.md)**  
Use the field encryption with Vault module agentic workflow to encrypt specific fields and configure secure access to users with designated roles.

**Parent Topic:**[ServiceNow Vault](../../vault/reference/servicenow-vault-landing.md)

