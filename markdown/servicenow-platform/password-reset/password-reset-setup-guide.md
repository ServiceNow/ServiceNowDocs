---
title: Setting up Password Reset
description: The Password Reset application is active by default and includes example verifications. The base system enables connections only to the local ServiceNow instance credential store types.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Setting up Password Reset

The Password Reset application is active by default and includes example verifications. The base system enables connections only to the local ServiceNow instance credential store types.

## Requirements

Role required: admin

**Note:** The Password Reset application is not available during an upgrade.

## Active and available plugins

-   To enable connections to Active Directory \(AD\) and Remote \(SOAP\) ServiceNow Instance credential store types, activate the Password Reset Windows App \(Password Reset Orchestration\) \(com.glideapp.password\_reset\_desktop\) plugin and Microsoft AD for Password Reset store app. No other components are installed. Orchestration is available as a separate subscription. See [Request the Password Reset Windows App plugin](../task/t_ActPassRstOrchAddOn.md).
-   To enable connections to Microsoft Entra ID Integration for Password Reset, [Integrate Microsoft Entra ID Integration with Password Reset](../task/Config-credential-store-micro-azure.md) and [Configure the connection to Microsoft Entra ID Credential Store](../task/config-azure-credential-store.md).

## Next steps

Plan and configure the Password Reset processes for your organization. See the [Configuring Password Reset](password-reset-admin-guide.md).

