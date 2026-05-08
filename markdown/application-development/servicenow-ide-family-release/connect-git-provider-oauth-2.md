---
title: Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE
description: Set up an OAuth 2.0 application registry and credentials to connect to your Git provider from the ServiceNow IDE.Configure how the client ID and secret are sent to the OAuth 2.0 provider associated with your Git provider.Connect to a Git domain using OAuth 2.0 credentials to manage applications in source control from the ServiceNow IDE.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integrate source control, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE

Set up an OAuth 2.0 application registry and credentials to connect to your Git provider from the ServiceNow IDE.

**Parent Topic:**[Integrating source control with the ServiceNow IDE](integrating-source-control-servicenow-ide.md)

**Related topics**  


[Connect to a Git provider using basic authentication with the ServiceNow IDE](../task/connect-git-provider-basic-auth.md)

[Configure a MID Server to use source control with the ServiceNow IDE](../task/configure-mid-server-source-control.md)

[Initialize a Git repository with the ServiceNow IDE](../task/initialize-git-repository-servicenow-ide.md)

[Using source control in the ServiceNow IDE](using-source-control-servicenow-ide.md)

## Configure an OAuth 2.0 application registry for the ServiceNow IDE

Configure how the client ID and secret are sent to the OAuth 2.0 provider associated with your Git provider.

### Before you begin

Create an OAuth application with your Git provider and configure it to redirect to your instance. In this OAuth application, use your instance URL as the homepage URL and `https://<instance>/oauth_redirect.do` for the authorization callback URL. GitHub, GitLab, Bitbucket, and Azure Repos are supported by default.

**Important:** For Azure Repos, the maximum length of the **Client Secret** field must be updated to 2048 before you add the secret.

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.
2.  Filter the table by entering `oauth_entity` for the **Name** field.
3.  Select the Application Registries \[oauth\_entity\] table.
4.  In the Columns related list, locate the Client Secret column and enter `2048` as the value of its **Max length** attribute.
5.  Select **Update**.

Role required: admin

### About this task

To use OAuth 2.0 authentication with the ServiceNow IDE, you must register the OAuth application you created from your Git provider. Follow this procedure to configure an OAuth application registry \[oauth\_entity\] on your instance.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and then select **New**.

2.  On the interceptor page, select **Connect to a third-party OAuth provider**.

3.  On the form, fill in the fields.

    For additional information about fields on the form, see Connect to a third-party OAuth provider.

<table id="table_sgc_qqv_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for the third-party OAuth connection.

</td></tr><tr><td>

Client ID

</td><td>

The client ID of the OAuth application in your Git provider.

</td></tr><tr><td>

Client Secret

</td><td>

The client secret of the OAuth application in your Git provider.

</td></tr><tr><td>

OAuth API Script

</td><td>

The script used to customize request and response to the external OAuth provider. Select one of the following depending on your Git provider:-   GitHub: OauthAPIScriptForGitHub
-   GitLab: OauthAPIScriptForGitLab
-   Bitbucket: OauthAPIScriptForBitbucket
-   Azure Repos: OauthAPIScriptForAzureRepos
**Note:** To use other Git providers, you can use these scripts as examples to create your own OAuth API script for your OAuth provider. The name of the script must begin with “Oauth”.

</td></tr><tr><td>

Default Grant type

</td><td>

The default grant type used to establish the token. Select **Authorization code**.An authorization code is granted to the client to obtain an access token, which is then used to obtain access to the resource.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

The time, in seconds, that the refresh token is valid.

</td></tr><tr><td>

Application

</td><td>

The application scope that contains this record.

</td></tr><tr><td>

Accessible from

</td><td>

An option to make the application registry accessible from all application scopes or from this scope only.

</td></tr><tr><td>

Active

</td><td>

An option for turning the OAuth application on or off.

</td></tr><tr><td>

Authorization URL

</td><td>

The OAuth authorization code endpoint for your Git domain. For example:-   GitHub: `https://github.com/login/oauth/authorize`
-   GitLab: `https://gitlab.com/oauth/authorize`
-   Bitbucket: `https://bitbucket.org/site/oauth2/authorize`
-   Azure Repos: `https://app.vssps.visualstudio.com/oauth2/authorize`


</td></tr><tr><td>

Token URL

</td><td>

The OAuth server token endpoint for your Git domain. For example:-   GitHub: `https://github.com/login/oauth/access_token`
-   GitLab: `https://gitlab.com/oauth/token`
-   Bitbucket: `https://bitbucket.org/site/oauth2/access_token`
-   Azure Repos: `https://app.vssps.visualstudio.com/oauth2/token`


</td></tr><tr><td>

Redirect URL

</td><td>

The OAuth callback endpoint. If empty, the instance auto-generates a value of `https://<instance>/oauth_redirect.do`.

</td></tr><tr><td>

Use mutual authentication

</td><td>

An option to use mutual authentication. Leave this option cleared to turn off using mutual authentication for token request and revocation.

</td></tr><tr><td>

Send Credentials

</td><td>

The way in which the OAuth client populates the client credentials in the request. -   For GitHub, GitLab, or Bitbucket, select **As Basic Authorization header**.
-   For Azure Repos, select **In Request Body \(Form URL-Encoded\)**.


</td></tr></tbody>
</table>4.  Select **Submit**.


### What to do next

Developers using the ServiceNow IDE must configure their own OAuth 2.0 credentials.

## Configure OAuth 2.0 credentials to connect to a Git provider with the ServiceNow IDE

Connect to a Git domain using OAuth 2.0 credentials to manage applications in source control from the ServiceNow IDE.

### Before you begin

-   An administrator must configure how the client ID and secret are sent to the OAuth 2.0 provider associated with your Git provider. For more information, see [Configure an OAuth 2.0 application registry for the ServiceNow IDE](connect-git-provider-oauth-2.md#).
-   Create a dedicated Git repository for an application in a Git provider such as GitHub, GitLab, Bitbucket, or Azure Repos.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
3.  Enter `Git: Set IDE Git credentials` and press Enter.

4.  From the New Git credential form, select **OAuth**.

5.  On the form, fill in the fields.

<table id="table_lxq_myn_sbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Git repository URL

</td><td>

The HTTPS URL of a Git repository associated with your Git credentials.

</td></tr><tr><td>

Git username

</td><td>

Your Git user name.

</td></tr><tr><td>

Select an OAuth profile

</td><td>

The OAuth 2.0 credentials for your Git provider. The OAuth profile is created with the application registry, which must be configured by an administrator.

</td></tr></tbody>
</table>6.  Select **Submit**.

    The first time you use a Git command, you're prompted to authorize your user from the Git provider.


### Result

Your Git credentials are associated with your user on the instance and used for all repositories in the domain from the Git repository URL. If you add different credentials for a repository in the same domain, the new credentials are used and the previous credentials are set to inactive.

### What to do next

After initializing or cloning a repository, you can begin using source control. For more information, see [Using source control in the ServiceNow IDE](using-source-control-servicenow-ide.md).

To manage existing Git credentials, use the `Git: Manage Git credentials` command from the command palette.

