---
title: Set up the GoTo spoke
description: Integrate the ServiceNow instance and GoTo by creating a custom OAuth client in GoTo to authenticate ServiceNow requests.Create an OAuth client for authenticating GoTo API requests.Create a connection between your GoTo applications and your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [GoTo Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the GoTo spoke

Integrate the ServiceNow instance and GoTo by creating a custom OAuth client in GoTo to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the GoTo spoke.
-   GoTo role required: User with a LogMeIn developer account and admin account.
-   Role required: admin.

## Create a GoTo OAuth client

Create an OAuth client for authenticating GoTo API requests.

### Before you begin

Role required: GoTo user with a LogMeIn developer account and admin account.

### Procedure

1.  From a web browser, open the [GoTo Developer Center](https://developer.goto.com/).

2.  Sign in using your LogMeIn developer account.

    If you have not already set up a LogMeIn developer account, see [How to login or create a developer account](https://developer.goto.com/guides/HowTos/01_HOW_developerAccount/) for detailed instructions.

3.  From the LogMeIn Developers home page, select the **OAuth Clients** tab.

4.  Click **Create a client**.

5.  On the Details tab of the form, fill in the client details.

    |Field|Description|
    |-----|-----------|
    |Client name|Name of the OAuth client.|
    |Description|Optional description for the OAuth client.|
    |Redirect URLs|Redirect URL of the ServiceNow instance on which you are integrating your GoTo applications. Enter `https://<*instance-url*>/oauth_redirect.do`, where &lt;*instance-url*&gt; is the URL of your ServiceNow instance.|

6.  Click **Next**.

7.  On the Scopes tab, specify the level of access that the OAuth client has to your GoTo users and applications.

<table id="table_zcp_yvn_tnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Profile

</td><td>

OAuth scopes for getting and modifying user information for your authenticated users. The **Get user information** scope is enabled automatically. Select the check box to enable the **Modify user details** scope.

</td></tr><tr><td>

GoToMeeting, GoToWebinar, or GoTo Training

</td><td>

OAuth scope for creating, starting, and modifying sessions for your GoToMeeting, GoToWebinar, and GoTo Training applications. Select the check box to enable this scope.

 **Note:** The SaaS License Management GoTo integration does not support license management for the GoTo Training application.

</td></tr><tr><td>

GoTo Assist Remote Support or Service Desk

</td><td>

OAuth scope for creating, starting, and modifying sessions for the GoTo Assist Remote Support and Service Desk applications. Leave this check box unselected.**Note:** The SaaS License Management GoTo integration does not support license management for the GoTo Assist applications.

</td></tr><tr><td>

SCIM

</td><td>

OAuth scope for automating user management using the System for Cross-domain Identity Management \(SCIM\) protocol. Leave this check box unselected.

</td></tr><tr><td>

Admin Center

</td><td>

OAuth scope for managing LogMeIn users through the GoTo Admin Center. Select the check box to enable this scope.

</td></tr><tr><td>

GoToConnect

</td><td>

OAuth scope for initiating phone calls and other telephone services using GoToConnect. If the GoToConnect license is enabled, select these check boxes:-   Access call history for phone lines in the PBX \[cr.v1.read\]
-   Retrieve your phone line information \[users.v1.lines.read\]


</td></tr></tbody>
</table>8.  Click **Save**.

9.  On the Credentials tab, copy the values in the **Client ID** and **Client secret** fields.

    Save them in a secure location for later use.

10. Select the check box to verify that you have stored the client secret.

11. Click **Done**.


## Create a GoTo connection

Create a connection between your GoTo applications and your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Click **View Details** for your GoTo connection.

4.  From the list of available connections, locate GoTo and then click **Configure**.

    The Configure Connection dialog box opens.

5.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the GoTo connection. This field populates automatically.|
    |Name|Name of your GoTo credentials. This field populates automatically.|
    |OAuth Client ID|Client ID that is assigned to your GoTo OAuth client.|
    |OAuth Client Secret|Client secret that is assigned to your GoTo OAuth client.|
    |OAuth Redirect URL|Redirect URL of the ServiceNow instance on which you are integrating your GoTo applications. This field populates automatically.|

6.  Click **Configure and Get OAuth Token**.

    The Authorize App dialog box opens.

7.  On the dialog box, click **Allow**.

    The OAuth access token becomes available for authorizing your GoTo connection.

8.  If the GoToConnect license is enabled, navigate to the **Connections** tab.

9.  Find the connection for GoToConnect and click **View Details**.

10. Click **Get OAuth Token** to generate a token for GoToConnect.


