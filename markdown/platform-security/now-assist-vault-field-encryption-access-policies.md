---
title: Field encryption and auto-generate access policies agentic workflow
description: The field encryption and auto-generate access policies agentic workflow encrypts a table field and creates the access policies that its roles need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/now-assist-vault-field-encryption-access-policies.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI, field encryption, module access policy]
breadcrumb: [Use agentic AI, ServiceNow Vault]
---

# Field encryption and auto-generate access policies agentic workflow

The field encryption and auto-generate access policies agentic workflow encrypts a table field and creates the access policies that its roles need.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Field encryption and auto-generate access policies agentic workflow overview

After you encrypt a field, only the roles that have access to the encryption module can read the data. Identifying those roles manually means reviewing access control lists \(ACLs\), or configuring Access Observer, waiting for the logs, and building the role list from the results. If a role is missing from the list, users lose access to the data and you must add that role afterward.

This agentic workflow retrieves the roles that can read the field. You refine the list, and then the workflow creates a module access policy for each role in the final list and encrypts the field.

When you install ServiceNow Otto for Vault, this agentic workflow is turned on by default.

To modify the agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

## Use the field encryption and auto-generate access policies workflow

Encrypt a field and create the module access policies for it. The workflow requires the following roles:

-   sn\_vault\_console.vault\_console\_admin
-   security\_admin
-   sn\_kmf.admin
-   sn\_kmf.cryptographic\_manager

Select your profile icon, select **Elevate role**, and then elevate to the roles that appear in the list.

**Note:** The `security_admin` role isn't included in the `sn_vault_console.vault_console_admin` role composition and doesn't appear in the Elevate role list. A user with the admin role must assign it through the standard user-administration process. If the workflow reports that you don't have the `security_admin` role, or that the role isn't active for your session, contact your admin. For more information, see [ServiceNow Vault roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-roles.md).

To access and configure the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Field Encryption and Auto Generate Access Policies**.

**Note:** To invoke the agentic workflow, open the ServiceNow Otto panel and select **Field Encryption and Auto Generate Access Policies**. The workflow asks you to confirm each action before it runs. Nothing is encrypted and no policy is created until you confirm.

**Important:**

Elevated roles aren't evaluated when the workflow retrieves the roles that have access to the field. Grant access to elevated roles separately. The workflow states this once in each conversation.

The workflow encrypts the field with the `vault_encryption_module` encryption module and creates the module access policies against the same module.

## AI agents used in the field encryption and auto-generate access policies agentic workflow

|Name|Description|
|----|-----------|
|Field access auditor agent|Evaluates the table and field, retrieves the non-elevated user roles that have access to the field, applies the changes that you make to the role list, and returns the final list of roles.|
|Vault crypto module manager agent|Uses various tools to encrypt fields so that only users with particular roles have access to those fields.|

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Parent Topic:**[Use agentic AI in ServiceNow Otto for Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/use-now-assist-vault-agentic-ai.md)

