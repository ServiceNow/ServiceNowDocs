---
title: OAuth 2.0 credentials for GitHub Apps - Authorization Code
description: Perform the following steps to integrate your GitHub Apps using Authorization code.Create a custom GitHub App from your GitHub account to enable OAuth 2.0 authentication with your ServiceNow instance.Use the information generated during GitHub App account configuration to register GitHub as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create a credential record to the GitHub App provider previously created to authorize actions.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up GitHub OAuth 2.0 credentials for DevOps Change Velocity, GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# OAuth 2.0 credentials for GitHub Apps - Authorization Code

Perform the following steps to integrate your GitHub Apps using Authorization code.

**Before you begin**

Role required:

-   oauth\_admin in DevOps Change Velocity.
-   Admin account in GitHub.

**Note:** Only user-level repositories are supported. You must have access to all the GitHub repositories that you want to configure in DevOps Change Velocity using Authorization code.

The OAuth Authorization Code grant type is supported for GitHub &amp; GitHub Enterprise with MID server.

## Configure the GitHub App in your GitHub account \(Authorization Code\)

Create a custom GitHub App from your GitHub account to enable OAuth 2.0 authentication with your ServiceNow instance.

### Before you begin

GitHub requirement: GitHub App configured to integrate with ServiceNow

Role required: No instance role required

### About this task

Complete these steps from your GitHub account. See [Building GitHub Apps](https://developer.github.com/apps/building-github-apps/) on the GitHub Developer site for instructions on creating and configuring custom applications.

### Procedure

1.  From your GitHub account, create your GitHub App by navigating to **Developer Settings** &gt; **GitHub Apps**.

2.  In the **Homepage URL** field, enter `https://<instance-name>.service-now.com`.

3.  In the **User authorization callback URL** field, enter `https://<instance-name>.service-now.com/oauth_redirect.do`.

4.  In the **Identifying and authorizing users** section, deselect the **Expire user authorization tokens** field.

5.  In the **Webhook** section, deselect the **Active** field.

6.  Leave the remaining fields empty \(default\).

7.  In the **Repository permissions** section, configure these settings.

<table id="table_j5m_wcs_4mb"><tbody><tr><td>

Action

</td><td>

Read-only

</td></tr><tr><td>

Checks

</td><td>

Read-only

</td></tr><tr><td>

Contents

</td><td>

Read-only

</td></tr><tr><td>

Deployments

</td><td>

Read and write

</td></tr><tr><td>

Environments

</td><td>

Read-only

</td></tr><tr><td>

Metadata

</td><td>

Read-only

</td></tr><tr><td>

Pull requests

</td><td>

Read-only

</td></tr><tr><td>

Secrets

</td><td>

Read-only

</td></tr><tr><td>

Webhooks

</td><td>

Read and write**Note:** Read and write permissions are required to configure webhooks from ServiceNow.

</td></tr></tbody>
</table>8.  Leave the remaining permissions as `No access` \(default\).

9.  Install the newly created GitHub App on the accounts of your choice.


## Register GitHub as an OAuth Provider \(Authorization Code\)

Use the information generated during GitHub App account configuration to register GitHub as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin, sn\_devops.admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message **What kind of OAuth application?**

3.  Select **Connect to a third party OAuth Provider**.

    The system displays an empty Application Registries form.

4.  Complete the form.

<table id="table_fd2_2xr_4mb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record. For example, enter `My GitHub App Provider`.

</td></tr><tr><td>

Client ID

</td><td>

Enter the client ID of your GitHub App \(hint: available in the **About** section of your GitHub App configuration in GitHub \).

</td></tr><tr><td>

Client Secret

</td><td>

Enter the client secret of your GitHub App \(hint: available in the **About** section of your GitHub App configuration in GitHub \).

</td></tr><tr><td>

OAuth API script

</td><td>

Select **OAuthDevOpsGitHubHandler**.

</td></tr><tr><td>

Default Grant type

</td><td>

Select **Authorization Code**.

</td></tr><tr><td>

Authorization URL

</td><td>

Enter `https://github.com/login/oauth/authorize`.

 For an on-premises deployment, use the proper GitHub host URL.

</td></tr><tr><td>

Token URL

</td><td>

Enter `https://github.com/login/oauth/access_token`.

 For an on-premises deployment, use the proper GitHub host URL.

</td></tr></tbody>
</table>5.  Leave the rest of the form fields as default.

    ![Application Registry form](../image/github-oauth-auth-app-registries.png)

6.  Right-click the form header, and click **Save**.

    -   The system validates the OAuth credentials and populates the **Redirect URL** \(Hint: It should match the **User authorization callback URL** previously provided in your GitHub App configuration\).
    -   The system populates **OAuth Entity Profile** with **Grant Type** as **Authorization Code**. For example, **OAuth Entity Profile** is created with default **Name**, **My GitHub App Provider default\_profile**

## Create a credential record for GitHub App provider \(Authorization Code\)

Create a credential record to the GitHub App provider previously created to authorize actions.

### Before you begin

Role required: admin, credential\_admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays an empty OAuth 2.0 Credentials form.

4.  Fill in these values.

<table id="table_sxv_zgp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record. For example, enter `My GitHub App Credential`.

</td></tr><tr><td>

Active

</td><td>

Enable

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

Select the default OAuth Entity profile you created previously.

</td></tr><tr><td>

Applies to

</td><td>

Select the MID Servers that can use this credential. For example, select **All MID Servers**.**Note:** You must connect to your GitHub tool instance using MID Server to use this credential.

</td></tr><tr><td>

Order

</td><td>

Select the order to apply this credential. For example, enter `100`.

</td></tr></tbody>
</table>5.  Save the record.

6.  Click the **Get OAuth Token** related link to generate the OAuth token.


**Related topics**  


[GitHub Actions configurations](github-actions-integration-with-devops.md#)

[ServiceNow DevOps custom actions from GitHub marketplace](servicenow-devops-custom-actions-from-github-marketplace.md#)

