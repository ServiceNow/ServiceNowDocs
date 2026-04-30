---
title: Credentials Store for Password Reset for Active Directory
description: A credential store type is a set of workflows that specify how to connect to a credential store. You can connect to Password Reset Credential Stores to view the list of example credential stores that are based on the base-system types.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Credential stores for Password Reset, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Credentials Store for Password Reset for Active Directory

A credential store type is a set of workflows that specify how to connect to a credential store. You can connect to **Password Reset** **Credential Stores** to view the list of example credential stores that are based on the base-system types.

## Overview of Credentials Store for Password Reset for Active Directory

Navigate to **Password Reset** &gt; **Credential Stores** to view the list of example credential stores that are based on the base-system types. You can also use subflows and integration hub [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **[Integrate Password Reset with your Active Directory service](../task/t_ConPassResetActiveDir.md)**  
The Password Reset application can change passwords on an Active Directory credential store. The application changes passwords by referencing an Active Directory user role with the appropriate password change privileges.
-   **[Enable history check for password reset](../task/manage-history-check.md)**  
Manage the process to perform a history check for the old used passwords when users reset their passwords. The history check ensures that they don’t reuse old passwords which can lead to significant security risk.
-   **[Configure the connection to an AD credential store](../task/config-ad-credential-store.md)**  
You can create a Password Reset credential store record to configure access to your Active Directory server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.

**Parent Topic:**[Credential stores for Password Reset](c_CredentialStores.md)

**Related topics**  


[Integrate Password Reset with your Active Directory service](../task/t_ConPassResetActiveDir.md)

[Configure the connection to an AD credential store](../task/config-ad-credential-store.md)

