---
title: Configure client credential flow for SMTP OAuth2 using certificate-based authentication
description: Configure an OAuth application profile to authenticate using certificates for outbound email.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Send email using client credential flow, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure client credential flow for SMTP OAuth2 using certificate-based authentication

Configure an OAuth application profile to authenticate using certificates for outbound email.

## Before you begin

Create an [Microsoft Azure](https://portal.azure.com) account to configure an OAuth profile.

Complete the setup steps using your Microsoft Azure Developer account. See [Microsoft Azure product documentation](https://docs.microsoft.com/en-us/azure/) for instructions on creating and configuring custom applications.

Role required: Microsoft Azure portal administrator and admin

## Procedure

1.  Log in to the Microsoft Azure registration profile with your organization credentials.

    For more information, see the Microsoft Azure [registration portal documentation](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade).

2.  Register a new custom application by filling in the application name, supported account type, and redirect URL, and then select **Register**.

    **Note:** Enter the redirect URL in the following format: `https://<instance>/oauth_redirect.do`.

    An overview of the application's basic information is displayed.

3.  Copy the client ID to a text file.

    You’ll use this client ID and the secret value generated in the next steps to register the app as a third-party OAuth provider on your ServiceNow instance. You use the application ID as the client ID when you connect the application to ServiceNow.

4.  Enable the **SMTP.SendAsApp** permission.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **API permissions**.

    2.  Select **Add a permission**.

    3.  Select the Microsoft Office 365 tile.

    4.  Select **Application Permissions**.

    5.  In the **Select permissions** field, enter `SMTP.SendAsApp`.

    6.  Select the **SMTP.SendAsApp** check box.

    7.  Select **Add permissions**.

5.  Select **Grant admin consent for &lt;organization name&gt;**, then select **Yes** to confirm.

6.  Upload the certificate.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  Select **upload certificate**.

    3.  Provide a description, a start date, and an expiration date, then upload the certificate.

7.  Copy the client ID and directory ID to a text file.

8.  Register service principals in Microsoft Exchange using PowerShell.

    1.  Run the following commands.

        ```powershell
        Install-Module -Name ExchangeOnlineManagement -allowprerelease
        Import-module ExchangeOnlineManagement
        Connect-ExchangeOnline -Organization <tenantId>
        ```

        For more information, see [Authenticate SMTP connection using OAuth](https://learn.microsoft.com/en-us/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth)

    2.  Register an Microsoft Azure AD application's service principal by running the following command.

        ```powershell
        New-ServicePrincipal -AppId <APPLICATION_ID> -ObjectId <OBJECT_ID>
        ```

        **Important:** For the OBJECT\_ID value, go to **Overview** &gt; **Managed applications in local directory** and copy the Object ID.

    3.  Add permission to user email ID using the following command.

        ```powershell
        Add-MailboxPermission -Identity "<email_id>" -User <object_id> -AccessRights FullAccess 
        
        ```

9.  Navigate to **Overview** &gt; **Endpoints** and copy the **OAuth 2.0 token endpoint \(v2\)** to a text file.

    You use the **OAuth 2.0 token endpoint \(v2\)** when configuring a JWT provider. For more information, see [Configure a JWT provider](config-jwt-credential-flow.md).


## What to do next

[Configure a JWT provider](config-jwt-credential-flow.md)

-   **[Configure a JWT provider](config-jwt-credential-flow.md)**  
Configure a JWT provider on the ServiceNow AI Platform to configure an OAuth application profile to authenticate using certificates.
-   **[Generate SHA-1 thumbprint](generate-sha-1-thumbprint.md)**  
Generate an SHA-1 thumbprint using the JWT provider's sys\_id, the Java Key Store \(JKS\) certificate's sys\_id, and the JKS certificate's alias to the GraphCertificateOAuthTemplate script.
-   **[Create an OAuth API script](create-oauth-api-script-cred-flow.md)**  
Create and duplicate an OAuth API script for application registry.

**Parent Topic:**[Send email using client credential flow](../concept/send-email-client-credential-flow.md)

