---
title: Setting up the SharePoint Online Search Connector
description: Set up the SharePoint Online Search Connector by configuring and connecting the Microsoft SharePoint tenant with your instance. Validate the connection to avoid any setup failures before indexing the sites for search.Configure your Microsoft SharePoint tenant to get started with the SharePoint Online Search Connector.Link search sources to a search profile to specify the content users can search through the linked search profile.Connect your ServiceNow instance with a Microsoft SharePoint tenant. Create custom ServiceNow OAuth connections for Microsoft SharePoint to authenticate ServiceNow requests.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [SharePoint Online Search Connector, Employee Service Management]
---

# Setting up the SharePoint Online Search Connector

Set up the SharePoint Online Search Connector by configuring and connecting the Microsoft SharePoint tenant with your instance. Validate the connection to avoid any setup failures before indexing the sites for search.

## Configure the Microsoft SharePoint tenant

Configure your Microsoft SharePoint tenant to get started with the SharePoint Online Search Connector.

### Before you begin

As a Microsoft SharePoint administrator, create a custom application by specifying the root URL \(`https:// <sitename>.sharepoint.com`\), app domain, redirect URL, and other settings.

**Important:** Starting with the Yokohama release, SharePoint Online Search Connector is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continue to be supported.

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

Ensure you complete the following prerequisites.

