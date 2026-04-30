---
title: Configure Microsoft Viva Engage for external content indexing
description: Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft Viva Engage external content connector to access your Microsoft Viva Engage source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-30"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft Viva Engage external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Microsoft Viva Engage for external content indexing

Register an OAuth 2.0 application in the Microsoft Entra admin center to allow the Microsoft Viva Engage external content connector to access your Microsoft Viva Engage source system.

## Before you begin

You need the following credentials and permissions for your organization in the Microsoft Entra admin center:

-   Login credentials
-   Permission to register an application
-   Permission to add API permissions to an application
-   Permission to create client secrets for an application

Role required: none

## About this task

The Microsoft Viva Engage external content connector retrieves content from your Microsoft Viva Engage source system using the Yammer API.

To enable the connector to access your Microsoft Viva Engage source system via these APIs, you must configure an OAuth 2.0 application in the Microsoft Entra admin center. Your connector admin can use settings copied from this Microsoft Entra application to configure the Microsoft Viva Engage external content connector for proper connection to your Microsoft Viva Engage source system.

## Procedure

1.  Register a new application in the Microsoft Entra admin center.

    1.  Log in to the Microsoft Entra admin center at [https://entra.microsoft.com/](https://entra.microsoft.com/).

        **Note:** If your Microsoft Viva Engage tenant is in the Microsoft 365 GCC or GCC High cloud or the Microsoft 365 DoD cloud, log in at [https://entra.microsoft.us/](https://entra.microsoft.us/) instead.

    2.  Select **Applications** &gt; **App registrations**.

    3.  On the App registrations page, select **New registration**.

        ![App registrations page in Microsoft Entra admin center with New registration link.](../image/ms-entra-home-app-registrations.png)

    4.  On the Register an application form, fill in the following fields:

        |Field|Instructions|
        |-----|------------|
        |Name|Enter a unique name for your OAuth 2.0 application. For example, you might enter `Microsoft Viva Engage external content connector`.|
        |Supported account types|Select **Accounts in this organizational directory only \(&lt;instance-name&gt; only - Single tenant\)**, where `<instance-name>` is the name of your Microsoft Entra instance.|
        |Redirect URI \(optional\)|Select **Web** as the redirect URI type, then enter `https://<instance-name>.service-now.com/oauth_redirect.do` as the URI, replacing `<instance-name>` with the hostname for the ServiceNow AI Platform® instance where the Microsoft Viva Engage external content connector will be created.|

        ![Register an application dialog box in Microsoft Entra admin center.](../image/ms-viva-engage-entra-register-application.png)

    5.  Select **Register**.

        The new application's Overview page appears.

2.  Record the values of the new application's **Application \(client\) ID** and **Directory \(tenant\) ID** properties in a secure location.

    ![Application's overview page in Microsoft Entra admin center showing application/client and directory/tenant ID values.](../image/ms-viva-engage-entra-app-overview.png)

    **Important:** Your connector admin needs the application's tenant and client IDs to configure a Microsoft Viva Engage external content connector.

3.  Create a client secret for the new application.

    1.  In the application menu, select **Manage** &gt; **Certificates &amp; secrets**.

    2.  Select **Client secrets**, then select **New client secret**.

        ![Application's client secrets list in Microsoft Entra admin center with New client secret link.](../image/ms-viva-engage-entra-new-client-secret.png)

    3.  In the Add a client secret pane, enter a description for the secret and select its expiration period, then select **Add**.

        ![Add a client secret dialog box in Microsoft Entra admin center.](../image/ms-viva-engage-entra-add-client-secret.png)

        The new client secret appears in the Client secrets list.

    4.  Copy the new client secret's **Value** and record it in a secure location.

        ![Application's client secrets list in Microsoft Entra admin center showing value for newly added client secret.](../image/ms-viva-engage-entra-copy-client-secret-value.png)

        **Important:** Your connector admin needs the value of this client secret to configure a Microsoft Viva Engage external content connector.

4.  Add the Yammer API permission required by the Microsoft Viva Engage external content connector.

    1.  In the application menu, select **Manage** &gt; **API permissions**.

        ![Application's API permissions page in Microsoft Entra admin center with Add a permission link.](../image/ms-viva-engage-entra-api-permissions.png)

    2.  Select **Add a permission**, then select **Yammer**.

        ![Request API permissions dialog box in Microsoft Entra admin center showing Yammer API tile.](../image/ms-entra-request-api-permissions-yammer.png)

    3.  Select **Delegated permissions**, then select the option for the **user\_impersonation** permission and select **Add permissions**.

        ![Request API permissions dialog box in Microsoft Entra admin center showing Delegated permissions tile and user_impersonation permission option.](../image/ms-viva-engage-entra-yammer-api-delegated-permissions.png)

        The new Yammer API permission appears in the application's Configured permissions list.

    ![Application's API permissions page in Microsoft Entra admin center showing added Yammer permission.](../image/ms-viva-engage-entra-api-permissions-after.png)


## What to do next

Provide the following items to your connector admin:

-   The OAuth 2.0 application's tenant ID and client ID that you recorded in step [2](configure-microsoft-viva-engage-external-content-indexing.md#client-tenant-ids-step).
-   The client secret value that you recorded in step [3.d](configure-microsoft-viva-engage-external-content-indexing.md#copy-client-secret).

Your connector admin needs these items to configure a Microsoft Viva Engage external content connector to retrieve searchable content and security principals from your Microsoft Viva Engage instance.

For details on creating and configuring a Microsoft Viva Engage external content connector, see [Create a Microsoft Viva Engage external content connector](create-ext-cont-connector-microsoft-viva-engage.md).

**Parent Topic:**[Microsoft Viva Engage external content connector](../concept/microsoft-viva-engage-external-content-connector.md)

