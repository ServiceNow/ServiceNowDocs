---
title: Integrate Password Reset with your Active Directory service
description: The Password Reset application can change passwords on an Active Directory credential store. The application changes passwords by referencing an Active Directory user role with the appropriate password change privileges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/password-reset/t\_ConPassResetActiveDir.html
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Credentials Store for Password Reset for Active Directory, Credential stores for Password Reset, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Integrate Password Reset with your Active Directory service

The Password Reset application can change passwords on an Active Directory credential store. The application changes passwords by referencing an Active Directory user role with the appropriate password change privileges.

## Before you begin

Role required: admin

Before you begin, make sure the following prerequisites are met:

-   [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-installation.md) installed and running on a Windows computer that can connect to an Active Directory.
-   -   Reset password
-   Read/Write pwdlastset
-   Read/Write UserAccountcontrol
-   Write Account Restrictions
-   Read/Write lockouttime
-   Read MemberOf

Descendent Group objects:

-   Read Members
-   Read MemberOf

## Procedure

1.  [Install a MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-installation.md) on a Windows computer that can connect to Active Directory.

2.  [Configure the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/c_MIDServerConfiguration.md).

3.  If using the Workflow and Orchestration add-ons, in the ServiceNow instance, navigate to **Orchestration** &gt; **Credentials**.

4.  Click **New**, complete the form with the following values for the AD credential, and then click **Submit**.

    |Field|Description|
    |-----|-----------|
    |Type|Select Windows.|
    |User name|Enter your Active Directory domain user. For example, **domain\\admin**.|
    |Password|Enter your Active Directory domain user password.|
    |Applies to|Select the MID Server that you use to access the Active Directory server.|

    **Note:** If you are using Integration Hub, from the Microsoft AD Credential store, click **Microsoft AD Connection Alias** to create a new connection. To learn more, see Set up the Microsoft AD v2 spoke.


## What to do next

Create a connection to the credential store as described in [Configure the connection to an AD credential store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/password-reset/config-ad-credential-store.md).

**Parent Topic:**[Credentials Store for Password Reset for Active Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/password-reset/credentials-store-AD.md)

