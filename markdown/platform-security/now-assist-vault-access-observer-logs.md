---
title: Summarize Access Observer logs agentic workflow
description: Use the summarize Access Observer logs agentic workflow to review and summarize access logs for a specific field, identifying access sources, users, and their roles.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-23"
reading_time_minutes: 1
keywords: [Now Assist, agentic AI]
breadcrumb: [Use agentic AI, Now Assist for Vault]
---

# Summarize Access Observer logs agentic workflow

Use the summarize Access Observer logs agentic workflow to review and summarize access logs for a specific field, identifying access sources, users, and their roles.

## Summarize Access Observer logs agentic workflow overview

Generate a summary of the user, role, and caller types that attempted to access a table column configured in Access Observer. For example, ask the agentic workflow to summarize access logs to view users who accessed a field, along with their roles and how they accessed the data.

When you install Now Assist for Vault, this agentic workflow is turned on by default.

To modify the agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

## Summarize Access Observer logs

Generate a summary of all Access Observer logs. The workflow requires that you have the following roles and elevate to them:

-   sn\_vault\_console.vault\_console\_admin
-   security\_admin

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Summarize Access Observer logs**.

**Note:** The summarize Access Observer logs agentic workflow is triggered automatically when you secure custom applications using ServiceNow Vault console dashboard. You can also invoke the agentic workflow manually in the Now Assist panel.

## AI agents used in the summarize Access Observer logs agentic workflow

|Name|Description|
|----|-----------|
|Access Observer log analyzer agent|Uses various tools to generate a summary of the user, role, and caller types that attempted to access a table column configured in Access Observer.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Use agentic AI in Now Assist for Vault](use-now-assist-vault-agentic-ai.md)

