---
title: Field encryption with Vault module agentic workflow
description: Use the field encryption with Vault module agentic workflow to encrypt specific fields and configure secure access to users with designated roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/now-assist-vault-field-encryption-module.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI]
breadcrumb: [Use agentic AI, ServiceNow Vault]
---

# Field encryption with Vault module agentic workflow

Use the field encryption with Vault module agentic workflow to encrypt specific fields and configure secure access to users with designated roles.

## Field encryption with Vault module agentic workflow overview

Add field encryption protection and improve your security posture with the field encryption with Vault module agentic workflow.

When you install ServiceNow Otto for Vault, this agentic workflow is turned on by default.

To modify the agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Note:** To encrypt a field and create its module access policies in the same conversation, use the field encryption and auto-generate access policies agentic workflow. See [Field encryption and auto-generate access policies agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-field-encryption-access-policies.md).

## Use the field encryption with Vault module

Encrypt specific fields and configure user access. The workflow requires the following roles:

-   sn\_vault\_console.vault\_console\_admin
-   security\_admin
-   sn\_kmf.admin
-   sn\_kmf.cryptographic\_manager

Elevate to the roles that appear in the Elevate role list by selecting your profile icon and then selecting **Elevate role**.

**Note:** The `security_admin` role isn't included in the `sn_vault_console.vault_console_admin` role composition and doesn't appear in the Elevate role list. A user with the admin role must assign it through the standard user-administration process. If the workflow reports that you don't have the `security_admin` role, or that the role isn't active for your session, contact your admin. For more information, see [ServiceNow Vault roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-roles.md).

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Field Encryption with Vault module**.

**Note:** The field encryption with Vault module agentic workflow is triggered automatically when you secure custom applications using ServiceNow Vault console dashboard. You can also invoke the agentic workflow manually in the ServiceNow Otto panel.

## AI agents used in the field encryption with Vault module agentic workflow

|Name|Description|
|----|-----------|
|Vault crypto module manager agent|Uses various tools to encrypt fields and ensures that only those users with particular roles have access to those fields.|

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Parent Topic:**[Use agentic AI in ServiceNow Otto for Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/use-now-assist-vault-agentic-ai.md)

