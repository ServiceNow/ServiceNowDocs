---
title: Configure SharePoint API permissions for your External Content Q&amp;A Genius Results OAuth 2.0 application
description: Add the AllSites.FullControl SharePoint API delegated permission to your External Q&amp;A Genius Results OAuth 2.0 application in Microsoft Azure portal and grant admin consent to allow the application to access this permission. The OAuth 2.0 application for External Q&amp;A Genius Results requires the delegated permission to search your Microsoft SharePoint Online sites.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Q&amp;A Genius Results, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure SharePoint API permissions for your External Content Q&amp;A Genius Results OAuth 2.0 application

Add the AllSites.FullControl SharePoint API delegated permission to your External Q&amp;A Genius Results OAuth 2.0 application in Microsoft Azure portal and grant admin consent to allow the application to access this permission. The OAuth 2.0 application for External Q&amp;A Genius Results requires the delegated permission to search your Microsoft SharePoint Online sites.

## Before you begin

The Now Assist in AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install Now Assist in AI Search](install-now-assist-ais.md).

You need to have an OAuth 2.0 application configured in Microsoft Azure portal for External Content Q&amp;A Genius Results. For details on this procedure, see [Configure OAuth application in Microsoft Azure](https://www.servicenow.com/docs/access?context=configure-oauth-application-in-microsoft-azure&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

You must have permissions to change the OAuth 2.0 application's settings in Microsoft Azure portal.

Role required: admin

## Procedure

1.  Access your OAuth 2.0 application's settings in Microsoft Azure portal.

    1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).

    2.  In the **Azure services** section, select **App registrations**.

        ![Microsoft Azure portal with App registrations service highlighted.](../image/azure-portal-app-reg.png)

    3.  Select **All applications** or **Owned applications**.

        ![Microsoft Azure portal with All applications and Owned applications categories highlighted.](../image/azure-portal-all-owned-apps.png)

    4.  In the search field, enter the name or application \(client\) ID of the OAuth 2.0 application you created for External Content Q&amp;A Genius Results, then select that application's display name from the list of results.

        ![Microsoft Azure portal with search term and matching application display name highlighted.](../image/azure-portal-app-srch.png)

        To learn how to configure an OAuth 2.0 application for External Content Q&amp;A Genius Results, see [Configure OAuth application in Microsoft Azure](https://www.servicenow.com/docs/access?context=configure-oauth-application-in-microsoft-azure&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

2.  Add an AllSites.FullControl SharePoint API delegated permission to your OAuth 2.0 application.

    1.  In the menu, select **Manage** &gt; **API permissions**.

        ![Microsoft Azure portal application page with API permissions menu item highlighted.](../image/azure-portal-api-perms.png)

    2.  Under the **Configured permissions** heading, select **Add a permission**.

        ![Microsoft Azure portal application page with Add a permission link highlighted.](../image/azure-portal-add-perm.png)

    3.  In the **Request API permissions** window's **Select an API** section, select **Microsoft APIs**, then select the **SharePoint** API.

        ![Microsoft Azure portal Request API permissions page with Microsoft APIs category highlighted.](../image/azure-portal-req-ms-apis.png)

        ![Microsoft Azure portal Request API permissions page with SharePoint API highlighted.](../image/azure-portal-req-sharepoint-api.png)

    4.  When prompted, select **Delegated permissions** as the type of permission to add.

        ![Microsoft Azure portal Request API permissions page with delegated permissions type highlighted.](../image/azure-portal-req-delegated-perms.png)

    5.  In the **Select permissions** section, select **AllSites** &gt; **AllSites.FullControl**, then select **Add permissions**.

        ![Microsoft Azure portal Request API permissions page with AllSites category, AllSites.FullControl selected permission, and Add permissions button highlighted.](../image/azure-portal-allsites-perm.png)

        The new AllSites.FullControl SharePoint API permission appears in the list of configured permissions with status `Not granted for ServiceNow`.

    6.  Under the **Configured permissions** heading, select **Grant admin consent for ServiceNow**.

        ![Microsoft Azure portal application page with Grant admin consent for ServiceNow link highlighted.](../image/azure-portal-grant-admin-consent.png)

    7.  In the **Grant admin consent confirmation** dialog box, select **Yes**.

        ![Microsoft Azure portal application page with Grant admin consent confirmation dialog box's Yes button highlighted.](../image/azure-portal-grant-confirmation.png)

        The AllSites.FullControl SharePoint API permission's status changes to `Granted for ServiceNow`.


## What to do next

Configure the OAuth 2.0 settings in your ServiceNow AI Platform® instance that are needed for External Content Q&amp;A Genius Results. For details on this procedure, see [Configure OAuth settings for External Content Q&amp;A Genius Results](configure-oauth-ext-cont-qna-gr.md).

**Parent Topic:**[External Content Q&amp;A Genius Results](../concept/external-content-qna.md)

