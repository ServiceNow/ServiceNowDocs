---
title: ServiceNow Vault roles
description: Learn and set up the roles necessary to use ServiceNow Vault.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/vault-roles.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: concept
last_updated: "2026-03-27"
reading_time_minutes: 1
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# ServiceNow Vault roles

Learn and set up the roles necessary to use ServiceNow Vault.

Ensure that you elevate to all these roles so you can make the most of ServiceNow Vault and its capabilities. Elevate to these roles by selecting your profile icon and then select **Elevate role**.

|Role|Description|
|----|-----------|
|`sn_vault_console.vault_console_admin`|This role is necessary to view Vault console dashboard and use guided setup in your instance. It is a combination of Data Classification admin, Data Privacy admin, and CA Admin roles for easy management of Vault console.|
|`ca_policy_admin`|This role is necessary to create, edit, and view Continuous Authentication \(CA\) policies.|
|`ca_admin`|This role is necessary to create, edit, and view CA policies, configure CA properties, and access CA dashboards and metrics.|
|`data_privacy_admin`|This role is necessary to create technique and policy configurations. Doesn't include access to create, read, or view jobs.|
|`data_privacy_processor`|This role is necessary to create, read, update, and delete user-based jobs.|
|`data_privacy_clone_processor`|This role is necessary to create, read, update, and delete dataclass-based jobs.|
|`security_admin`|This role is required to modify high security settings and manage the Access Control List. Elevate to this role to assign the `data_privacy_admin` role.|
|`sn_vault_console.vault_console_auditor`|Provides read-only access to the Vault console. Use this role to review data classification and protection policies without modifying configurations.|

**Note:** Contact your admin to assign roles related to Field Encryption like `sn_kmf.admin` and `sn_kmf.cryptographic manager`. For more information, see [Role requirements for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/fe-roles.md).

