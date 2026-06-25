---
title: Bitbucket integration with DevOps Change Velocity
description: Connect to your Bitbucket instance to track Bitbucket repositories, commits, branches, and pull requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/bitbucket-integration-dev-ops.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Bitbucket integration with DevOps Change Velocity

Connect to your Bitbucket instance to track Bitbucket repositories, commits, branches, and pull requests.

## Bitbucket integration overview

DevOps Change Velocity supports the Code \(Repository\) capability for the Bitbucket tool.

## Authentication methods

You can connect to Bitbucket Cloud using one of the following authentication methods:

-   **Basic Auth**

    When you select the credential type as Basic Auth the repositories for all the workspaces in the organization are discovered. You need the email address and API token with scopes of your Bitbucket Cloud account to connect using Basic Auth. You can copy your email address by navigating to **Profile avatar &gt; Personal settings &gt; Account settings &gt; Email** of your Bitbucket Cloud account.

    To get the API token with scopes, perform the following steps:

    1.  Select your profile avatar at the bottom-left of the Bitbucket sidebar, then select **Account settings**.
    2.  From the Atlassian Account page, select the **Security** tab on the top navigation bar.
    3.  Select **Create and manage API tokens**.
    4.  Select **Create API token with scopes**.
    5.  Give the API token a name and an expiry date, usually related to the application that will use the token and select **Next**.
    6.  Select **Bitbucket** as the app and select **Next**.
    7.  Select the following scopes \(permissions\) and select **Next**.

        -   read:account — Required to view users profiles.
        -   read:project:bitbucket — View your projects
        -   read:pullrequest:bitbucket — View your pull requests
        -   read:repository:bitbucket — View your repositories
        -   read:webhook:bitbucket — View your webhooks
        -   write:webhook:bitbucket — Modify your webhooks
        \[Omitted image "bitbucket-oauth-permissions.png"\] Alt text: Permissions for Bitbucket basic auth

    8.  Review your token and select the **Create token** button.
    9.  Copy the generated API token and either record or paste it into the application you want to give access.
-   **OAuth 2.0 - Authorization Code**

    You must create the OAuth consumer in the Bitbucket tool with the required permissions before creating the OAuth record for Authorization Code. You can navigate to **Workspace settings &gt; OAuth consumers &gt; Add consumer** in Bitbucket to add the OAuth consumer. \[Omitted image "bitbucket-oauth-consumer.png"\] Alt text: OAuth consumer page Select the following permissions for the OAuth consumer.

    -   Account: Read
    -   Projects: Read
    -   Webhooks: Read and write
    -   Pull requests: Read
    Ensure that the **This is a private consumer** option isn’t selected. You must enter your ServiceNow instance URL in the **Callback URL** field in the following format.

    ```
    https://<instanceurl>/oauth_redirect.do
    ```

    \[Omitted image "bitbucket-oauth-permissions-auth-code.png"\] Alt text: Permissions for Bitbucket OAuth 2.0 - Authorization Code

    You can create an OAuth 2.0 - Authorization Code credential by performing the steps specified in the [Set up OAuth 2.0 Authorization Code for Bitbucket Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/set-up-oauth-2-0-authorization-code.md) procedure.

    **Note:** When you select the credential type as Oauth 2.0 - Authorization Code for Bitbucket Cloud, the repositories for all the workspaces are discovered. This is a limitation from Bitbucket side

-   **OAuth 2.0 - Client Credentials**

    You must create the OAuth consumer in the Bitbucket tool with the required permissions before creating the OAuth record for Client Credentials. You can navigate to **Workspace settings &gt; OAuth consumers &gt; Add consumer** in Bitbucket to add the OAuth consumer. \[Omitted image "bitbucket-oauth-consumer.png"\] Alt text: OAuth consumer page Select the following permissions for the OAuth consumer.

    -   Account: Read
    -   Projects: Read
    -   Webhooks: Read and write
    -   Pull requests: Read
    Ensure that the **This is a private consumer** option is selected as well. You must enter your ServiceNow instance URL in the **Callback URL** field in the following format.

    ```
    https://<instanceurl>/oauth_redirect.do
    ```

    \[Omitted image "bitbucket-oauth-client-credentials.png"\] Alt text: Permissions for Bitbucket OAuth 2.0 - Client Credentials

    You can create an OAuth 2.0 - Client Credential record in the workspace UI while onboarding the tool. You need the **Client Id** and **Client secret** values of your Bitbucket workspace. Client ID of your Bitbucket tool is available in the OAuth consumers section of your workspace settings \(**Workspace settings &gt; OAuth consumers &gt; Add consumer**\) in the **Key** field. Client secret of your Bitbucket tool is available in the OAuth consumers section of your workspace settings \(**Workspace settings &gt; OAuth consumers &gt; Add consumer**\) in the **Secret** field. \[Omitted image "bitbucket-oauth-consumer.png"\] Alt text: OAuth consumer page

-   **Access Token**

    You can create the access token by performing the steps specified in the [Atlassian](https://support.atlassian.com/bitbucket-cloud/docs/create-a-workspace-access-token/) documentation. Ensure that the following permissions are provided while creating the access token:

    -   Account: Read
    -   Projects: Read
    -   Webhooks: Read and write
    -   Pull requests: Read
    \[Omitted image "bitbucket-access-token.png"\] Alt text: Create Access Token in Bitbucket

    You also need the workspace ID of your Bitbucket workspace. Copy it from the **Workspace ID** field in the Workspace settings of your Bitbucket Cloud account.


## Get started

Use one of the following options to onboard Bitbucket. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard Bitbucket to DevOps Change Velocity — Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/devops-wkspc-bitbucket-tool-conn.md)**  
Create, connect, discover, and configure your Bitbucket instance using the DevOps Change Velocity workspace.
-   **[Onboard Bitbucket to DevOps Change Velocity — Service Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/sc-bitbucket.md)**  
Create, connect, discover, and configure your Bitbucket instance using the ServiceNow Service Catalog.
-   **[Onboard Bitbucket to DevOps Change Velocity — Classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/onboard-bitbucket-to-devops-change-velocity-classic.md)**  
Create, connect, discover, and configure your Bitbucket instance using the Classic UI.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/integrating-devops-change-with-third-party-tools.md)

