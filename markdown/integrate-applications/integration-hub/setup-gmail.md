---
title: Set up the Gmail spoke
description: Set up an outbound integration between the ServiceNow instance and the Google APIs.Create a custom OAuth application to enable OAuth 2.0 authentication of the ServiceNow by the Google APIs.Configure the Gmail connection record to establish a connection between the ServiceNow instance and the Google APIs.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Gmail Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Gmail spoke

Set up an outbound integration between the ServiceNow instance and the Google APIs.

## Before you begin

-   Request an Integration Hub subscription.
-   Install the Gmail spoke plugin on the ServiceNow instance.
-   Role required: admin.

## About this task

To establish an outbound integration, you must complete these steps.

-   [Set up an OAuth 2.0 client ID](setup-gmail.md#)
-   [Configure a connection for the Gmail spoke](setup-gmail.md#)

## Set up an OAuth 2.0 client ID

Create a custom OAuth application to enable OAuth 2.0 authentication of the ServiceNow by the Google APIs.

### Before you begin

Google Tasks integration requirements:

-   A domain and an email address associated with the domain. For example, www.mydomain.com and jane-admin@mydomain.com. You can only register one email address per domain in G Suite.
-   A Google G Suite or Gmail login created with the domain.

Role required: admin.

### Procedure

1.  Navigate to [https://console.developers.google.com](https://console.developers.google.com), create a project with your G Suite administrator credentials, and open the project.

2.  From the APIs &amp; Services menu, select **OAuth consent screen**.

3.  Enter the application name, and specify the Authorized domain `service-now.com`.

4.  Click **Save**.

5.  From the APIs &amp; Services menu, select **Credentials**, and select **Create OAuth client ID** from the **Create credentials** list.

6.  Select the application type **Web application**.

7.  Enter the following Authorized redirect URI: `https://<instance>.service-now.com/oauth_redirect.do` and select **Create**.

8.  Copy the Client ID and the Client Secret to a text file.


## Configure a connection for the Gmail spoke

Configure the Gmail connection record to establish a connection between the ServiceNow instance and the Google APIs.

### Before you begin

Role required: admin.

### About this task

The connection and credentials contain the details such as the client ID, client secret, and the redirect URL that the Google Workspace must authenticate the ServiceNow instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Select the **Connections** tab.

4.  In the Search all connections field, enter `Gmail`.

5.  Select **View Details**.

    ![View Details button on Gmail spoke connection alias.](../image/gmail-spk-conn-alias.png)

6.  Select **Configure**.

    ![Configure button on Gmail spoke connection alias.](../image/gmail-spk-alias-config-button.png)

7.  Fill the form with the details given in the table.

<table id="table_ebx_vjh_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection between the Google Workspace and the ServiceNow instance.**Note:** The default name is Gmail and it's read-only. However, you can provide custom names when you set up more connection and credential records after this record.

</td></tr><tr><td>

Connection URL

</td><td>

Enter the URL `https://www.googleapis.com`**Note:** Make sure that you don't include spaces before or after this URL. If there are spaces, the connection fails.

.

</td></tr><tr><td>

OAuth Entity Name

</td><td>

Name to identity the OAuth entity record.

</td></tr><tr><td>

OAuth Client ID

</td><td>

The OAuth client ID generated when you created the OAuth client ID.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

The OAuth client secret generated when you created the OAuth client ID.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The OAuth redirect URL. It must be in the format: `https://<instance-name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>    ![Gmail connection form.](../image/gmail-spk-conn-form.png)

8.  Select **Configure and Get OAuth Token**.

    You must log into Gmail after the OAuth token is issued.


