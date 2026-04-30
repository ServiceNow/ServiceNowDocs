---
title: Set up the Zendesk spoke
description: Integrate the ServiceNow instance and Zendesk by creating a custom OAuth application in Zendesk to authenticate ServiceNow requests.Create an OAuth client for authenticating Zendesk API requests.Create a connection between your Zendesk applications and your ServiceNow instance so that your instance can retrieve user data from your applications.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Zendesk Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Zendesk spoke

Integrate the ServiceNow instance and Zendesk by creating a custom OAuth application in Zendesk to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Zendesk spoke.
-   Zendesk role required: admin
-   Role required: admin

## Create a Zendesk OAuth client

Create an OAuth client for authenticating Zendesk API requests.

### Before you begin

Role required: Zendesk admin

### Procedure

1.  From a web browser, open [Zendesk](https://www.zendesk.com).

2.  Log in using your admin credentials.

    The Zendesk Agent Workspace opens.

3.  On the left navigation menu of the Zendesk Agent Workspace, select the Admin icon \(![Admin icon.](../image/admin-icon.png)\).

    The Admin menu opens.

4.  From the Admin menu, navigate to **Channels** &gt; **API**.

    The Zendesk API page opens.

5.  Select the **OAuth Clients** tab and then click **Add OAuth client**.

6.  The Create a new OAuth client form opens.

7.  On the form, fill in the fields.

<table id="table_aym_sgf_cqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Client name

</td><td>

Name of the OAuth client.

</td></tr><tr><td>

Description

</td><td>

Brief description of the OAuth client.

</td></tr><tr><td>

Company

</td><td>

Name of the company whose data the OAuth client grants access to through the Zendesk API. The company name is displayed during authentication of your Zendesk API requests.This field populates automatically based on the company that your Zendesk account is associated with. However, you can modify the company name as needed.

</td></tr><tr><td>

Logo

</td><td>

Logo that is displayed during authentication of your Zendesk API requests. Click the green square to locate and select the logo that you want to display.

</td></tr><tr><td>

Unique identifier

</td><td>

Unique identifier for the OAuth client. This field populates automatically based on the OAuth client name that you specified in the **Client name** field. However, you can modify the unique identifier as needed.**Note:** The unique identifier is used only in the Zendesk code.

</td></tr><tr><td>

Redirect URLs

</td><td>

URL of the OAuth provider that users are redirected to after authentication. Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

</td></tr></tbody>
</table>8.  Click **Save**.

    The Please store the secret that will appear dialog box opens.

9.  On the dialog box, click **OK**.

    The dialog box closes and the form reloads.

10. Copy the value in the **Secret** field.

    Save this in a secure location for later use.


## Create a Zendesk connection

Create a connection between your Zendesk applications and your ServiceNow instance so that your instance can retrieve user data from your applications.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Locate your Zendesk connection and then click **Add Connection**.

    The Create Connection dialog box opens.

4.  On the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name of the Zendesk connection. This field populates automatically.|
    |Connection URL|URL for the connection. Enter `https://<subdomain>.zendesk.com`, where &lt;*subdomain*&gt; is your organization subdomain.|
    |Credential Information|
    |OAuth Client ID|Unique identifier for your Zendesk OAuth client. Enter the same unique identifier that you specified in [Create a Zendesk OAuth client](setup-zendesk.md#).|
    |OAuth Client Secret|Secret that is assigned to your Zendesk OAuth client. Enter the same secret that you copied in [Create a Zendesk OAuth client](setup-zendesk.md#).|
    |OAuth Redirect URL|URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the redirect URL that you specified in [Create a Zendesk OAuth client](setup-zendesk.md#).|

5.  Click **Create and Get OAuth Token**.

    The Zendesk OAuth authorization dialog box opens.

6.  On the dialog box, click **Authorize**.

    The OAuth access token becomes available for authorizing your Zendesk connection.

7.  In your ServiceNow instance, add OAuth entity profile scope.

    1.  Navigate to **System OAuth** &gt; **Application Registry**.

    2.  Open the record for the Zendesk spoke. For example, **Zendesk OAuth**.

    3.  In the **OAuth Entity Profiles** tab, open the default record, for example, **Zendesk.OAuthProfile**.

    4.  Insert a new row with these values.

        |Field|Value|
        |-----|-----|
        |OAuth Entity Scope|users:write read|
        |OAuth scope|write read|


