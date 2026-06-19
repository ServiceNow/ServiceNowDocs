---
title: Configure SharePoint API permissions for your External Content Q&amp;A Genius Results OAuth 2.0 application
description: Add the AllSites.FullControl SharePoint API delegated permission to your External Q&amp;A Genius Results OAuth 2.0 application in Microsoft Azure portal and grant admin consent to allow the application to access this permission. The OAuth 2.0 application for External Q&amp;A Genius Results requires the delegated permission to search your Microsoft SharePoint Online sites.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/grant-perms-azure-ext-cont-qna-grs.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Q&amp;A Genius Results, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure SharePoint API permissions for your External Content Q&amp;A Genius Results OAuth 2.0 application

Add the AllSites.FullControl SharePoint API delegated permission to your External Q&amp;A Genius Results OAuth 2.0 application in Microsoft Azure portal and grant admin consent to allow the application to access this permission. The OAuth 2.0 application for External Q&amp;A Genius Results requires the delegated permission to search your Microsoft SharePoint Online sites.

## Before you begin

The Now Assist in AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/install-now-assist-ais.md).

You need to have an OAuth 2.0 application configured in Microsoft Azure portal for External Content Q&amp;A Genius Results. For details on this procedure, see .

You must have permissions to change the OAuth 2.0 application's settings in Microsoft Azure portal.

Role required: admin

## Procedure

1.  Access your OAuth 2.0 application's settings in Microsoft Azure portal.

    1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).

    2.  In the **Azure services** section, select **App registrations**.

        \[Omitted image "azure-portal-app-reg.png"\] Alt text: Microsoft Azure portal with App registrations service highlighted.

    3.  Select **All applications** or **Owned applications**.

        \[Omitted image "azure-portal-all-owned-apps.png"\] Alt text: Microsoft Azure portal with All applications and Owned applications categories highlighted.

    4.  In the search field, enter the name or application \(client\) ID of the OAuth 2.0 application you created for External Content Q&amp;A Genius Results, then select that application's display name from the list of results.

        \[Omitted image "azure-portal-app-srch.png"\] Alt text: Microsoft Azure portal with search term and matching application display name highlighted.

        To learn how to configure an OAuth 2.0 application for External Content Q&amp;A Genius Results, see .

2.  Add an AllSites.FullControl SharePoint API delegated permission to your OAuth 2.0 application.

    1.  In the menu, select **Manage** &gt; **API permissions**.

        \[Omitted image "azure-portal-api-perms.png"\] Alt text: Microsoft Azure portal application page with API permissions menu item highlighted.

    2.  Under the **Configured permissions** heading, select **Add a permission**.

        \[Omitted image "azure-portal-add-perm.png"\] Alt text: Microsoft Azure portal application page with Add a permission link highlighted.

    3.  In the **Request API permissions** window's **Select an API** section, select **Microsoft APIs**, then select the **SharePoint** API.

        \[Omitted image "azure-portal-req-ms-apis.png"\] Alt text: Microsoft Azure portal Request API permissions page with Microsoft APIs category highlighted.

        \[Omitted image "azure-portal-req-sharepoint-api.png"\] Alt text: Microsoft Azure portal Request API permissions page with SharePoint API highlighted.

    4.  When prompted, select **Delegated permissions** as the type of permission to add.

        \[Omitted image "azure-portal-req-delegated-perms.png"\] Alt text: Microsoft Azure portal Request API permissions page with delegated permissions type highlighted.

    5.  In the **Select permissions** section, select **AllSites** &gt; **AllSites.FullControl**, then select **Add permissions**.

        \[Omitted image "azure-portal-allsites-perm.png"\] Alt text: Microsoft Azure portal Request API permissions page with AllSites category, AllSites.FullControl selected permission, and Add permissions button highlighted.

        The new AllSites.FullControl SharePoint API permission appears in the list of configured permissions with status `Not granted for ServiceNow`.

    6.  Under the **Configured permissions** heading, select **Grant admin consent for ServiceNow**.

        \[Omitted image "azure-portal-grant-admin-consent.png"\] Alt text: Microsoft Azure portal application page with Grant admin consent for ServiceNow link highlighted.

    7.  In the **Grant admin consent confirmation** dialog box, select **Yes**.

        \[Omitted image "azure-portal-grant-confirmation.png"\] Alt text: Microsoft Azure portal application page with Grant admin consent confirmation dialog box's Yes button highlighted.

        The AllSites.FullControl SharePoint API permission's status changes to `Granted for ServiceNow`.


## What to do next

Configure the OAuth 2.0 settings in your ServiceNow AI Platform® instance that are needed for External Content Q&amp;A Genius Results. For details on this procedure, see [Configure OAuth settings for External Content Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-oauth-ext-cont-qna-gr.md).

**Parent Topic:**[External Content Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/external-content-qna.md)

