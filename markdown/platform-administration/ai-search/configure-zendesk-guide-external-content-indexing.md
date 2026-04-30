---
title: Configure Zendesk for external content indexing
description: Create an API token in Zendesk Admin Center to allow the Zendesk Guide external content connector to access your Zendesk source system.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Zendesk Guide external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Zendesk for external content indexing

Create an API token in Zendesk Admin Center to allow the Zendesk Guide external content connector to access your Zendesk source system.

## Before you begin

You need administrator access to your Zendesk instance.

Role required: none

## About this task

The Zendesk Guide external content connector retrieves documents and user permissions from your Zendesk source system using the Zendesk API.

To allow the connector to access your Zendesk source system via the Zendesk API, you must create an API token in the Zendesk Admin Center. Your connector admin can use this API token to configure the Zendesk Guide external connector for proper connection to your source system.

## Procedure

1.  Navigate to `https://<subdomain>.zendesk.com`, where `<subdomain>` is the unique identifier for your Zendesk instance.

2.  Log in with your Zendesk administrator credentials.

3.  Open the app menu by selecting its icon ![](../image/zendesk-app-menu-icon.png), then select **Admin Center**.

    ![Admin center link in Zendesk app menu.](../image/zendesk-admin-center.png)

4.  In the Admin Center menu, navigate to **Apps and integrations** &gt; **APIs** &gt; **OAuth clients**.

    If the Admin Center menu labels aren't shown, select the **Apps and integrations** icon ![](../image/zendesk-ac-apps-integrations-icon.png) to expand the menu and navigate.

5.  On the Zendesk OAuth clients page, select **Add OAuth client**.

    ![OAuth clients page in Zendesk with Add OAuth client button.](../image/zendesk-oauth-clients-before.png)

    The Add OAuth client page appears.

6.  On the Add OAuth client page, fill in the fields.

<table id="table_y32_hsr_tfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name\* \(required\)

</td><td>

Enter a name for your new OAuth 2.0 client application. As an example, you might enter `Zendesk Guide external content connector`.

</td></tr><tr><td>

Description\*

</td><td>

Enter a short description for your new OAuth 2.0 client application. This description is shown to users when they're asked to grant access to the application. As an example, you might enter `App that allows the ServiceNow Zendesk Guide external content connector to access our Zendesk source system.`.

</td></tr><tr><td>

Company\*

</td><td>

Enter the name of your organization. As an example, you might enter `Example.com`.

</td></tr><tr><td>

Identifier\*

</td><td>

Enter the identifier string you want to use when referring to your new OAuth 2.0 client application in code. A default identifier is automatically generated from the application name you enter, but you can override it if you want to use a different value.**Important:** Your connector admin needs this client identifier when configuring the Zendesk external content connector.

</td></tr><tr><td>

Client kind

</td><td>

Select **Confidential**.

</td></tr><tr><td>

Redirect URLs

</td><td>

Enter `https://<instance-name>.service-now.com/oauth_redirect.do`, where `<instance-name>` is the hostname for your ServiceNow AI Platform® instance where you will create and run the external content connector. As an example, you might enter `https://example.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>    ![Add OAuth client page in Zendesk.](../image/zendesk-add-oauth-client.png)

7.  Select **Save**.

    Zendesk adds your new OAuth 2.0 client application and displays its generated client secret at the bottom of the Add OAuth client page.

8.  Copy your new OAuth 2.0 client application's **Secret** and save it in a secure location.

    ![Add OAuth client page in Zendesk showing generated client secret.](../image/zendesk-save-oauth-client-secret.png)

    **Important:** Your connector admin needs this client secret when configuring the Zendesk external content connector.

9.  Select **Save**.

    ![OAuth clients page in Zendesk showing new OAuth 2.0 client application.](../image/zendesk-oauth-clients-after.png)

    Zendesk updates your new OAuth 2.0 client application with the generated secret. Your new application appears on the Zendesk OAuth clients page.


## What to do next

Provide the following items to your connector admin:

-   The OAuth 2.0 client identifier that you entered in step [6](configure-zendesk-guide-external-content-indexing.md#choose-client-identifier-step).
-   The client secret that you saved in step [8](configure-zendesk-guide-external-content-indexing.md#save-client-secret-step).

Your connector admin needs these settings to configure a Zendesk Guide external content connector to retrieve searchable content and security principals from your Zendesk source system.

For details on creating and configuring a Zendesk Guide external content connector, see [Create a Zendesk Guide external content connector](create-ext-cont-connector-zendesk-guide.md).

**Parent Topic:**[Zendesk Guide external content connector](../concept/zendesk-guide-external-content-connector.md)

