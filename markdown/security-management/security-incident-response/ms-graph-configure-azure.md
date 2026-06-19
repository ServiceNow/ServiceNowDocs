---
title: Configure the Microsoft Azure portal
description: To retrieve security alerts for an application available in the Microsoft Azure tenant using the Microsoft Graph Security API, you must register the application in the Microsoft Azure portal and grant security event read and write access to the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/ms-graph-configure-azure.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up instance, Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure the Microsoft Azure portal

To retrieve security alerts for an application available in the Microsoft Azure tenant using the Microsoft Graph Security API, you must register the application in the Microsoft Azure portal and grant security event read and write access to the application.

## Before you begin

Role required:

-   Application Developer: Required for registering the application.
-   Tenant Administrator: The Microsoft Azure tenant administrator must grant permissions to the application by making a call to the admin consent endpoint.

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Enter **App registrations** in the **Search** box.

3.  Select **New registration**.

4.  Enter a name for your application and the redirect URI, for example http://localhost and click **Register**.

    The Redirect URI is used while providing admin consent for the application.

5.  In the App registrations page, select the application you have registered, for example Graph Security Demo.

6.  Under **Manage**, select **Certificates &amp; secrets**.

    \[Omitted image "ms-graph-azure-config.png"\] Alt text: MIicrosoft Azure portal configuration

7.  Select **New client secret** to create a client secret.

    Copy the client secret and save it as it will not be visible later. In case you forgot the client secret you can generate a new client secret.

    **Note:** If you forget the client secret, you can generate a new one by following the instructions in steps 4 and 5.

8.  Select **View API Permissions** in the Overview page.

9.  Add new Application level API permissions for SecurityAlert.ReadWrite.All security events.

    \[Omitted image "ms-graph-azure-config-1.png"\] Alt text: Microsoft Graph Security API configuration: security events

10. Grant admin consent for the newly added API permissions.

    For more information, see the [Microsoft Graph Permissions reference](https://docs.microsoft.com/en-us/graph/permissions-reference) Microsoft Graph permission model.

    \[Omitted image "ms-graph-azure-config-2.png"\] Alt text: Microsoft Graph Security API configuration: grant admin consent

11. Log in as a tenant administrator and provide consent for the application.

    The steps are given below:

    1.  Navigate to the following URL: [https://login.microsoftonline.com/common/adminconsent?client\_id=APPLICATION\_ID&amp;state=12345](https://docs.microsoft.com/en-us/graph/permissions-reference)

        Enter the APPLICATION\_ID of the application that you have registered.

12. Select **Accept** to accept permissions requested by the application created above.

    You can then use the application to read security events. See the [Microsoft Graph Security Authorization](https://docs.microsoft.com/en-us/graph/permissions-reference) documentation for more details.


