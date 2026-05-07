---
title: Create a project and add APIs using OAuth
description: Create a project in the Adobe Developer Console for accessing Adobe APIs and add APIs to your project using OAuth.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate Adobe Cloud using OAuth Server-to-Server credentials, Integrating with Adobe Cloud, Software Asset Management publisher pack for Adobe, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a project and add APIs using OAuth

Create a project in the Adobe Developer Console for accessing Adobe APIs and add APIs to your project using OAuth.

## Before you begin

Role required: Adobe Cloud admin

## Procedure

1.  Create a project in the Adobe Developer Console to access the Adobe APIs by selecting **Create new project**.

    For more information, see [Projects Overview](https://developer.adobe.com/developer-console/docs/guides/projects/).

2.  Add an API to your project by selecting **Add API**.

    For more information, see [Add API to project using OAuth](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth/).![Adobe Developer Console user interface showing the Add API functionality](../image/adobe-add-api.png)

3.  Select **User Management API** for the Adobe service that you want to integrate with.

    This service enables you to access the Adobe user management API. After you successfully add the API to your project, you’re redirected to the API overview page.

4.  Select **Next**.

5.  On the Configure API form, expand **Credentials**.

6.  Select the **OAuth Server-to-Server** authentication.

7.  Provide a name in the **Credential name** field to find the correct API credential easily on the **Admin Console** &gt; **Users** &gt; **API Credentials**.

    You can also modify the name later in your project on the OAuth Server-to-Server credential overview page.

8.  Select **Save configured API**.

    The following values are displayed on the credential overview page:

    -   CLIENT ID
    -   CLIENT SECRET
    -   SCOPES
    -   CREDENTIAL NAME
    -   TECHNICAL ACCOUNT ID
    -   TECHNICAL ACCOUNT EMAIL
    -   ORGANIZATION ID
    **Note:**

    Copy the CLIENT ID and ORGANIZATION ID and also retrieve the CLIENT SECRET to use them later.

9.  Get the Connection URL \(Instance URL\) from the Adobe Developer Console to create and get an OAuth token for Adobe Cloud.

    1.  In the Generate access token section, select **View cURL command**.

    2.  Copy the Connection URL.

        **Note:**

        Copy only the required URL from the entire command.

        For example, here the Connection URL is the highlighted part.

        ![Connection URL in Adobe Developer Console.](../image/access-token-adobe.jpg)


