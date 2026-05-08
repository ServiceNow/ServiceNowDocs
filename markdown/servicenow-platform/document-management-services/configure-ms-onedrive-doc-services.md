---
title: Setup Microsoft OneDrive for Document Services
description: Integrate the ServiceNow instance and Microsoft OneDrive for Document Services by creating a custom OAuth application in Document Services to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft OneDrive integration with Document Services, Integrate with Document Services, Multi Provider Document Services Framework, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Setup Microsoft OneDrive for Document Services

Integrate the ServiceNow instance and Microsoft OneDrive for Document Services by creating a custom OAuth application in Document Services to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Set up and connect Microsoft Entra ID Spoke, see Set up Microsoft Entra ID spoke and Microsoft OneDrive Spoke.

Microsoft OneDrive requirements:

-   Microsoft OneDrive account
-   [Microsoft Azure](https://portal.azure.com) account
-   Microsoft OneDrive tenant administrator credentials

Role required: admin

## About this task

Complete these steps from your [Azure](https://docs.microsoft.com/en-us/azure/) Developer account. See the [Azure](https://docs.microsoft.com/en-us/azure/) product documentation for instructions on creating and configuring custom applications.

## Procedure

1.  Log in to the Microsoft Azure registration portal with your organization credentials.

    For more information, see the Microsoft documentation on the [Microsoft Azure App registration portal](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade).

2.  Register a new custom application.

    1.  Provide the application name and the supported account type.

    2.  Select **Register**.

    3.  Enter the redirect URL in the following format: `https://<instance>.service-now.com/oauth_redirect.do`.

    An overview of the application's basic information is Displayed.

3.  Copy the application ID to a text file.

    You will use this ID and the client secret generated in the next step to register the app as a third-party OAuth provider on your ServiceNow instance. The application ID is the client ID when you connect the application to your ServiceNow instance.

4.  Add a client secret.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  Provide a description and an expiration date.

    3.  Select **Add**.

5.  Enable the permissions you want the application to support.

    For more information, see the [Microsoft Graph permissions reference](https://docs.microsoft.com/en-us/graph/permissions-reference) documentation.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **API permissions**.

    2.  Click the Microsoft Graph tile.

    3.  Select the delegated or application permissions that the application supports.

        Delegated permissions enable the application to access the API as a signed-in user.

        Application permissions enable the application to run as a background service or daemon without a signed-in user.

        You must mention these API permissions in the **OAuth Entity scopes** tab while configuring the application registry.

    4.  Ensure that required API permissions are provided for your custom app.

        |Name|OAuth scope|
        |----|-----------|
        |Files.Read|Files.Read|
        |Files.Read.All|Files.Read.All|
        |offline\_access|offline\_access|
        |Files.ReadWrite|Files.ReadWrite|
        |Files.ReadWrite.All|Files.ReadWrite.All|
        |AuditLog.Read.All|AuditLog.Read.All|
        |Directory.AccessAsUser.All|Directory.AccessAsUser.All|
        |Directory.Read.All|Directory.Read.All|
        |User.Read|User.Read|

    5.  Select **Add permissions**.


## What to do next

[Register Microsoft OneDrive as an OAuth provider for Document Services](register-ms-onedrive-oauth-provider.md)

**Parent Topic:**[Microsoft OneDrive integration with Document Services](../concept/one-drive-integration.md)

