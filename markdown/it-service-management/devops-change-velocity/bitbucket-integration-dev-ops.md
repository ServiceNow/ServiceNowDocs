---
title: Bitbucket integration with DevOps Change Velocity
description: Connect to your Bitbucket instance to track Bitbucket repositories, commits, branches, and pull requests.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Bitbucket integration with DevOps Change Velocity

Connect to your Bitbucket instance to track Bitbucket repositories, commits, branches, and pull requests.

## Bitbucket integration overview

DevOps Change Velocity supports the Code \(Repository\) capability for the Bitbucket tool.

## Authentication methods

You can connect to Bitbucket Cloud using one of the following authentication methods:

-   **Basic Auth**

    When you select the credential type as Basic Auth the repositories for all the workspaces in the organization are discovered. You can get the user name and password for Basic Auth from the settings of your Bitbucket account. To copy the user name, navigate to **Settings &gt; General &gt; Account settings**, and copy the user name from the Bitbucket profile settings section. To copy the password, navigate to **Settings &gt; Personal Bitbucket settings &gt; App passwords**, and select **Create app password**. Enter the necessary details and select the required permissions, and then select **Create**, and copy the password. The following permissions must be selected while creating the credentials:

    -   Account: Read
    -   Projects: Read
    -   Webhooks: Read and write
    -   Pull requests: Read
    ![Permissions for Bitbucket basic auth](../image/bitbucket-oauth-permissions.png)

-   **OAuth 2.0 - Authorization Code**

    You must create the OAuth consumer in the Bitbucket tool with the required permissions before creating the OAuth record for Authorization Code. You can navigate to **Workspace settings &gt; OAuth consumers &gt; Add consumer** in Bitbucket to add the OAuth consumer. ![OAuth consumer page](../image/bitbucket-oauth-consumer.png) Select the following permissions for the OAuth consumer.

    -   Account: Read
    -   Projects: Read
    -   Webhooks: Read and write
    -   Pull requests: Read
    Ensure that the **This is a private consumer** option isn’t selected. You must enter your ServiceNow instance URL in the **Callback URL** field in the following format.

    ```
    https://<instanceurl>/oauth_redirect.do
    ```

    ![Permissions for Bitbucket OAuth 2.0 - Authorization Code](../image/bitbucket-oauth-permissions-auth-code.png)

    You can create an OAuth 2.0 - Authorization Code credential by performing the steps specified in the [Set up OAuth 2.0 Authorization Code for Bitbucket Cloud](../task/set-up-oauth-2-0-authorization-code.md) procedure.

    **Note:** When you select the credential type as Oauth 2.0 - Authorization Code for Bitbucket Cloud, the repositories for all the workspaces are discovered. This is a limitation from Bitbucket side

-   **OAuth 2.0 - Client Credentials**

    You must create the OAuth consumer in the Bitbucket tool with the required permissions before creating the OAuth record for Client Credentials. You can navigate to **Workspace settings &gt; OAuth consumers &gt; Add consumer** in Bitbucket to add the OAuth consumer. ![OAuth consumer page](../image/bitbucket-oauth-consumer.png) Select the following permissions for the OAuth consumer.

    -   Account: Read
    -   Projects: Read
    -   Webhooks: Read and write
    -   Pull requests: Read
    Ensure that the **This is a private consumer** option is selected as well. You must enter your ServiceNow instance URL in the **Callback URL** field in the following format.

    ```
    https://<instanceurl>/oauth_redirect.do
    ```

    ![Permissions for Bitbucket OAuth 2.0 - Client Credentials](../image/bitbucket-oauth-client-credentials.png)

    You can create an OAuth 2.0 - Client Credential record in the workspace UI while onboarding the tool. You need the **Client Id** and **Client secret** values of your Bitbucket workspace. Client ID of your Bitbucket tool is available in the OAuth consumers section of your workspace settings \(**Workspace settings &gt; OAuth consumers &gt; Add consumer**\) in the **Key** field. Client secret of your Bitbucket tool is available in the OAuth consumers section of your workspace settings \(**Workspace settings &gt; OAuth consumers &gt; Add consumer**\) in the **Secret** field. ![OAuth consumer page](../image/bitbucket-oauth-consumer.png)

-   **Access Token**

    You can create the access token by performing the steps specified in the [Atlassian](https://support.atlassian.com/bitbucket-cloud/docs/create-a-workspace-access-token/) documentation. Ensure that the following permissions are provided while creating the access token:

    -   Account: Read
    -   Projects: Read
    -   Webhooks: Read and write
    -   Pull requests: Read
    ![Create Access Token in Bitbucket](../image/bitbucket-access-token.png)

    You also need the workspace ID of your Bitbucket workspace. Copy it from the **Workspace ID** field in the Workspace settings of your Bitbucket Cloud account.


## Get started

Use one of the following options to onboard Bitbucket. For a guided experience, use the workspace to onboard a tool. Alternatively, you can use the Service Catalog or Classic experience.

-   **[Onboard Bitbucket to DevOps Change Velocity — Workspace](../task/devops-wkspc-bitbucket-tool-conn.md)**  
Create, connect, discover, and configure your Bitbucket instance using the DevOps Change Velocity workspace.
-   **[Onboard Bitbucket to DevOps Change Velocity — Service Catalog](../task/sc-bitbucket.md)**  
Create, connect, discover, and configure your Bitbucket instance using the ServiceNow Service Catalog.
-   **[Onboard Bitbucket to DevOps Change Velocity — Classic](../task/onboard-bitbucket-to-devops-change-velocity-classic.md)**  
Create, connect, discover, and configure your Bitbucket instance using the Classic UI.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

