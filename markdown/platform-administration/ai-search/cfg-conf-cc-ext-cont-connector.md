---
title: Configure Atlassian Confluence Cloud for external content indexing
description: Register an OAuth 2.0 integration in the Atlassian Developer console and create an API key in Atlassian Administration to allow the Atlassian Confluence Cloud external content connector to crawl spaces and security principals in your Atlassian Confluence Cloud source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Atlassian Confluence Cloud external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Atlassian Confluence Cloud for external content indexing

Register an OAuth 2.0 integration in the Atlassian Developer console and create an API key in Atlassian Administration to allow the Atlassian Confluence Cloud external content connector to crawl spaces and security principals in your Atlassian Confluence Cloud source system.

## Before you begin

You need the following credentials and permissions for your organization's Atlassian management applications:

<table id="table_wr3_s1q_xdc"><thead><tr><th>

Atlassian portal

</th><th>

Required credentials and permissions

</th></tr></thead><tbody><tr><td>

Atlassian Developer console \([https://developer.atlassian.com/console/myapps/](https://developer.atlassian.com/console/myapps/)\)

</td><td>

-   Login credentials
-   Permission to view settings for registered applications
-   Permission to register a new application
-   Permission to set granular Confluence API scopes for an application
-   Permission to set the OAuth 2.0 callback URL for an application

</td></tr><tr><td>

Atlassian Administration \([https://admin.atlassian.com/](https://admin.atlassian.com/)\)

</td><td>

-   Organization admin login credentials

</td></tr></tbody>
</table>Role required: none

## About this task

The Atlassian Confluence Cloud external content connector retrieves content from your Atlassian Confluence Cloud source system using the Confluence Cloud API.

To allow the connector to access your Atlassian Confluence Cloud source system via the Confluence Cloud API, you must configure an OAuth 2.0 integration in the Atlassian Developer console and an API key in Atlassian Administration. Your connector admin can use settings copied from the OAuth 2.0 integration and the API key to configure the Atlassian Confluence Cloud external content connector for proper connection to your Atlassian Confluence Cloud source system.

## Procedure

1.  In the Atlassian Developer console, register a new OAuth 2.0 integration for the Atlassian Confluence Cloud external content connector.

    1.  Login to the Atlassian Developer console at [https://developer.atlassian.com/console/myapps/](https://developer.atlassian.com/console/myapps/).

    2.  In the My apps section, select **Create** &gt; **OAuth 2.0 integration**.

        ![Create button and OAuth 2.0 integration menu item on Atlassian Developer console My apps page.](../image/conf-cloud-ad-create-oauth2-app.png)

    3.  Enter a name for your OAuth 2.0 integration, select the option to agree to Atlassian's developer terms, and select **Create**.

        ![OAuth 2.0 (3LO) integration name, Atlassian developer terms option, and Create button on Atlassian Developer console.](../image/conf-cloud-ad-name-oauth2-app.png)

        As an example, you might enter `Confluence Cloud external content connector` as the name for your OAuth 2.0 integration.

    4.  Navigate to the OAuth 2.0 integration's Permissions page, then select **Add** in the Confluence API row.

        ![Add Confluence API button on Atlassian Developer console Permissions page.](../image/conf-cloud-ad-add-conf-api-perms.png)

    5.  In the Confluence API row, select **Configure**.

        ![Configure Confluence API button on Atlassian Permissions console.](../image/conf-cloud-ad-conf-conf-api-perms.png)

    6.  On the Granular scopes tab, select **Edit Scopes** and then select the options for each of the following scopes:

        -   read:attachment:confluence
        -   read:blogpost:confluence
        -   read:content-details:confluence
        -   read:content.metadata:confluence
        -   read:folder:confluence
        -   read:group:confluence
        -   read:page:confluence
        -   read:space:confluence
        -   read:user:confluence
        ![Edit Scopes button on Atlassian Developer console Permissions page.](../image/conf-cloud-ad-conf-api-edit-scopes.png)

    7.  Select **Save**.

        ![Save button in Atlassian Developer console Edit Confluence API dialog box.](../image/conf-cloud-ad-conf-api-save-scopes.png)

    8.  Navigate to the OAuth 2.0 integration's Authorization page, then select **Add** in the row for the OAuth 2.0 \(3LO\) authorization type.

        ![Add OAuth 2.0 (3LO) authorization button on Atlassian Developer console Authorization page.](../image/conf-cloud-ad-auth-add.png)

    9.  Enter `https://<instance-name>.service-now.com/oauth_redirect.do` as the callback URL, replacing `<instance-name>` with your ServiceNow AI Platform® instance name, then select **Save changes**.

        ![Callback URL field and Save changes button on Atlassian Developer console Authorization page.](../image/conf-cloud-ad-auth-redirect-url.png)

    10. Navigate to the OAuth 2.0 integration's Settings page and record the Client ID and Secret values in a secure location.

        ![Client ID and Secret fields on Atlassian Developer console Settings page.](../image/conf-cloud-ad-settings.png)

        **Important:** Your connector admin needs these Client ID and Secret values when configuring the Atlassian Confluence Cloud external content connector.

2.  In Atlassian Administration, create a new admin API key.

    1.  Login to Atlassian Administration at [https://admin.atlassian.com/](https://admin.atlassian.com/).

    2.  Select **Settings** in the tab list.

        ![Atlassian Administration console Settings tab.](../image/conf-cloud-admin-settings.png)

    3.  Select **API keys**, then select **Create API key**.

        ![Create API key button on API keys page of Atlassian Administration console Settings section.](../image/conf-cloud-admin-api-keys.png)

    4.  On the Before you begin page, select **API key without scopes**, then select **Next**.

        ![API key scopes options in Atlassian Administration console dialog box.](../image/conf-cloud-admin-api-key-scopes.png)

    5.  Enter a name and an expiration date for your new API key.

        ![API key name field, expiration-date field, and Create button in Atlassian Administration console dialog box.](../image/conf-cloud-admin-create-api-key.png)

        As an example, you might enter `Confluence Cloud external content connector` as the name for your API key and set its expiration date to be one year in the future.

    6.  Select **Create**.

    7.  Record the value of the API key in a secure location.

        ![API key in Atlassian Administration console dialog box.](../image/conf-cloud-admin-copy-api-key.png)

        **Important:** Your connector admin needs the API key's value when configuring the Atlassian Confluence Cloud external content connector.

    8.  Select **Done**.


## What to do next

Provide the following items to your connector admin:

-   The OAuth 2.0 integration's Client ID and Secret values that you recorded in step [1.j](cfg-conf-cc-ext-cont-connector.md#record-client-id-and-secret-step).
-   The API key's value that you recorded in step [2.g](cfg-conf-cc-ext-cont-connector.md#record-api-key).

Your connector admin needs these items to configure an Atlassian Confluence Cloud external content connector to retrieve searchable content and security principals from your Atlassian Confluence Cloud instance.

For details on creating and configuring an Atlassian Confluence Cloud external content connector, see [Create an Atlassian Confluence Cloud external content connector](create-ext-cont-connector-acc.md).

**Note:** By default, the Atlassian Confluence Cloud external content connector only retrieves content access permissions for Confluence Cloud users who are managed by your organization. Other Confluence Cloud users can allow the connector to retrieve their content access permissions by setting their own email visibility to **Anyone** as explained in the [https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/](https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/) Atlassian support resource.

**Parent Topic:**[Atlassian Confluence Cloud external content connector](../concept/atlassian-confluence-cloud-external-content-connector.md)

