---
title: Configure client credential flow for SMTP OAuth2 using a client id and secret
description: Configure outbound email accounts in a ServiceNow instance using a client id and secret.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Sending email using client credential flow, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Configure client credential flow for SMTP OAuth2 using a client id and secret

Configure outbound email accounts in a ServiceNow instance using a client id and secret.

## Before you begin

Create an [Microsoft Azure](https://portal.azure.com) account to configure an OAuth profile.

Complete the setup steps using your Microsoft Azure Developer account. See [Microsoft Azure product documentation](https://docs.microsoft.com/en-us/azure/) for instructions on creating and configuring custom applications.

Role required: Microsoft Azure portal administrator and admin

## Procedure

1.  Log in to the Microsoft Azure registration portal with your organization credentials.

    For more information, see the Microsoft Azure [registration portal documentation](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade).

2.  Register a new custom application by filling in the application name, supported account type, and redirect URL, and select **Register**.

    **Note:** Enter the redirect URL in the following format: `https://<instance>/oauth_redirect.do`.

    An overview of the application's basic information is displayed.

3.  Copy the client ID to a text file.

    You’ll use this client ID and the client secret value generated in the next steps to register the app as a third-party OAuth provider on your ServiceNow instance. You use the application ID as the client ID when you connect the application to your instance.

4.  Enable the **SMTP.SendAsApp** permission.

    1.  In Microsoft Entra ID, navigate to **API permissions**, and select **Add a permission**.

    2.  Select **Application Permissions**.

    3.  From the list of permissions, select **SMTP.SendAsApp**.

    4.  Select **Add permissions**.

5.  Select **Grant admin consent for &lt;your organization name&gt;**, then select **Yes** to confirm.

6.  Add a client secret.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  Select **New client secret**.

    3.  Provide a description and an expiration date, then select **Add**.

7.  Copy the value \(secret value\) to a text file.

8.  Register service principals in Microsoft Exchange using PowerShell.

    1.  Run the following commands.

        ```powershell
        Install-Module -Name ExchangeOnlineManagement -allowprerelease
        Import-module ExchangeOnlineManagement
        Connect-ExchangeOnline -Organization <tenantId>
        ```

        For more information, see [Authenticate SMTP connection using OAuth](https://learn.microsoft.com/en-us/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth)

    2.  Register an Microsoft Entra ID application's service principal by running the following command.

        ```powershell
        New-ServicePrincipal -AppId <APPLICATION_ID> -ObjectId <OBJECT_ID>
        ```

        **Important:** When registering the service principal, copy the **Object ID** from **Microsoft Entra ID** &gt; **Enterprise applications** for the registered application, and use that value in the PowerShell command.

    3.  Add permission to user email ID using the following command.

        ```powershell
        Add-MailboxPermission -Identity "<email_id>" -User <object_id> -AccessRights FullAccess 
        
        ```

9.  Navigate to **Overview** &gt; **Endpoints** and copy the **OAuth 2.0 token endpoint \(v2\)** to a text file.

    You use the **OAuth 2.0 token endpoint \(v2\)** when registering an OAuth provider. For more information, see [Register an OAuth provider](register-oauth-cred-flow.md).


## What to do next

[Register an OAuth provider](register-oauth-cred-flow.md)

**Parent Topic:**[Sending email using client credential flow](../concept/send-email-client-credential-flow.md)

