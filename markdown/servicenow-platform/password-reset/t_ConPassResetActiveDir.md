---
title: Integrate Password Reset with your Active Directory service
description: The Password Reset application can change passwords on an Active Directory credential store. The application changes passwords by referencing an Active Directory user role with the appropriate password change privileges.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Credentials Store for Password Reset for Active Directory, Credential stores for Password Reset, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrate Password Reset with your Active Directory service

The Password Reset application can change passwords on an Active Directory credential store. The application changes passwords by referencing an Active Directory user role with the appropriate password change privileges.

## Before you begin

Role required: admin

Active Directory must have a user role with the following privileges:

Descendent User objects:

-   Reset password
-   Read/Write pwdlastset
-   Read/Write UserAccountcontrol
-   Write Account Restrictions
-   Read/Write lockouttime
-   Read MemberOf

Descendent Group objects:

-   Read Members
-   Read MemberOf

## Procedure

1.  [Install a MID Server](../../../product/mid-server/concept/mid-server-installation.md) on a Windows computer that can connect to Active Directory.

2.  [Configure the MID Server](../../../product/mid-server/concept/c_MIDServerConfiguration.md).

3.  If using the Workflow and Orchestration add-ons, in the ServiceNow instance, navigate to **Orchestration** &gt; **Credentials**.

4.  Click **New**, complete the form with the following values for the AD credential, and then click **Submit**.

    |Field|Description|
    |-----|-----------|
    |Type|Select Windows.|
    |User name|Enter your Active Directory domain user. For example, **domain\\admin**.|
    |Password|Enter your Active Directory domain user password.|
    |Applies to|Select the MID Server that you use to access the Active Directory server.|

    **Note:** If you are using Integration Hub, from the Microsoft AD Credential store, click **Microsoft AD Connection Alias** to create a new connection. To learn more, see [Set up the Microsoft AD v2 spoke](https://www.servicenow.com/docs/access?context=setup-ms-ad-v2&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).


## What to do next

Create a connection to the credential store as described in [Configure the connection to an AD credential store](config-ad-credential-store.md).

**Parent Topic:**[Credentials Store for Password Reset for Active Directory](../concept/credentials-store-AD.md)

