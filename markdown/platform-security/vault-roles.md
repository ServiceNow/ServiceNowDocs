---
title: ServiceNow Vault roles
description: Learn and set up the roles necessary to use ServiceNow Vault.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/vault-roles.html
release: australia
topic_type: concept
last_updated: "2026-07-08"
reading_time_minutes: 1
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# ServiceNow Vault roles

Learn and set up the roles necessary to use ServiceNow Vault.

To use ServiceNow Vault and its capabilities, elevate to the roles in this table by selecting your profile icon and then selecting **Elevate role**. The `security_admin` role is not available in the Elevate role list; a user with the admin role must assign it through the standard user-administration process.

|Role|Description|
|----|-----------|
|`sn_vault_console.vault_console_admin`|This role is necessary to view the Vault console dashboard and use guided setup in your instance. It is a combination of Data Classification admin, Data Privacy admin, and CA admin roles for management of the Vault console. On the Vault console dashboard, this role provides read-only access to all the tool charts and available protection configurations.|
|`ca_policy_admin`|This role is necessary to create, edit, and view Continuous Authentication \(CA\) policies.|
|`ca_admin`|This role is necessary to create, edit, and view CA policies, configure CA properties, and access CA dashboards and metrics.|
|`data_privacy_admin`|This role is necessary to create technique and policy configurations. Doesn't include access to create, read, or view jobs.|
|`data_privacy_processor`|This role is necessary to create, read, update, and delete user-based jobs.|
|`data_privacy_clone_processor`|This role is necessary to create, read, update, and delete dataclass-based jobs.|
|`security_admin`|This role is required to modify high-security settings and manage the Access Control List \(ACL\). On the **Protect existing data** screen in guided setup, this role is required to create or modify field encryption configurations.|
|`sn_vault_console.vault_console_auditor`|Provides read-only access to the Vault console. Use this role to review data classification and protection policies without modifying configurations. On the **Protect existing data** screen in guided setup, this role provides read-only access to available protection configurations.|

**Note:** The `security_admin` role was removed from the `sn_vault_console.vault_console_admin` role composition for security reasons. It no longer appears in the Elevate role list. A user with the admin role must assign `security_admin` through the standard user-administration process. To assign roles related to Field Encryption such as `sn_kmf.admin` and `sn_kmf.cryptographic manager`, contact your admin. For more information, see [Role requirements for Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/fe-roles.md).

