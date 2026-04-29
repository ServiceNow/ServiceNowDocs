---
title: Configure GitHub Enterprise Cloud for external content indexing
description: Create and authorize a GitHub App to allow the GitHub Enterprise Cloud external content connector to access your GitHub Enterprise Cloud content.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [GitHub Enterprise Cloud external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure GitHub Enterprise Cloud for external content indexing

Create and authorize a GitHub App to allow the GitHub Enterprise Cloud external content connector to access your GitHub Enterprise Cloud content.

## Before you begin

You need all of the following:

-   The Organization Owner role for your GitHub Enterprise Cloud organization. For details on this role, see the [https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization](https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization) and [https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/maintaining-ownership-continuity-for-your-organization](https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/maintaining-ownership-continuity-for-your-organization) GitHub documentation resources.
-   Access to a programming language that you can use to create a JSON Web Token \(JWT\) for a GitHub App, such as Ruby, Python, bash, or PowerShell. For details on this procedure and the supported programming languages, see the [https://docs.github.com/en/enterprise-cloud@latest/apps/creating-github-apps/authenticating-with-a-github-app/generating-a-json-web-token-jwt-for-a-github-app](https://docs.github.com/en/enterprise-cloud@latest/apps/creating-github-apps/authenticating-with-a-github-app/generating-a-json-web-token-jwt-for-a-github-app) GitHub documentation resource.
-   Access to the curl command-line tool.

Role required: none

## About this task

The GitHub Enterprise Cloud external content connector retrieves searchable content and metadata from commits, issues, and pull requests found in your GitHub Enterprise Cloud source system's public and internal repositories using the GitHub REST API.

To allow the connector to access your GitHub Enterprise Cloud source system via the REST API, you must configure and authorize a GitHub App for your organization in GitHub Enterprise Cloud. Your connector admin can use settings copied from the GitHub App to configure the GitHub Enterprise Cloud external connector for proper connection to your source system.

## Procedure

1.  Create a new GitHub App for the GitHub Enterprise Cloud external content connector.

    1.  Navigate to [https://github.com/](https://github.com/) and log in with your GitHub Enterprise Cloud credentials.

    2.  Select your profile picture, then select **Your enterprise** from the context menu.

        If you don't use Enterprise Managed Users, select **Your enterprises**, then select **Settings**.

    3.  In the menu, navigate to **Settings** &gt; **Developer Settings** &gt; **GitHub Apps**.

    4.  Select **New GitHub App**.

    5.  On the Register new GitHub App page, enter a name for your new GitHub App.

        As an example, you might enter `External content connector`.

        **Note:** The App name can't exceed 34 characters in length.

    6.  In the **Homepage URL** field, enter the URL for your organization's GitHub account.

        As an example, you might enter `https://github.com/example`.

    7.  In the Webhook section, clear the **Active** option.

    8.  In the Permissions section, expand the Repository permissions list and select **Read-only** access for each of these permissions.

        -   Commit statuses
        -   Contents
        -   Discussions
        -   Issues
        -   Merge queues
        -   Pull requests
    9.  In the Permissions section, expand the Organization permissions list and select **Read-only** access for the **Members** permission.

    10. In the **Where can this GitHub App be installed?** field, select the **Only on this account** option.

    11. Select **Create GitHub App**.

    A message indicates that your new GitHub App was successfully registered, and you're taken to its General settings page.

2.  Get the client ID and private key for your new GitHub App from its General settings page.

    1.  In the About section, copy the client ID for your new GitHub App and store it in a secure location.

        **Important:** Your external content connector admin needs this client ID when configuring the GitHub Enterprise Cloud external content connector.

    2.  In the Private keys section, select **Generate a private key**.

    3.  When prompted, download the PEM-format private key certificate file to a secure location.

        **Important:** Your external content connector admin needs this PEM-format private key certificate file when configuring the GitHub Enterprise Cloud external content connector.

3.  Install your new GitHub App.

    1.  In the menu for your new GitHub App, select **Install App**.

    2.  In the entry for your GitHub organization account, select **Install**.

    3.  On the Install page for your new GitHub App, choose which repositories you want the external content connector to have access to.

        -   To grant the external content connector access to all repositories owned by your organization, select **All repositories**.
        -   To grant the external content connector access to a specified set of repositories owned by your organization, select **Only select repositories**, then use the **Select repositories** drop-down list to find and select the repositories you want to grant the connector access to.
    4.  Select **Install**.

4.  Get the App Installation ID for your new GitHub App.

    1.  Get the identifier for your GitHub organization from the URL for your GitHub organization page.

        The identifier for your organization is the URL element after the third slash in the URL for your GitHub organization page. As an example, if the URL for your GitHub organization page is `https://github.com/example`, the identifier for your organization is `example`.

    2.  Generate a JSON Web Token \(JWT\) for your new GitHub App.

        For details on generating a JWT for a GitHub App using Ruby, Python, bash, or PowerShell, see the [https://docs.github.com/en/enterprise-cloud@latest/apps/creating-github-apps/authenticating-with-a-github-app/generating-a-json-web-token-jwt-for-a-github-app](https://docs.github.com/en/enterprise-cloud@latest/apps/creating-github-apps/authenticating-with-a-github-app/generating-a-json-web-token-jwt-for-a-github-app) GitHub documentation resource.

        To generate a JWT, you need the client ID that you copied in step [2.a](configure-github-enterprise-cloud-external-content-indexing.md#copy-client-id-step) and the PEM-format client secret certificate file that you downloaded in step [2.c](configure-github-enterprise-cloud-external-content-indexing.md#copy-client-secret-step).

        **Important:** Your JWT expires 10 minutes after creation. If it expires before you can perform the next step, repeat this step to generate a new JWT.

    3.  Execute the following curl command, replacing `<org>` with the identifier for your GitHub organization and `<json-web-token>` with the JWT you generated.

        ```bourne
        curl --request GET \
          --url "https://api.github.com/orgs/<org>/installation" \
          --header "Accept: application/vnd.github+json" \
          --header "Authorization: Bearer <json-web-token>" \
          --header "X-GitHub-Api-Version: 2022-11-28"
        ```

    4.  In the JSON response object, find the application installation's `id` key-value pair, copy its value, and store it in a secure location.

        **Important:** Your external content connector admin needs this App Installation ID when configuring the GitHub Enterprise Cloud external content connector.


## What to do next

Provide the following items to your connector admin:

-   The client ID that you copied in step [2.a](configure-github-enterprise-cloud-external-content-indexing.md#copy-client-id-step).
-   The PEM-format private key certificate file that you downloaded in step [2.c](configure-github-enterprise-cloud-external-content-indexing.md#copy-client-secret-step).
-   The app installation ID that you copied in step [4.d](configure-github-enterprise-cloud-external-content-indexing.md#copy-app-installation-id-step).

Your connector admin needs these items to configure a GitHub Enterprise Cloud external content connector to retrieve items and security principals from your GitHub Enterprise Cloud source system.

For details on creating and configuring a GitHub Enterprise Cloud external content connector, see [Create a GitHub Enterprise Cloud external content connector](create-ext-cont-connector-github-enterprise-cloud.md).

**Parent Topic:**[GitHub Enterprise Cloud external content connector](../concept/github-enterprise-cloud-external-content-connector.md)

