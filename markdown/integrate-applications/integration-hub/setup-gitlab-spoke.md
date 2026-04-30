---
title: Set up GitLab spoke
description: Integrate your ServiceNow instance and the GitLab by creating a custom OAuth application in the GitLab.Add GitLab token to authenticate requests from your ServiceNow instance.Create a custom OAuth application from your GitLab account to enable OAuth 2.0 authentication with the GitLab spoke.Add and configure a GitLab connection to authenticate ServiceNow requests in GitLab spoke.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [GitLab Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up GitLab spoke

Integrate your ServiceNow instance and the GitLab by creating a custom OAuth application in the GitLab.

## Before you begin

-   Request Integration Hub subscription
-   Activate the GitLab spoke plugin
-   Create an account with GitLab at [https://gitlab.com/users/sign\_in](https://gitlab.com/users/sign_in)
-   Role required: admin

## Add GitLab token

Add GitLab token to authenticate requests from your ServiceNow instance.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **GitLab Token Management** &gt; **GitLab Token Managements**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Secret|Secret created during the GitLab application configuration.|
    |Name|Name to identify the record.|
    |OAuth Entity Profile|Leave the field empty. System auto-assigns the default entity profile after the connection is configured.|

4.  Right-click the form header and click **Save**.

5.  Click **Generate Secure Token**.

    Value of the generated secure token is displayed.

6.  Copy and record the value of the secure token for later use.

7.  Click **Update**.


## Create OAuth application in GitLab account

Create a custom OAuth application from your GitLab account to enable OAuth 2.0 authentication with the GitLab spoke.

### Before you begin

-   GitLab account
-   Role required: GitLab admin.

### About this task

Complete these steps from your GitLab account. See the [GitLab](https://docs.gitlab.com/ee/README.html) documentation for instructions on creating and configuring applications.

### Procedure

1.  From your GitLab account, create an application.

2.  Enter ServiceNow instance URL in **Redirect URI**.

    The format of the redirect URL is: `https://<instance-name>.service-now.com/api/sn_gitlab_spoke/gitlab_oauth_redirect/oauth?secureToken=<Secure-Token>`.

    Replace **&lt;Instance-Name&gt;** with the name of your ServiceNow instance and replace **&lt;Secure-Token&gt;** with the secure token you had generated in the ServiceNow instance.

3.  Copy and record the **Application Id** and **Secret** for later use.

    These details are required to register the application as a third-party OAuth provider on your ServiceNow instance.


### Result

The custom OAuth application from your GitLab account is created and can be integrated with the ServiceNow instance.

## Configure a connection for the GitLab spoke

Add and configure a GitLab connection to authenticate ServiceNow requests in GitLab spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **GitLab** connection alias and click **View Details**.

5.  Click **Edit** or if you are configuring the spoke for the first time, click **Configure**.

6.  On the **Connection** form, fill in the fields.

<table id="table_tfv_3d5_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to uniquely identify the connection.

</td></tr><tr><td>

Connection URL

</td><td>

Enter `https://gitlab.com/api`.**Note:** If you have installed GitLab on an on-premise server, enter the URL in this format: `https://<gitlab-hosted-instance>.com/api`

</td></tr><tr><td>

OAuth Entity Name

</td><td>

Name to identify the OAuth entity record.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application ID created during the GitLab application configuration.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Secret created during the GitLab application configuration.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

OAuth callback endpoint. The format of the redirect URL is: `https://<instance-name>.service-now.com/api/sn_gitlab_spoke/gitlab_oauth_redirect/oauth?secureToken=<Secure-Token>`.Replace **&lt;Instance-Name&gt;** with the name of your ServiceNow instance and replace **&lt;Secure-Token&gt;** with the secure token you had generated in the ServiceNow instance.

</td></tr></tbody>
</table>7.  Click **Configure and Get OAuth Token**.


