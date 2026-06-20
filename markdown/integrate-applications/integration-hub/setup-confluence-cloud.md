---
title: Set up the Confluence Cloud spoke
description: Integrate the ServiceNow instance and Confluence Cloud by creating a custom OAuth 2.0 application in Confluence Cloud to authenticate ServiceNow requests.Add and configure a Confluence Cloud connection to authenticate ServiceNow requests in Confluence Cloud spoke.Integrate the ServiceNow instance with your Confluence Cloud account using OAuth to authenticate ServiceNow requests.Create a Confluence Cloud OAuth 2.0 \(3LO\) application to enable access to the Confluence Cloud API.Specify the groups that have access to Confluence products so that you can manage the users within only these groups using the Confluence Cloud spoke.Create a connection record for the Confluence Cloud account. The connection and credential alias uses this connection to perform actions in Confluence Cloud.Create a credential record for the Confluence Cloud account. The Confluence Cloud spoke connection and credential alias uses this credential to authorize actions.Create an application registry record to configure OAuth 2.0 authentication for the Confluence Cloud spoke. The record stores the client credentials and scopes required to authorize Confluence Cloud spoke actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/setup-confluence-cloud.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Confluence Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Confluence Cloud spoke

Integrate the ServiceNow instance and Confluence Cloud by creating a custom OAuth 2.0 application in Confluence Cloud to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Confluence Cloud spoke.
-   Atlassian role required: site admin
-   Role required: admin.

## Option 1: Using OAuth authentication \(Authorization Code grant type\) connection

Add and configure a Confluence Cloud connection to authenticate ServiceNow requests in Confluence Cloud spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **Confluence Cloud** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Confluence Cloud spoke, click **View Details**.
    -   To manage more than one Confluence Cloud spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection. For example, `Confluence Cloud Spoke Connection`.|
    |Connection URL|URL of the Atlassian API endpoint: `https://api.atlassian.com/`.|
    |Scopes|By default, these scopes are provided: `ace:confluence, read:page:confluence, search:confluence, read:confluence-groups, write:confluence-groups, read:confluence-user, read:me, read:account, offline_access`. You can modify the scopes as per your requirement.|

    \[Omitted image "confluence-cloud-spoke-conn-config.png"\] Alt text: Create a connection for Confluence Cloud spoke using connection template

6.  Click **Save and Get OAuth Token**.


## Option 2: Using OAuth authentication \(Client Credentials grant type\)

Integrate the ServiceNow instance with your Confluence Cloud account using OAuth to authenticate ServiceNow requests.

### Before you begin

**Important:** Apps that collect API tokens to create individual 3LO apps don't comply with Atlassian security requirements for cloud apps and Atlassian acceptable use policy.

Role required: admin

### Create a Confluence Cloud OAuth 2.0 \(3LO\) application

Create a Confluence Cloud OAuth 2.0 \(3LO\) application to enable access to the Confluence Cloud API.

#### Before you begin

Role required: Atlassian site admin.

#### Procedure

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


### Add Confluence groups

Specify the groups that have access to Confluence products so that you can manage the users within only these groups using the Confluence Cloud spoke.

#### Before you begin

ServiceNow role required: admin

Role required: Atlassian site admin

#### Procedure

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


### Create a connection record for the Confluence Cloud spoke

Create a connection record for the Confluence Cloud account. The connection and credential alias uses this connection to perform actions in Confluence Cloud.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the alias record for **Confluence Cloud** that shipped with the spoke.

3.  On the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  Enter these values and click **Submit**.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `Confluence Cloud OAuth Connection`.|
    |Credential|Select the credential record created for Confluence Cloud. For example, select **Confluence Cloud client credential cred**.|
    |Connection URL|Enter the URL of the Atlassian API endpoint: `https://api.atlassian.com/`.|

5.  Click **Submit**.

    The Confluence Cloud spoke is configured to use OAuth 2.0 Client Credentials via the service account.


### Create credential record for the Confluence Cloud spoke

Create a credential record for the Confluence Cloud account. The Confluence Cloud spoke connection and credential alias uses this credential to authorize actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record for the Confluence Cloud spoke. For example, `Confluence Cloud client credential cred`.|
    |OAuth Entity Profile|Select the OAuth entity profile record that was created when the application registry record is configured. For more information, see[Create an application registry record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-confluence-cloud.md).|

5.  Right-click the form header and click **Save**.

6.  Click the **Get OAuth Token** related link.


### Create an application registry record

Create an application registry record to configure OAuth 2.0 authentication for the Confluence Cloud spoke. The record stores the client credentials and scopes required to authorize Confluence Cloud spoke actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the application registry record. For example, `Confluence Cloud Client Credentials OAuth`.|
    |Client ID|Client ID generated when the OAuth 2.0 integration was created in Atlassian Developer console.|
    |Client Secret|Client secret generated when the OAuth 2.0 integration was created in Atlassian Developer console.|
    |Default Grant type|Grant type used to establish the token. Select **Client Credentials**.|
    |Token URL|OAuth server token endpoint. Enter: `https://auth.atlassian.com/oauth/token`.|
    |Token Revocation URL|OAuth server token revocation endpoint. Enter: `https://auth.atlassian.com/oauth/token`.|
    |Active|Select the check box.|

5.  In the **OAuth Entity Scopes** tab, create this entity scope record.

    |Name|OAuth scope|
    |----|-----------|
    |Confluence Cloud scopes|`ace:confluence read:page:confluence search:confluence read:confluence-groups write:confluence-groups read:confluence-user read:me read:account offline_access`|

6.  Right-click the form header and click **Save**.

    The record is saved and a OAuth Entity Profile record is created under the **OAuth Entity Profiles** tab.

7.  Click the **OAuth Entity Profiles** tab and open the default profile record.

8.  Verify these values.

    -   **Grant type** is set to **Client Credentials**.
    -   Scope records previously created are listed under the **OAuth Entity Profile Scopes** related list.
9.  Click **Update**.


