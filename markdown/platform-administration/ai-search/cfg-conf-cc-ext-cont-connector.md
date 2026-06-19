---
title: Configure Atlassian Confluence Cloud for external content indexing
description: Register an OAuth 2.0 integration in the Atlassian Developer console and create an API key in Atlassian Administration to allow the Atlassian Confluence Cloud external content connector to crawl spaces and security principals in your Atlassian Confluence Cloud source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/cfg-conf-cc-ext-cont-connector.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-12-17"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Atlassian Confluence Cloud external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
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

To allow the connector to access your Atlassian Confluence Cloud source system via the Confluence Cloud API, you must configure an OAuth 2.0 integration in the Atlassian Developer console and an API key in Atlassian Administration. Your connector administrator can use settings copied from the OAuth 2.0 integration and the API key to configure the Atlassian Confluence Cloud external content connector for proper connection to your Atlassian Confluence Cloud source system.

## Procedure

1.  In the Atlassian Developer console, register a new OAuth 2.0 integration for the Atlassian Confluence Cloud external content connector.

    1.  Login to the Atlassian Developer console at [https://developer.atlassian.com/console/myapps/](https://developer.atlassian.com/console/myapps/).

    2.  In the My apps section, select **Create** &gt; **OAuth 2.0 integration**.

        \[Omitted image "conf-cloud-ad-create-oauth2-app.png"\] Alt text: Create button and OAuth 2.0 integration menu item on Atlassian Developer console My apps page.

    3.  Enter a name for your OAuth 2.0 integration, select the option to agree to Atlassian's developer terms, and select **Create**.

        \[Omitted image "conf-cloud-ad-name-oauth2-app.png"\] Alt text: OAuth 2.0 \(3LO\) integration name, Atlassian developer terms option, and Create button on Atlassian Developer console.

        As an example, you might enter `Confluence Cloud external content connector` as the name for your OAuth 2.0 integration.

    4.  Navigate to the OAuth 2.0 integration's Permissions page, then select **Add** in the Confluence API row.

        \[Omitted image "conf-cloud-ad-add-conf-api-perms.png"\] Alt text: Add Confluence API button on Atlassian Developer console Permissions page.

    5.  In the Confluence API row, select **Configure**.

        \[Omitted image "conf-cloud-ad-conf-conf-api-perms.png"\] Alt text: Configure Confluence API button on Atlassian Permissions console.

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
        \[Omitted image "conf-cloud-ad-conf-api-edit-scopes.png"\] Alt text: Edit Scopes button on Atlassian Developer console Permissions page.

    7.  Select **Save**.

        \[Omitted image "conf-cloud-ad-conf-api-save-scopes.png"\] Alt text: Save button in Atlassian Developer console Edit Confluence API dialog box.

    8.  Navigate to the OAuth 2.0 integration's Authorization page, then select **Add** in the row for the OAuth 2.0 \(3LO\) authorization type.

        \[Omitted image "conf-cloud-ad-auth-add.png"\] Alt text: Add OAuth 2.0 \(3LO\) authorization button on Atlassian Developer console Authorization page.

    9.  Enter `https://<instance-name>.service-now.com/oauth_redirect.do` as the callback URL, replacing `<instance-name>` with your ServiceNow AI Platform® instance name, then select **Save changes**.

        \[Omitted image "conf-cloud-ad-auth-redirect-url.png"\] Alt text: Callback URL field and Save changes button on Atlassian Developer console Authorization page.

    10. Navigate to the OAuth 2.0 integration's Settings page and record the Client ID and Secret values in a secure location.

        \[Omitted image "conf-cloud-ad-settings.png"\] Alt text: Client ID and Secret fields on Atlassian Developer console Settings page.

        **Important:** Your connector administrator needs these Client ID and Secret values when configuring the Atlassian Confluence Cloud external content connector.

2.  In Atlassian Administration, create a new admin API key.

    1.  Login to Atlassian Administration at [https://admin.atlassian.com/](https://admin.atlassian.com/).

    2.  Select **Settings** in the tab list.

        \[Omitted image "conf-cloud-admin-settings.png"\] Alt text: Atlassian Administration console Settings tab.

    3.  Select **API keys**, then select **Create API key**.

        \[Omitted image "conf-cloud-admin-api-keys.png"\] Alt text: Create API key button on API keys page of Atlassian Administration console Settings section.

    4.  On the Before you begin page, select **API key without scopes**, then select **Next**.

        \[Omitted image "conf-cloud-admin-api-key-scopes.png"\] Alt text: API key scopes options in Atlassian Administration console dialog box.

    5.  Enter a name and an expiration date for your new API key.

        \[Omitted image "conf-cloud-admin-create-api-key.png"\] Alt text: API key name field, expiration-date field, and Create button in Atlassian Administration console dialog box.

        As an example, you might enter `Confluence Cloud external content connector` as the name for your API key and set its expiration date to be one year in the future.

    6.  Select **Create**.

    7.  Record the value of the API key in a secure location.

        \[Omitted image "conf-cloud-admin-copy-api-key.png"\] Alt text: API key in Atlassian Administration console dialog box.

        **Important:** Your connector administrator needs the API key's value when configuring the Atlassian Confluence Cloud external content connector.

    8.  Select **Done**.


## What to do next

Provide the following items to your connector administrator:

-   The OAuth 2.0 integration's Client ID and Secret values that you recorded in step [1.j](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/cfg-conf-cc-ext-cont-connector.md).
-   The API key's value that you recorded in step [2.g](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/cfg-conf-cc-ext-cont-connector.md).

Your connector administrator needs these items to configure an Atlassian Confluence Cloud external content connector to retrieve searchable content and security principals from your Atlassian Confluence Cloud instance.

For details on creating and configuring an Atlassian Confluence Cloud external content connector, see [Create an Atlassian Confluence Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-ext-cont-connector-acc.md).

**Note:** By default, the Atlassian Confluence Cloud external content connector only retrieves content access permissions for Confluence Cloud users who are managed by your organization. Other Confluence Cloud users can allow the connector to retrieve their content access permissions by setting their own email visibility to **Anyone** as explained in the [https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/](https://support.atlassian.com/confluence-cloud/docs/configure-user-email-visibility/) Atlassian support resource.

**Parent Topic:**[Atlassian Confluence Cloud external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/atlassian-confluence-cloud-external-content-connector.md)