-   Follow the procedure to [Configure OAuth application in Microsoft Azure](https://www.servicenow.com/docs/access?context=configure-oauth-application-in-microsoft-azure&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
-   Follow the procedure to [Set up Microsoft Entra ID spoke](https://www.servicenow.com/docs/access?context=set-up-azure&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US). Microsoft Entra ID spoke \(formerly known as Microsoft Azure Active Directory spoke\) is a dependent plugin that needs to be set up before indexing the users.
-   Understand how to [Configure Microsoft SharePoint Graph connection](https://www.servicenow.com/docs/access?context=configure-microsoft-sharepoint-graph-connection&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
-   Log in with your admin credentials to grant permissions.

Role required: admin

### About this task

Complete the following procedure from your Microsoft SharePoint account. For more information on creating and configuring custom applications, see the [SharePoint development](https://docs.microsoft.com/en-us/sharepoint/dev/)

**Note:** When the permissions assigned in the Azure apps have privilege issues, the following error message appears: `Error message: Method failed: (/_api/web/XXXXXXX) with code: 401 - Invalid username/password combo`. Address this issue with the instructions available in [KB1117977](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117977).

When you want the search results to display only the published versions of the documents, ensure you select **Application permissions** instead of the **Delegated permissions** while configuring the permissions explained in [Microsoft SharePoint Online Spoke](https://www.servicenow.com/docs/access?context=sharepoint-online-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

**Note:** Admins can limit indexing to the published versions only, ensuring that drafts or unfinished work aren’t displayed in the search results.​

### Procedure

1.  Navigate to **Azure** &gt; **Active Directory** &gt; **App registrations** &gt; **All applications**, and select an existing app.

    Use an existing application or create an application.

2.  **Configured permissions**
3.  Navigate to **App registrations** &gt; **API permissions**, and click **Add a permission**.

4.  Select one of the following options:

    1.  Navigate to **Microsoft Graph** &gt; **Delegated permissions** for Graph.

    2.  Navigate to **Microsoft Graph** &gt; **Application permissions** for Graph.

    Add the **Sites.ReadWrite.All** permission from the Sites list. The Sites.ReadWrite.All permission helps with subscription creation.

    Add the **User.Read** permission from the Users list.

    These user permissions are used to crawl the Microsoft SharePoint data later.

5.  Navigate to **Sharepoint** &gt; **Application permissions** &gt; **Sites**, and select **Sites.FullControl.All**, **Sites.Read.All**, or **Sites.Selected** for REST.

    Enable the **Sites.Selected** permission by performing the following steps.

    1.  In the Microsoft Azure application, enable the **Sites.Selected** and the **User.Read.All** permissions.

        Use any API client to provide read access for the following site collections.

        -   Application X that is connected to a ServiceNow instance and has the **Sites.Selected** permission.
        -   Application Y that is an admin application and has the **Sites.Full.Control** permission for Graph connection.
    2.  Get a bearer token by calling the API method https://login.microsoftonline.com/\{Tenant Id\}/oauth2/v2.0/token.

        Payload:

        ```json
        client_id={App Y client id}
        &scope=https%3A%2F%2Fgraph.microsoft.com%2F.default
        &client_secret={App Y client secret}
        &grant_type=client_credentials
        ```

    3.  Pass the token received in step b as the authorization token while calling the API method https://graph.microsoft.com/v1.0/sites/\{site id\}/permissions.

        Payload:

        ```
        {
        "roles": [
        "read"
        ],
        "grantedToIdentities": [
        {
        "application": {
        "id": "App X client id",
        "displayName": "App X"
        }
        }
        ]
        }
        ```

6.  Ensure you configure the required API permissions as shown in the following image:

    ![SharePoint configured permission list](../image/spoc-permissions-azure.png "Configured permissions list")

    For more information, see [Configure Microsoft SharePoint Graph connection](https://www.servicenow.com/docs/access?context=configure-microsoft-sharepoint-graph-connection&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

7.  Click **Grant admin consent**, select **Yes**, and click **Save and Continue**.

8.  Navigate to **Authentication** &gt; **Web** &gt; **Redirect URLs** and add the URL in this format `https://<your Servicenow instance URL>/oauth_redirect.do`, for example, [https://eesharepoint.example.com/oauth\_redirect.do](https://eesharepoint.example.com/oauth_redirect.do) and click **Save**.

9.  Navigate to [Microsoft SharePoint Online Spoke](https://www.servicenow.com/docs/access?context=sharepoint-online-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) and register the certificate and secret for your application.

10. Click **Add user** on the [Microsoft admin portal](http://admin.microsoft.com/AdminPortal/Home#/users), specify the user details, and click **Finish**.

    **Note:** The search crawls the sites that you can access. Ensure that you select the user with appropriate permissions for only the required content. For more information, see [user permissions](https://docs.microsoft.com/en-us/sharepoint/customize-sharepoint-site-permissions). Selecting a high-level user can import more documents than you want to import.

    For more information, see [Granting access via Azure AD App-Only](https://docs.microsoft.com/en-us/sharepoint/dev/solution-guidance/security-apponly-azuread).


### What to do next

Complete the integration from your ServiceNow AI Search account. For more information, see [Integrate the Microsoft SharePoint search sources with the AI Search profiles](setup-sp-ovrvw.md#).

## Integrate the Microsoft SharePoint search sources with the AI Search profiles

Link search sources to a search profile to specify the content users can search through the linked search profile.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Search Applications** &gt; **Search Application Configurations** \(sys\_search\_context\_config\).

2.  Update the following values, for **Virtual Agent Default Search Application**

    -   Search Engine: **AI Search**.
    -   Search Profile: **ESC Portal Default Search Profile**. This dynamic field value is visible after you change the **Search Engine** value.
    For more information, see [Create a search application configuration for AI Search](https://www.servicenow.com/docs/access?context=create-search-app-config-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).


### What to do next

Connect the ServiceNow® instance with the Microsoft SharePoint tenant. Complete the steps from your ServiceNow® account. For more information, see [Connect your ServiceNow instance to a Microsoft SharePoint tenant](setup-sp-ovrvw.md#).

## Connect your ServiceNow instance to a Microsoft SharePoint tenant

Connect your ServiceNow instance with a Microsoft SharePoint tenant. Create custom ServiceNow OAuth connections for Microsoft SharePoint to authenticate ServiceNow requests.

### Before you begin

-   Ensure that you have working knowledge of the [SharePoint developer program](https://developer.microsoft.com/en-us/microsoft-365/dev-program) tools and other resources to configure the application.
-   Ensure that you’re aware of the ServiceNow® integrations.

Role required: sn\_sp\_con.admin and admin.

### Procedure

1.  Navigate to **ServiceNow instance** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message `What kind of OAuth application?`

3.  Select **Connect to a third-party OAuth Provider**.

4.  Create the following registries:

    1.  On the Graph connection form, fill in the fields.

        For a description of the field value, see [Graph connection form](../reference/graph-connection-form.md).

    2.  On the REST connection form, fill in the fields.

        For a description of the field value, see [REST connection form](../reference/rest-connection-form.md).

    3.  Right-click the form header and click **Save**.

5.  **OAuth Entity Profile**
6.  Navigate to the OAuth Entity Profiles \[oauth\_entity\_profile\] table to find the following entries:

    -   `<Graph application registry name>.default_profile`
    -   `<REST application registry name>.default_profile`
    Two system-generated OAuth entity profiles \(REST and Graph\) are created in the OAuth Entity Profiles \[oauth\_entity\_profile\] table. For more information, see [Specify an OAuth profile](https://www.servicenow.com/docs/access?context=t_SpecifyAnOAuthProfile&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

7.  **OAuth Entity Scopes**
8.  Insert a row with the following values in the OAuth Entity Scopes \[oauth\_entity\_scope\] table:

<table id="table_vvw_4rl_s1c"><thead><tr><th>

Graph

</th><th>

REST

</th></tr></thead><tbody><tr><td>

Name: Any name of your choice

</td><td>

Name: Any name of your choice

</td></tr><tr><td>

OAuth Provider: Graph Application Registry record

</td><td>

OAuth Provider: REST Application Registry record

</td></tr><tr><td>

Application: Global

</td><td>

Application: Global

</td></tr><tr><td>

\(For Delegated permissions\) OAuthscope: `offline_access https://graph.microsoft.com/Sites.ReadWrite.All`\(For Application permissions\) OAuthscope: `https://graph.microsoft.com/.default`

</td><td>

OAuth Scope:`https://<instance name>.sharepoint.com/.default`

</td></tr></tbody>
</table>    For more information, see [Specify an OAuth scope](https://www.servicenow.com/docs/access?context=t_SpecifyAnOAuthScope&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

9.  **OAuth Entity Profiles Scopes**
10. Insert a row with the following values in the OAuth Entity Profiles Scopes \[oauth\_entity\_profile\_scope\] table:

    |Graph|REST|
    |-----|----|
    |OAuth Entity Profile: Graph entity profile generated in the OAuth Entity Profiles \[oauth\_entity\_profile\] table.|OAuth Entity Profile: REST entity profile generated in the OAuth Entity Profiles \[oauth\_entity\_profile\] table.|
    |OAuth Entity Scope: Select the graph OAuth Entity Scope \[oauth\_entity\_profile\_scope\] table.|OAuth Entity Scope: Select the REST OAuth Entity Scope \[oauth\_entity\_profile\_scope\] table.|
    |Application: Global|Application: Global|

11. **Credentials**
12. Navigate to **Connections &amp; Credentials** &gt; **Credentials**, and create the OAuth 2.0 credentials:

    1.  On the Graph or REST credential forms, fill in the fields.

<table id="table_qyn_qtg_ywb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your choice.

</td></tr><tr><td>

OAuth entity profile

</td><td>

\(For Graph\) Graph entity profile identified.\(For REST\) REST entity profile identified.

</td></tr></tbody>
</table>    2.  Right-click the form header and click **Save**.

        **Note:** For more information on Entities, Connection &amp; Credential Aliases, see [Configure the SharePoint Graph Root Site Subscription connection and credential alias record](https://www.servicenow.com/docs/access?context=conf-graph-root&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

13. **Connection**
14. Navigate to **Connections &amp; Credentials** &gt; **Connection**, and click **New** to create HTTP\(s\) connections for the following **Graph** or **REST**.

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name: Any name of your choice for Graph|Name: Any name of your choice for REST|
        |Credentials: Select the graph **Credentials**|Credentials: Select the REST **Credentials**|
        |Connection alias: `sn_sp_spoke.MicrosoftSharePointGraph`|Connection alias: `sn_sp_spoke.MicrosoftSharepointOnline`|
        |Connection URL:`https://graph.microsoft.com/v1.0/`|Connection URL: `https://<Host URL of your SharePoint instance>/`|
        |Domain: Global|Domain: Global|

    2.  Right-click the form header and click **Save**.

    For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) and [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

15. **Tenants**
16. Navigate to **Microsoft Sharepoint Online** &gt; **Tenants.**

    1.  Click **New** to create **Graph** or **REST** connections.

    2.  On the form, fill in the fields.

<table id="table_cpv_vvg_ywb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your choice.

</td></tr><tr><td>

Alias

</td><td>

For Graph: `sn_sp_spoke.MicrosoftSharePointGraph`For REST: `sn_sp_spoke.MicrosoftSharepointOnline`

</td></tr><tr><td>

SharePoint root URL

</td><td>

Root URL as `<SiteName>.sharepoint.com`

</td></tr><tr><td>

Tenant ID

</td><td>

Tenant ID required for the Graph or REST connection.

</td></tr><tr><td>

Domain

</td><td>

Global

</td></tr></tbody>
</table>    3.  Right-click the topic header and click **Save**.

    For more information, see [Define tenants](https://www.servicenow.com/docs/access?context=create-tenant&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US), [Configure the SharePoint Graph Root Site Subscription connection and credential alias record](https://www.servicenow.com/docs/access?context=conf-graph-root&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US), and [Create aliases for multiple tenants](https://www.servicenow.com/docs/access?context=create-aliases-sharepoint&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)

17. **Certificates**
18. Navigate to **System definition** &gt; **Certificates** &gt; **Microsoft SharePoint Online Certificate**.

    1.  Attach the file-generated Java Key Store certificate on the Azure AD portal.

        For more information, see [Attach a Java Key Store certificate](https://www.servicenow.com/docs/access?context=set-up-microsoft-sharepoint-online-and-connection-record&version=xanadu&pubname=xanadu-integrate-applications&section=ms-sharept-attachjks&ft:locale=en-US).

    2.  Update the Key store password with the password of the `Java Key Store (.jks)` file.

    3.  Update the type to the Java key store.

    4.  Right-click the topic header and click **Save**.

    For more information, see [Configure the SharePoint Graph Root Site Subscription connection and credential alias record](https://www.servicenow.com/docs/access?context=conf-graph-root&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

19. **JWT keys**
20. Navigate to **System OAuth** &gt; **JWT keys** &gt; **Microsoft SharePoint Online JWT Keys**.

    1.  Update signing key with password of `Certificate (.cer)` file.

    2.  Right-click the topic header and click **Save**.

21. Navigate to **System OAuth** &gt; **JWT providers** &gt; **Microsoft SharePoint Online JWT Provider**.

    1.  Update the **aud** claim with `https://login.microsoftonline.com/<Tenant-id>/oauth2/token`.

    2.  Update the **iss** and **sub** claim with the respective client ids on the Azure ad app registrations.

    3.  Click **Save**.

22. **Connection**
23. Navigate to **Connections &amp; Credentials** &gt; **Connection**.

    1.  Open the REST connection record and on the **Attributes** tab, specify the Base64 encoded certificate **Thumbprint**.

        **Note:** The SharePoint app thumbprint value is hex encoded. Encode the same in the Base64 format in the connection record.

    2.  Select the following **Credentials** option:

        -   \(For **Graph**\): Navigate to the \[Credentials\] table \(oauth\_2\_0\_credentials\), open **Graph**, and click **Get OAuth Token**.

            Ensure that you log in to your Microsoft SharePoint instance with the credentials of the user that you created to get the OAuth token for the Graph connection. Store the credentials in the instance.

        -   \(For **REST**\): Go to the \[Credentials\] table \(oauth\_2\_0\_credentials\), open **REST**, and click **Get OAuth Token**.

            Ensure that you log in to your Microsoft SharePoint instance with the Tenant administrator credentials to get the OAuth token for the REST connection. Store the credentials in the instance. Validate the credential to avoid any configuration failure.

    3.  Click **Save**.

24. **Trusted Domains**
25. Go to **Trusted Domains** table \(sn\_ais\_spoke\_trusted\_domains\) and click **New** to create a domain record.

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of your choice.|
        |Domain|&lt;Host URL of your Microsoft SharePoint tenant&gt;.|

    2.  Click **Save**.

        For more information, see [Set up the AI Search spoke](https://www.servicenow.com/docs/access?context=setup-ais-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

        **Note:** Ensure you create a trusted domain record for each tenant, when there are multiple tenants.

26. **Sharepoint Ingest User**
27. Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases** &gt; **Sharepoint Ingest User** \(sn\_sp\_con.Sharepoint\_Ingest\_User\).

    1.  Click **New** on **Credentials** to create a **Basic Auth Credential** for ingesting external content by AIS.

    2.  Specify the **User name** and **Password** of the user \(sys\_user\) who has the **ais\_external\_content** role.

        ![ingest user](../image/spoc-ingest-user.png)

        **Note:** In the example screenshot, the user `abel.tuter` is the sys\_user who has the ais\_external\_content role assigned.

    3.  Click **Submit**.

        For more information, see [Create aliases for multiple tenants](https://www.servicenow.com/docs/access?context=create-aliases-sharepoint&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    4.  Configure the [AI Search server connection](https://www.servicenow.com/docs/access?context=setup-ais-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) before you proceed with the next steps.

    The Entity View Action Mapper \(EVAM\) configuration is available by default with Employee Center Pro version 32.0.

    For more information on EVAM definition, see [Create an EVAM action definition](https://www.servicenow.com/docs/access?context=define-evam-action&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) and [Create a multi-data source list display in Entity View Action Mapper](https://www.servicenow.com/docs/access?context=tutorial-create-evam&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


### Result

Your configuration is complete.

### What to do next

Index the sites for search. For more information, see [Index sites for search](sharepoint-how-to-configure-search.md).

