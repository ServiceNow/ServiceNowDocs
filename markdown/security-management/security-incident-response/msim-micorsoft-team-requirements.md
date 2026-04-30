---
title: Establish MS Teams Graph connection on ServiceNow AI Platform
description: Integrate ServiceNow AI Platform instance and Microsoft Teams account by establishing a Microsoft Teams Graph connection.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Establish MS Teams Graph connection on ServiceNow AI Platform

Integrate ServiceNow AI Platform instance and Microsoft Teams account by establishing a Microsoft Teams Graph connection.

## Before you begin

If you want, you can use the same application that you created for SharePoint to establish the Microsoft Teams Graph connection.

Role required: admin, Azure admin

**Register a new application on Azure for Microsoft Teams Graph Connection**

## Procedure

1.  Sign in to [Azure](https://portal.azure.com/#home) portal using your Microsoft account.

2.  Navigate to **Azure Services** &gt; **Application Registration** &gt; **New Registration**.

3.  Enter name of the application.

    For example, Microsoft Teams Graph.

4.  Select the respective **Supported account types** option whichever is applicable to your organization.

    For example, select **Accounts in this organizational directory only \(Service Now only - Single tenant\)** option.

    **Note:** For information on supported account types, see [Register an application with the Microsoft identity platform](https://docs.microsoft.com/en-us/graph/auth-register-app-v2).

5.  Select **Web** type from drop down list under the Redirect URL.

6.  Enter ServiceNow AI Platform instance redirect URL in the allowed redirect URL field.

    For example, https://&lt;&lt;InstanceName&gt;&gt;.service-now.com/oauth\_redirect.do

7.  Click **Register** to register your new application and make sure the page is displayed with **Overview** section.


-   **[Using Certificates for authentication](../../secops-integration-major-security-incident-management/task/using-certificates-for-authentication.md)**  
Request an access token with a certificate credential.
-   **[Using Client Secret value](using-client-secret-value.md)**  
Use client secret value to configure the Graph application registry record.

**Parent Topic:**[Integrating Major Security Incident Management](../../secops-integration-major-security-incident-management/concept/integrate-with-other-applications.md)

**Related topics**  


[Integrate Major Security Incident Management with Microsoft SharePoint](../../secops-integration-major-security-incident-management/concept/integrate-msim-sharepoint.md)

[Integrate Major Security Incident Management with Microsoft Teams](../../secops-integration-major-security-incident-management/concept/integrate-teams-msim.md)

[Major Security Incident Management Conference Call Integration](../../secops-integration-major-security-incident-management/concept/integrate-msim-conference-calls.md)

