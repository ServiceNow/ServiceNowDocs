---
title: Configure an OAuth profile to use certificates for authentication with Microsoft Azure
description: Configure an OAuth application profile to authenticate using certificates.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reading email using Microsoft Graph, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Configure an OAuth profile to use certificates for authentication with Microsoft Azure

Configure an OAuth application profile to authenticate using certificates.

## Before you begin

Create an [Microsoft Azure](https://portal.azure.com) account to configure OAuth profile.

Complete the set up steps using your Microsoft Azure Developer account. See the [Microsoft Azure product documentation](https://docs.microsoft.com/en-us/azure/) for instructions on creating and configuring custom applications.

Role required: admin and Microsoft Azure portal administrator

## Procedure

1.  Log in to the Microsoft Azure registration profile with your organization credentials.

    For more information, see the Microsoft Azure [registration portal documentation](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade).

2.  Register a new custom application by filling in the application name, supported account type, and redirect URL, and then select **Register**.

    **Note:** Enter the redirect URL in the following format: `https://<instance>/oauth_redirect.do`.

    An overview of the application's basic information is displayed.

3.  Copy the client ID to a text file.

    You will use this ID and the secret value generated in the next steps to register the app as a third-party OAuth provider on your ServiceNow instance. You use the application ID as the client ID when you connect the application to ServiceNow.

4.  Enable the **Mail.ReadWrite** permission.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **API permissions**.

    2.  Select **Add a permission**.

    3.  Click the Microsoft Graph tile.

    4.  Select **Application Permissions**.

    5.  In the **Select permissions** field, enter `Mail.ReadWrite`.

    6.  Select the **Mail.ReadWrite** check box.

    7.  Select **Add permissions**.

5.  Select **Grant admin consent for &lt;your organization name&gt;**.

6.  Select **Yes** to confirm.

7.  Upload the certificate

    1.  In Microsoft Azure, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  Select **upload certificate**.

    3.  Provide a description, a start date, and an expiration date and upload the certificate.

8.  Copy the client ID and directory ID to a text file.

9.  Navigate to **Overview** &gt; **Endpoints** and copy the **OAuth 2.0 token endpoint \(v2\)** to a text file.


## What to do next

[Configure a JWT provider](configure-jwt-provider.md)

-   **[Configure a JWT provider](configure-jwt-provider.md)**  
Configure a JWT provider on the ServiceNow AI Platform to configure an OAuth application profile to authenticate using certificates.
-   **[Generate a SHA-1 thumbprint](generate-thumbprint.md)**  
Generate a SHA-1 thumbprint using the JWT provider's sys\_id and JKS certificate's sys\_id and certificate's alias to be added to the GraphCertificateOAuthTemplate script.
-   **[Create an OAuth API script](oauth-api-script.md)**  
Create and duplicate an OAuth API script for application registry.

**Parent Topic:**[Reading email using Microsoft Graph](../concept/read-email-using-ms-graph.md)

**Related topics**  


[Activate Email - Support for Email Processing by Microsoft Graph API](ms-graph-plugin.md)

[Configure an OAuth profile to use a client ID and secret for token generation](microsoft-graph.md#)

[Create an email account for Microsoft Graph \(receive\)](create-email-account-ms-graph.md)

