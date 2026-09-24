---
title: Access Observer configuration agentic workflow
description: Use the Access Observer configuration agentic workflow to view, create, deactivate, and delete Access Observer settings for a particular field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/now-assist-vault-access-observer-config.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, agentic AI]
breadcrumb: [Use agentic AI, ServiceNow Vault]
---

# Access Observer configuration agentic workflow

Use the Access Observer configuration agentic workflow to view, create, deactivate, and delete Access Observer settings for a particular field.

## Access Observer configuration agentic workflow overview

Access Observer helps you monitor the people and processes that access data on your instance. Use the Access Observer configuration agentic workflow to modify Access Observer settings to track access across your enterprise.

When you install ServiceNow Otto for Vault, this agentic workflow is turned on by default.

To modify the agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

## Configure Access Observer

Configure Access Observer settings to track data access. The workflow requires the following roles:

-   sn\_vault\_console.vault\_console\_admin
-   security\_admin

Elevate to the roles that appear in the Elevate role list by selecting your profile icon and then selecting **Elevate role**.

**Note:** The `security_admin` role isn't included in the `sn_vault_console.vault_console_admin` role composition and doesn't appear in the Elevate role list. A user with the admin role must assign it through the standard user-administration process. If the workflow reports that you don't have the `security_admin` role, or that the role isn't active for your session, contact your admin. For more information, see [ServiceNow Vault roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-roles.md).

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Access Observer configuration**.

**Note:** The Access Observer configuration agentic workflow is triggered automatically when you secure custom applications using ServiceNow Vault console dashboard. You can also invoke the agentic workflow manually in the ServiceNow Otto panel.

## AI agents used in the Access Observer configuration agentic workflow

|Name|Description|
|----|-----------|
|Access Observer configuration manager agent|Uses various tools to view, create, deactivate, and delete Access Observer settings for a particular field.|

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Parent Topic:**[Use agentic AI in ServiceNow Otto for Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/use-now-assist-vault-agentic-ai.md)

