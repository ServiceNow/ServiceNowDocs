---
title: Use agentic AI in ServiceNow Otto for Vault
description: Use the ServiceNow Otto for Vault agentic workflows to complete tasks autonomously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/use-now-assist-vault-agentic-ai.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [AI Agents, Agentic AI]
breadcrumb: [ServiceNow Vault]
---

# Use agentic AI in ServiceNow Otto for Vault

Use the ServiceNow Otto for Vault agentic workflows to complete tasks autonomously.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

|Agentic workflow name|Description|Available AI agents|
|---------------------|-----------|-------------------|
|Securing custom apps with Vault agents|Proposes data classifications and available protections for a custom application.|Custom app recommendations|
|Access observer configuration|Views, creates, deactivates, and deletes Access Observer settings for a particular field.|Access observer configuration manager|
|Summarize access observer logs|Reviews and summarizes access logs for a specific field, identifying access sources, users, and their roles.|Access observer log analyzer|
|Field encryption with Vault module|Encrypts specific fields and configure secure access to users with designated roles.|Vault crypto module manager|
|Field Encryption and Auto Generate Access Policies|Encrypts a table field and creates a module access policy for each role that needs access to the field.|Field access auditor, Vault crypto module manager|
|Classifying ServiceNow assets with Vault agents|Recommends a data class for each ServiceNow column collected into the Data Catalog.|Classify assets with ServiceNow Vault|

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## AI model providers

You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all generative AI skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md).

Agentic workflows and AI agents use the large language model configured for your instance. Unlike ServiceNow Otto for Vault skills, they don't define a default model of their own. If you change the model for your instance, the agentic workflows use the new model.

## Turn off an agentic workflow or an AI agent

Agentic workflows and AI agents aren't listed with the ServiceNow Otto for Vault skills and can't be turned on or off from the skill list. To turn one off, use AI Agent Studio, or create a policy in AI Control Tower that prevents it from running.

## Security

Enable security settings to run AI agents and agentic workflows using access control lists \(ACLs\) and user identities. You can configure and manage the ACLs in AI Agent Studio. See [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aia-security-implementation.md) for more information.

## Installed agents

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

-   **[Securing custom apps with the Vault agents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-securing-custom-apps-agents.md)**  
Use the securing custom apps with Vault agents agentic workflow to get recommended data classifications and available protections for a custom application.
-   **[Access Observer configuration agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-access-observer-config.md)**  
Use the Access Observer configuration agentic workflow to view, create, deactivate, and delete Access Observer settings for a particular field.
-   **[Summarize Access Observer logs agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-access-observer-logs.md)**  
Use the summarize Access Observer logs agentic workflow to review and summarize access logs for a specific field, identifying access sources, users, and their roles.
-   **[Field encryption with Vault module agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-field-encryption-module.md)**  
Use the field encryption with Vault module agentic workflow to encrypt specific fields and configure secure access to users with designated roles.
-   **[Field encryption and auto-generate access policies agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-field-encryption-access-policies.md)**  
The field encryption and auto-generate access policies agentic workflow encrypts a table field and creates the access policies that its roles need.

**Parent Topic:**[ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/servicenow-vault-landing.md)

