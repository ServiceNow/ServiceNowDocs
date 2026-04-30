---
title: Set up the GitHub spoke
description: Integrate your ServiceNow instance with the GitHub and GitHub Enterprise Server to automate flows and perform actions on GitHub and GitHub Enterprise Server. For example, create a flow that creates a branch on GitHub and retrieves its details.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [GitHub Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the GitHub spoke

Integrate your ServiceNow instance with the GitHub and GitHub Enterprise Server to automate flows and perform actions on GitHub and GitHub Enterprise Server. For example, create a flow that creates a branch on GitHub and retrieves its details.

Demonstrates integrating the ServiceNow instance with GitHub and GitHub Enterprise Server.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the GitHub spoke.
-   An account with GitHub to create personal access tokens.
-   If you are using GitHub Enterprise server, an account to create personal access tokens.
-   Role required: admin.

## Procedure

1.  Generate a personal access token in GitHub account.

    1.  Log in to [https://github.com/](https://github.com/).

    2.  On the dashboard, select your profile icon.

        ![GitHub profile icon.](../image/github-spoke-profile-icon.png)

    3.  Select **Settings**.

    4.  In the Settings page, on the left panel, select **Developer settings**.

    5.  In the Developer settings page, on the left panel, navigate to **Personal access tokens** &gt; **Tokens \(classic\)**.

    6.  Select **Generate new token** &gt; **Generate new token \(classic\)**.

    7.  In **Note**, enter a description or purpose of the personal access token.

    8.  In **Expiration**, set the expiry period of the token or select No expiration.

    9.  Under the **Select scopes** heading, select the scopes that define the access for the personal access token you’re generating.

    10. Select **Generate token**.

        The personal access token is generated.

    11. To copy the personal access token, select the copy button.

        ![Personal access token copy button.](../image/github-spoke-copy-token-button.png)

        **Important:** Keep the personal access token at a secure place. You’ll need it when you create a connection record for GitHub.

2.  Configure the connection record that connects your ServiceNow instance with GitHub.

    1.  Log in to your ServiceNow.

    2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    3.  Click the **Integrations** tab.

    4.  Under **Connections**, toggle and enable the **Outbound** connections.

    5.  Locate the **GitHub** connection alias and click **View Details**.

        If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    6.  On the form, fill the details.

<table id="table_azk_3qd_s1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection. **Note:** The default and read-only name of the first connection record is **GitHub**.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to GitHub. Enter [https://api.github.com](https://api.github.com).

</td></tr><tr><td>

Use Mid Server

</td><td>

-   Enter `1` if your ServiceNow instance requires a MID Server to connect with GitHub.
-   Enter `0` if your ServiceNow instance does not require a MID Server to connect with GitHub.
 **Important:** To enable this option, you must already have a MID Server set up on your instance. See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for detailed instructions.

</td></tr><tr><td>

API Key

</td><td>

Personal access token that you had generated on GitHub.

</td></tr></tbody>
</table>    7.  Select **Create Connection**.

        The GitHub connection record is created.

3.  If you are using GitHub Enterprise server, configure the **GitHub Server** connection.

    **Important:** Generate a personal access token on the GitHub Enterprise server.

    To learn to generate a personal access token on the GitHub Enterprise server, see [Integrate with GitHub Enterprise Server](https://www.servicenow.com/docs/access?context=integrating-with-github-server&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).

    1.  Select the GitHub Server connection card.

    2.  Select **View Details**.

    3.  Fill the form.

<table id="table_x21_g1j_syb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

The name of the connection. **Note:** The default and read-only name of the first connection record is GitHub Server. To create a connection with your custom name, select **Add Connection** and fill the form.

</td></tr><tr><td>

Connection URL

</td><td>

URL of your GitHub instance.

</td></tr><tr><td>

Use Mid Server

</td><td>

-   Enter `1` if your ServiceNow instance requires a MID Server to connect with the GitHub Enterprise server.
-   Enter `0` if your ServiceNow instance does not require a MID Server to connect with the GitHub Enterprise server.
 **Important:** To enable this option, you must already have a MID Server set up on your instance. See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for detailed instructions.

</td></tr><tr><td>

API Key

</td><td>

Personal access token that you had generated on the GitHub Enterprise Server.

</td></tr></tbody>
</table>    4.  Select **Create Connection**.

        The GitHub Enterprise Server connection record is configured.


