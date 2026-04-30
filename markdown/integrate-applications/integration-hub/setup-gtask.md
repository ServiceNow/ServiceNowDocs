---
title: Set up the Google Tasks spoke
description: Integrate the ServiceNow instance and the Google Tasks spoke by using the G Suite credentials to authenticate the ServiceNow requests.Create a custom OAuth application to enable OAuth 2.0 authentication of the ServiceNow by the Google Workspace.Create a connection and credential record to establish a connection between the ServiceNow instance and the Google Workspace.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Google Tasks Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Tasks spoke

Integrate the ServiceNow instance and the Google Tasks spoke by using the G Suite credentials to authenticate the ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Tasks spoke.
-   Role required: admin.

## Set up an OAuth 2.0 Client application

Create a custom OAuth application to enable OAuth 2.0 authentication of the ServiceNow by the Google Workspace.

### Before you begin

Google Tasks integration requirements:

-   A domain and an email address associated with the domain. For example, www.mydomain.com and jane-admin@mydomain.com. Note that you can only register one email address per domain in G Suite.
-   A Google G Suite or Gmail login created with the domain.

Role required: admin.

### About this task

Complete these steps from the [Google Developers Console](https://console.developers.google.com/). See the G Suite product documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Navigate to [https://console.developers.google.com](https://console.developers.google.com), create a project with your G Suite administrator credentials, and open the project.

2.  From the APIs &amp; Services menu, select **OAuth consent screen**.

3.  Enter the application name, and specify the Authorized domain `service-now.com`.

4.  Select **Save**.

5.  From the APIs &amp; Services menu, select **Credentials**, and select **Create OAuth client ID** from the **Create credentials** list.

6.  Select the application type **Web application**.

7.  Enter the following Authorized redirect URI: `https://<instance>.service-now.com/oauth_redirect.do` and select **Create**.

8.  Copy the Client ID and the Client Secret to a text file.

    The animation demonstrates the setting up of OAuth Client ID. You must activate the Google Tasks API on [https://console.cloud.google.com/welcome?project=nowgsintegration](https://console.cloud.google.com/welcome?project=nowgsintegration) before creating an OAuth Client ID.![Set up OAuth Client ID.](../image/OAuth-client-ID.gif)

    **Tip:** Save the JSON file containing the OAuth client details for later reference.


## Configure a connection for Google Tasks spoke

Create a connection and credential record to establish a connection between the ServiceNow instance and the Google Workspace.

### Before you begin

Role required: admin.

### About this task

The connection and credentials contain the details such as the client ID, client secret, and the redirect URL that the Google Workspace must authenticate the ServiceNow instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select Integrations.

3.  In the Search all connections field, enter `Google Tasks`.

4.  On the Google Tasks tile, select **View Details**.

5.  Select **Configure**.

6.  Fill the form with the details given in the table.

<table id="table_ebx_vjh_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection between the Google Workspace and the ServiceNow instance.**Note:** The default name is Google Tasks and it's read-only. However, you can provide custom names when you set up more connection and credential records after this record.

</td></tr><tr><td>

Connection URL

</td><td>

Enter the URL `https://www.googleapis.com`**Note:** Make sure that you don't include spaces before or after this URL. If there are spaces, the connection fails.

.

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

The OAuth redirect URL. It must be in the format https://&lt;instance-name.service-now.com&gt;/oauth\_redirect.do.

</td></tr></tbody>
</table>7.  Select **Configure and Get OAuth Token**.


