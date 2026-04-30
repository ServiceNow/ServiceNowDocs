---
title: Setting up GitLab OAuth 2.0 credentials for DevOps
description: Integrate your GitLab account with your ServiceNow instance by creating a custom OAuth application in GitLab and authenticating requests from ServiceNow DevOps.Create a custom GitLab App from your GitLab account to enable OAuth 2.0 authentication with your ServiceNow instance.Use the information generated during GitLab App account configuration to register GitLab as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create a credential record for the GitLab App provider previously created to authorize actions.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [GitLab, Integrate, DevOps Change Velocity, IT Service Management]
---

# Setting up GitLab OAuth 2.0 credentials for DevOps

Integrate your GitLab account with your ServiceNow instance by creating a custom OAuth application in GitLab and authenticating requests from ServiceNow DevOps.

Configure your GitLab account, register GitLab in the application registry, and create a credential record for the GitLab App provider.

Role required: oauth\_admin.

**Parent Topic:**[GitLab integration with DevOps Change Velocity](gitlab-integration-dev-ops.md)

## Configure the GitLab App in your GitLab account \(Authorization Code\)

Create a custom GitLab App from your GitLab account to enable OAuth 2.0 authentication with your ServiceNow instance.

### Before you begin

Role required: admin

### About this task

Configure GitLab as an OAuth 2.0 authentication identity provider. For more information, see [GitLab documentation](https://docs.gitlab.com/ee/integration/oauth_provider.html#user-owned-applications).

### Procedure

1.  From your GitLab account, create your App by navigating to **Edit Profile** &gt; **Applications**.

2.  In the **Add new application** form, specify a **Name**, and in **Redirect URI** field, enter `https://<instance-name>.service-now.com/oauth_redirect.do`.

3.  In the **Scopes** section, ensure that you select the **api** check box.

4.  Leave the remaining fields empty \(default\).

5.  Click **Save application**.

    The application is created. You can open the application to access the Application ID, Secret key, and Callback URL.

6.  Install the newly created GitLab App on the accounts of your choice.


## Register GitLab as an OAuth Provider \(Authorization Code\)

Use the information generated during GitLab App account configuration to register GitLab as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System OAuth** &gt; **Application Registry**.

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

Enter any name to uniquely identify the record. For example, enter `My GitLab App Provider`.

</td></tr><tr><td>

Client ID

</td><td>

Enter the Application ID of your GitLab App.

</td></tr><tr><td>

Client Secret

</td><td>

Enter the secret key of your GitLab App.

</td></tr><tr><td>

OAuth API script

</td><td>

Select **OAuthDevOpsGitLabHandler**.

</td></tr><tr><td>

Default Grant type

</td><td>

Select **Authorization Code**.

</td></tr><tr><td>

Authorization URL

</td><td>

Enter `https://gitlab.com/oauth/authorize`.

 For an on-premise deployment, use the proper GitLab host URL.

</td></tr><tr><td>

Token URL

</td><td>

Enter `https://gitlab.com/oauth/token`.

 For an on-premise deployment, use the proper GitLab host URL.

</td></tr></tbody>
</table>5.  Leave the rest of the form fields as default.

6.  Right-click the form header, and click **Save**.

    -   The system validates the OAuth credentials and populates the **Redirect URL** \(Hint: It should match the **Redirect URI** value previously provided in your GitLab App configuration\).
    -   The system populates **OAuth Entity Profile** with **Grant Type** as **Authorization Code**. For example, **OAuth Entity Profile** is created with default **Name**, **My GitLab App Provider default\_profile**.
7.  Validate that the **OAuth Entity Scopes** related list contains the **api** scope.


## Create a credential record for GitLab App provider \(Authorization Code\)

Create a credential record for the GitLab App provider previously created to authorize actions.

### Before you begin

Role required: admin

**Note:** The user who creates the credential record, and generates the OAuth token in ServiceNow must have at least the Maintainer role in GitLab for project webhooks, and Owner role for group webhooks to ensure that webhooks can be auto-configured. For more information, see [GitLab](https://docs.gitlab.com/ee/user/project/integrations/webhooks.html) documentation.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays an empty OAuth 2.0 Credentials form.

4.  Fill in these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `My GitLab App Credential`.|
    |Active|Enable|
    |OAuth Entity Profile|Select the default OAuth Entity profile you created previously.|
    |Applies to|Select the MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Save the record.

6.  Click the **Get OAuth Token** related link to generate the OAuth token.

    A successful token generation indicates that you can now authenticate connection between ServiceNow DevOps and GitLab via OAuth.


