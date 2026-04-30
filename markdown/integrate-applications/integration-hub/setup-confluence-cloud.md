---
title: Set up the Confluence Cloud spoke
description: Integrate the ServiceNow instance and Confluence Cloud by creating a custom OAuth 2.0 application in Confluence Cloud to authenticate ServiceNow requests.Create a Confluence Cloud OAuth 2.0 \(3LO\) application to enable access to the Confluence Cloud API.Create a connection between your Confluence Cloud applications and your ServiceNow instance.Specify the groups that have access to Confluence products so that you can manage the users within only these groups using the Confluence Cloud spoke.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Confluence Cloud Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Confluence Cloud spoke

Integrate the ServiceNow instance and Confluence Cloud by creating a custom OAuth 2.0 application in Confluence Cloud to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Confluence Cloud spoke.
-   Atlassian role required: site admin
-   Role required: admin.

## Create a Confluence Cloud OAuth 2.0 \(3LO\) application

Create a Confluence Cloud OAuth 2.0 \(3LO\) application to enable access to the Confluence Cloud API.

### Before you begin

Role required: Atlassian site admin.

### Procedure

1.  From a web browser, open the [Atlassian Developer portal](https://developer.atlassian.com/).

2.  Log in to your site admin account.

3.  On the page header of the portal, click your profile icon and then select **Developer console**.

    The My apps page of the Atlassian Developer Console opens.

4.  Click the **Create app** menu and then select **OAuth 2.0 \(3LO\) integration**.

    The Create a new OAuth 2.0 \(3LO\) integration page opens.

5.  Enter a name for the OAuth 2.0 \(3LO\) application in the **Name** field.

6.  Select the **I agree to be bound by Atlassian's developer terms** check box and then click **Create**.

    The overview and settings for your newly created app open.

7.  Configure authorization settings for your application.

    1.  From the left navigation pane, select **Authorization**.

    2.  Click **Configure** for the OAuth 2.0 \(3LO\) authorization type.

        The OAuth 2.0 authorization code grants \(3LO\) for apps page opens.

    3.  In the **Callback URL** field, enter the URL of the OAuth provider that users are redirected to after authentication.

        Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

    4.  Click **Save changes**.

8.  Configure API scopes for your application.

    API scopes specify the level of access that the application has to the Atlassian APIs.

    1.  From the left navigation pane, select **Permissions**.

    2.  From the list of available APIs, locate the Confluence API and then click **Add**.

        The **Add** action button automatically changes to the **Configure** action button.

    3.  Click **Configure**.

        The Confluence API page opens.

    4.  Add the following scopes for the Confluence API:

        -   Search Confluence content and space summaries
        -   Read user groups
        -   Create, remove and update user groups
        -   Read user
9.  Retrieve the client ID and client secret that are assigned to your application.

    1.  From the left navigation pane, select **Settings**.

    2.  In the Authentication details section, copy the values in the **Client ID** and **Secret** fields.

        Save them in a secure location for later use.


## Create a Confluence Cloud connection

Create a connection between your Confluence Cloud applications and your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Click **View Details** for your Confluence Cloud connection.

4.  From the list of available connections, locate Confluence Cloud and then click **Configure**.

    The Configure Connection dialog box opens.

5.  In the dialog box, fill in the fields.

<table id="table_skk_54h_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the Confluence Cloud connection. This field populates automatically.

</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

Name

</td><td>

Name of your Confluence Cloud credentials. This field populates automatically.

</td></tr><tr><td>

Site URL**Note:** This field appears only if you have requested and installed version 1.0.2 or earlier of the Confluence Cloud spoke.

</td><td>

URL of your Confluence Cloud site.

</td></tr><tr><td>

Connection URL**Note:** This field appears only if you have requested and installed version 1.0.3 or later of the Confluence Cloud spoke.

</td><td>

API URL for Confluence Cloud. This field is automatically set to **https://api.atlassian.com**.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that is assigned to your Confluence Cloud OAuth 2.0 \(3LO\) application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that is assigned to your Confluence Cloud OAuth 2.0 \(3LO\) application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the callback URL that you specified in [Create a Confluence Cloud OAuth 2.0 \(3LO\) application](setup-confluence-cloud.md#).

</td></tr></tbody>
</table>6.  Click **Configure and Get OAuth Token**.

    The Authorize App dialog box opens.

7.  In the dialog box, click **Allow**.

    The OAuth token becomes available for authorizing your Confluence Cloud connection.


## Add Confluence groups

Specify the groups that have access to Confluence products so that you can manage the users within only these groups using the Confluence Cloud spoke.

### Before you begin

ServiceNow role required: admin

Role required: Atlassian site admin

### Procedure

1.  From a web browser, open the [Atlassian Administration portal](https://admin.atlassian.com/).

2.  Log in to your site admin account.

3.  Navigate to **SITE SETTINGS** &gt; **Product access**.

4.  In the Confluence section, view the list of groups that have access to Confluence products.

    Take note of this information for later use.

5.  Return to your ServiceNow instance and navigate to **Confluence Cloud** &gt; **Confluence Groups**.

6.  On the Confluence Groups form, click the **Add Groups** related link.

    The Add Confluence Groups dialog box opens.

7.  In the Available list, select the groups that have access to Confluence products.

    **Tip:** The Available list includes all groups that are associated with your Atlassian account. Select only the groups that have access to Confluence products.

8.  Click the right arrow button to move the groups from the Available list to the Selected list.

9.  Click **OK**.


