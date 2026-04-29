---
title: Credential stores for Password Reset
description: Credential stores hold user information such as user names and passwords that can be used as login credentials. Examples include the User table \[sys\_user\] or an Active Directory server.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Credential stores for Password Reset

Credential stores hold user information such as user names and passwords that can be used as login credentials. Examples include the User table \[sys\_user\] or an Active Directory server.

Users with the password\_reset\_admin or password\_reset\_credential\_manager role can create and modify connections to credential stores.

## Credential store types installed with the base system

A credential store type is a set of workflows that specify how to connect to a credential store. Navigate to **Password Reset** &gt; **Credential Store Types** to view the list of example credential stores that are based on the base-system types. The base system includes the following credential store types:

|Name|Description|
|----|-----------|
|Local ServiceNow Instance|Represents the current \(local\) ServiceNow instance.|

## Credential store types included in Store apps

<table id="table_mx5_cxy_bsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Microsoft AD Credential Store

</td><td>

Represents a Microsoft Active Directory credential store. See [Set up Microsoft Active Directory for Password Reset](setup-guide-ad.md#).

</td></tr><tr><td>

Microsoft Entra ID Credential Store

</td><td>

Represents a Microsoft Entra ID credential store.

</td></tr><tr><td>

Okta credential store

</td><td>

Represents an Okta credential store.

</td></tr><tr><td>

Google credential store

</td><td>

Represents a Google Directory credential store.

</td></tr></tbody>
</table>## Connection subflows for credential store types

A credential store type workflow requires a subflow that defines how to connect to the store, and can include an optional subflow that defines how to test the connection. Use the **Pwd reset – AD** and **Pwd Reset - Local** subflows as models for your custom connection workflows.

![Pwd Reset Local sub workflow](../image/PwdResetLocalServiceNowSubWorkflow.png "Pwd Reset Local sub workflow")

![Pwd connection test local SN sub workflow](../image/PwdConnectionTestLocalSNSubWorkflow.png "Pwd connection test local SN sub workflow")

## Creating a custom credential store type

You can use a credential store type as a model to create a custom type. See [Create a credential store type for Password Reset](../task/t_CreateACredentialStoreType.md).

-   **[Configure the connection to a credential store for the Password Reset processes](../task/t_CreateACredentialStore.md)**  
You create a Password Reset credential store record to configure access to your credential store server while a user is changing or resetting a password. In addition to host connection information, you can specify the password hints that users should see, restrictions on password reuse, the allowed number of failed reset attempts, and other settings.
-   **[Credentials Store for Password Reset for Active Directory](credentials-store-AD.md)**  
A credential store type is a set of workflows that specify how to connect to a credential store. You can connect to **Password Reset** **Credential Stores** to view the list of example credential stores that are based on the base-system types.
-   **[Credential Store for Password Reset for Microsoft Entra ID](credentials-store-micro-ad.md)**  
A credential store type is the set of flows to manage password and account of Microsoft Entra ID user. Navigate to **Password Reset** &gt; **Credential Stores** to view the list of example credential stores that are based on the base-system types.
-   **[Test the connection to a credential store](../task/test-cxn-to-credential-store.md)**  
You should test the connection to a credential store after you configure a new credential store or when users experience problems that might involve the connection.
-   **[Delete a connection to a credential store for Password Reset](../task/t_DeleteACredentialStore.md)**  
Important: Before you delete the connection to a credential store, check all Password Reset processes to ensure that the credential store is not in use. If the credential store is being used by a process, update the process before deleting the credential store.

**Parent Topic:**[Configure your Password Reset process](../task/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process](../reference/pwd-reset-process-recommend.md)

[Configure password expiration reminder](../task/password-reset-expiration-setup.md)

[Password Reset verifications](c_PWRVerifications.md)

[Configure your Password Reset process to auto-enroll users](../../security/task/configure-auto-enroll-for-pwd-reset.md)

[Enable users to enroll for Password Reset](../../security/task/configure-user-enroll-for-pwd-reset.md)

[Configure Password Reset properties](../task/t_SetPwdResetProps.md)

[Send email to remind users to enroll for Password Reset](../task/config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](../task/config-pwd-strength-rqmts.md)

[Specify lockout for failed login attempts](../../security/task/t_LockoutForFailedLogins.md)

[Configure Google reCAPTCHA for the password reset process](../task/t_ConfigureGoogleRecaptcha.md)

