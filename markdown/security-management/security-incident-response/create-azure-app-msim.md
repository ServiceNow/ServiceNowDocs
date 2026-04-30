---
title: Register a new application at Azure portal for SharePoint connections
description: Register a new application at Azure portal for Microsoft SharePoint integration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-04-01"
reading_time_minutes: 1
breadcrumb: [Integrate Major Security Incident Management with Microsoft SharePoint, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Register a new application at Azure portal for SharePoint connections

Register a new application at Azure portal for Microsoft SharePoint integration.

## Before you begin

Role required: admin, Azure admin

## Procedure

1.  Sign in to [Microsoft Azure](https://portal.azure.com/#home) portal using your Microsoft account as Azure admin.

2.  Navigate to **Azure Services** &gt; **Application Registration** &gt; **New Registration**.

    **Note:** In case if you don't find, navigate to **Azure Services** and search for **App Registration**.

3.  Enter the name of the application.

    For example, Microsoft SharePoint graph.

4.  Select **Supported account types: Accounts in this organizational directory only \(Service Now only - Single tenant**\).

5.  Select **Web** type from the drop down list under the Redirect URI \(optional\) field.

6.  Enter ServiceNow AI Platform® instance redirect URL in the allowed redirect URL field.

    For example, `https://<InstanceName>.service-now.com/oauth_redirect.do`.

7.  Click on **Register** and make sure the page is displayed with **Overview** section.

8.  Make a note of the Client ID and Tenant ID from **Essentials** section of the Overview page.

9.  Under **API Permissions**, add the Microsoft Graph permission:

    1.  Click **Add a permission**.
    2.  Select **Microsoft Graph**.
    3.  Select **Application Permissions**.
    4.  From the **Sites** list, select **Sites.Selected** permission.
    5.  Click **Add permissions**.
10. Under **API Permissions**, add the SharePoint permission:

    1.  Click **Add a permission**.
    2.  Select **SharePoint**.
    3.  Select **Application Permissions**.
    4.  From the **Sites** list, select the **Sites.Selected** permission.
    5.  Click **Add permissions**.
11. After adding the permissions, click on  **Grant admin consent**.

    All the permissions are now admin consented.


**Parent Topic:**[Integrate Major Security Incident Management with Microsoft SharePoint](../../secops-integration-major-security-incident-management/concept/integrate-msim-sharepoint.md)

