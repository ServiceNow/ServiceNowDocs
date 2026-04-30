---
title: Configure OAuth settings for External Content Q&amp;A Genius Results
description: Configure the settings that External Content Q&amp;A Genius Results need to interact with your Microsoft SharePoint Online instance.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-08-01"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Q&amp;A Genius Results, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure OAuth settings for External Content Q&amp;A Genius Results

Configure the settings that External Content Q&amp;A Genius Results need to interact with your Microsoft SharePoint Online instance.

## Before you begin

The Now Assist in AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install Now Assist in AI Search](install-now-assist-ais.md).

You must have already completed the following tasks:

-   [Request installation](https://www.servicenow.com/docs/access?context=request-integrationhub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) of the ServiceNow IntegrationHub Enterprise Pack Installer \[com.glide.hub.integrations.enterprise\] plugin
-   [Configure OAuth application in Microsoft Azure](https://www.servicenow.com/docs/access?context=configure-oauth-application-in-microsoft-azure&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)

You will need read access to the following Microsoft Azure Portal configuration settings for your Microsoft SharePoint Online instance:

-   Root site URL
-   Client ID
-   Client secret
-   Tenant ID
-   Authorization URL
-   Token URL
-   Token revocation URL
-   Redirect URL

Role required: admin

## About this task

Administrators need to perform this one-time procedure to enable External Content Q&amp;A Genius Results.

## Procedure

1.  Create an Application Registry record:

    1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

    2.  Select **New**.

    3.  Select **Connect to a third party OAuth Provider**.

    4.  On the Application Registries form, fill in the fields:

        |Field|Value|
        |-----|-----|
        |Name|Enter a name of your choice for the Application Registry record.|
        |Client ID|Enter the client ID value from your Microsoft SharePoint Online configuration on Microsoft Azure Portal.|
        |Client Secret|Enter the client secret value from your Microsoft SharePoint Online configuration on Microsoft Azure Portal.|
        |Default Grant type|Select **Authorization Code**.|
        |Authorization URL|Enter the fully-qualified authorization URL for your Microsoft SharePoint Online source system in this format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/authorize`. Replace `<tenant-id>` with your Microsoft SharePoint Online tenant ID, as found in your Microsoft Azure Portal settings.|
        |Token URL|Enter the fully-qualified token URL for your Microsoft SharePoint Online source system in this format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token`. Replace `<tenant-id>` with your Microsoft SharePoint Online tenant ID, as found in your Microsoft Azure Portal settings.|
        |Token Revocation URL|Enter the fully-qualified token revocation URL for your Microsoft SharePoint Online source system in this format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token`. Replace `<tenant-id>` with your Microsoft SharePoint Online tenant ID, as found in your Microsoft Azure Portal settings.|
        |Redirect URL|Enter the fully-qualified redirect URL for the Integration Hub subflow in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`. Replace `<instance-name>` with your ServiceNow AI Platform® instance name, as specified in your Microsoft Azure Portal settings.|

    5.  Select **Submit**.

        The new Application Registry record appears in the table list view.

2.  Define an OAuth entity scope for your new Application Registry record:

    1.  Open your new Application Registry record in form view by selecting it.

    2.  In the OAuth Entity Profiles related list, verify that an OAuth entity profile record appears with **Is default** set to **true** and **Grant type** set to **Authorization Code**.

        ![OAuth Entity Profiles related list showing entity profile record with correct field values.](../image/oauth-entity-profiles-related-list.png)

    3.  Open the new OAuth entity profile record in form view by selecting its name.

    4.  On the OAuth Entity Profile form, in the OAuth Entity Profile Scopes related list, double-click **Insert a new row**, then select the Lookup using list icon ![](../image/icon-lookup-using-list.png).

        ![OAuth Entity Profile form with OAuth Entity Profile Scopes related list's Insert a new row… link highlighted.](../image/oauth-entity-profile-form.png)

        ![OAuth Entity Profile form with OAuth Entity Profile Scopes related list's Lookup using list icon highlighted.](../image/oauth-entity-profile-lookup.png)

    5.  On the OAuth Entity Scopes form, select **New**.

        ![OAuth Entity Scopes list view with New button highlighted.](../image/oauth-entity-scopes-new.png)

    6.  On the OAuth Entity Scope form, fill in the fields:

<table id="table_scn_j5m_3bc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name of your choice for the connection and credential alias.

</td></tr><tr><td>

OAuth provider

</td><td>

Select or enter the name of the Application Registry record that you created in step [1.e](configure-oauth-ext-cont-qna-gr.md#create-application-registry-record).

</td></tr><tr><td>

OAuth scope

</td><td>

Enter `offline_access https://<root-site>.sharepoint.com/.default`, replacing `<root-site>` with the name of your Microsoft SharePoint Online instance's root site.**Important:** Make sure to include the dot before `default`.

</td></tr></tbody>
</table>    7.  Select **Submit**.

    8.  In the OAuth Entity Profile Scopes related list, select the Save \(Enter\) icon ![](../../list-administration/image/IconSave.png).

        ![OAuth Entity Profile form with OAuth Entity Profile Scopes related list's Save (Enter) icon highlighted.](../image/oauth-entity-scopes-save.png)

        The new OAuth entity scope record appears in the OAuth Entity Profile Scopes related list.

    9.  Select **Update**.

3.  Define a connection and credential alias record for Microsoft SharePoint Online:

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open the **MicrosoftSharePointOnlineforAISearch** alias record in form view by selecting it.

    3.  In the Connections related list, select **New**.

    4.  On the HTTP\(s\) Connection form, fill in the fields:

        |Field|Value|
        |-----|-----|
        |Name|Enter a name of your choice for the connection and credential alias.|
        |Connection URL|Enter the fully-qualified URL for your Microsoft SharePoint Online instance: `https://<root-site>.sharepoint.com`.|

    5.  To create your new connection record, select **Submit**.

        The new connection record appears in the Connections related list.

4.  Define a new OAuth 2.0 credential associated with your Application Registry record:

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Select **New**.

    3.  Select **OAuth 2.0 Credentials**.

    4.  If the **Integration Type** field isn't visible on the OAuth 2.0 Credentials form, configure the form layout to make the field visible.

        For details on configuring a form layout, see [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#).

    5.  On the OAuth 2.0 Credentials form, fill in the fields:

        |Field|Value|
        |-----|-----|
        |Name|Enter a name of your choice for the OAuth 2.0 credential record.|
        |OAuth Entity Profile|Select the new OAuth entity profile record associated with the Application Registry record that you created in step [1.e](configure-oauth-ext-cont-qna-gr.md#create-application-registry-record).|
        |Integration Type|Select **Personal**.|

    6.  Select **Submit**.

        The new OAuth 2.0 credentials record appears in the Credentials \[discovery\_credentials\] table list view.

5.  Specify your new OAuth 2.0 credential as the one to use when connecting to Microsoft SharePoint Online:

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open the **MicrosoftSharePointOnlineforAISearch** alias record in form view by selecting it.

    3.  In the Connections related list, select the connection record that you created in step [3.e](configure-oauth-ext-cont-qna-gr.md#create-https-connection-record).

    4.  On the HTTP\(s\) Connection form, select the **Credential** field's Lookup using list icon ![](../image/icon-lookup-using-list.png), then select the credential that you defined in step [4](configure-oauth-ext-cont-qna-gr.md#define-oauth-2.0-credential).

    5.  Select **Update**.


## What to do next

You can optionally configure a Microsoft Keyword Query Language \(KQL\) query to restrict the set of Microsoft SharePoint Online sites that External Content Q&amp;A Genius Results search for relevant documents. For details on defining this KQL query, see [Restrict the Microsoft SharePoint Online sites that External Content Q&amp;A Genius Results can search](filter-spo-sites-ext-cont-qa-gr.md).

**Parent Topic:**[External Content Q&amp;A Genius Results](../concept/external-content-qna.md)

