---
title: Summarize Access Observer logs agentic workflow
description: Use the summarize Access Observer logs agentic workflow to review and summarize access logs for a specific field, identifying access sources, users, and their roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/now-assist-vault-access-observer-logs.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI]
breadcrumb: [Use agentic AI, ServiceNow Vault]
---

# Summarize Access Observer logs agentic workflow

Use the summarize Access Observer logs agentic workflow to review and summarize access logs for a specific field, identifying access sources, users, and their roles.

## Summarize Access Observer logs agentic workflow overview

Generate a summary of the user, role, and caller types that attempted to access a table column configured in Access Observer. For example, ask the agentic workflow to summarize access logs to view users who accessed a field, along with their roles and how they accessed the data.

When you install ServiceNow Otto for Vault, this agentic workflow is turned on by default.

To modify the agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

## Summarize Access Observer logs

Generate a summary of all Access Observer logs. The workflow requires the following roles:

-   sn\_vault\_console.vault\_console\_admin
-   security\_admin

Elevate to the roles that appear in the Elevate role list by selecting your profile icon and then selecting **Elevate role**.

**Note:** The `security_admin` role isn't included in the `sn_vault_console.vault_console_admin` role composition and doesn't appear in the Elevate role list. A user with the admin role must assign it through the standard user-administration process. If the workflow reports that you don't have the `security_admin` role, or that the role isn't active for your session, contact your admin. For more information, see [ServiceNow Vault roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-roles.md).

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Summarize Access Observer logs**.

**Note:** The summarize Access Observer logs agentic workflow is triggered automatically when you secure custom applications using ServiceNow Vault console dashboard. You can also invoke the agentic workflow manually in the ServiceNow Otto panel.

## AI agents used in the summarize Access Observer logs agentic workflow

|Name|Description|
|----|-----------|
|Access Observer log analyzer agent|Uses various tools to generate a summary of the user, role, and caller types that attempted to access a table column configured in Access Observer.|

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Parent Topic:**[Use agentic AI in ServiceNow Otto for Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/use-now-assist-vault-agentic-ai.md)

