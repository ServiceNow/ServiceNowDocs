---
title: Set up the Box spoke
description: Integrate your ServiceNow instance and the Box APIs to automate the Box spoke actions. For example, you can set up a flow that removes a file in your Box account. When you set up the Box spoke, this flow is automated.Create a custom OAuth application from your Box account to enable OAuth 2.0 authentication with the Box spoke.Add and configure a Box connection to authenticate ServiceNow requests in a Box spoke.Regenerate the Box OAuth token when it expires. The Box spoke OAuth token expires every thirty days.Set up an OAuth provider with the JWT Bearer grant type to integrate your ServiceNow instance with Box.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Box Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Box spoke

Integrate your ServiceNow instance and the Box APIs to automate the Box spoke actions. For example, you can set up a flow that removes a file in your Box account. When you set up the Box spoke, this flow is automated.

## Before you begin

-   Request Integration Hub subscription
-   Activate the Box spoke plugin
-   Access to Box developer's console
-   Role required: admin

## Create an OAuth application

Create a custom OAuth application from your Box account to enable OAuth 2.0 authentication with the Box spoke.

### Before you begin

Box requirements:

-   Box account
-   Box administrator credentials
-   Role required: admin

### About this task

Complete these steps from your Box account. See the [Box Developer Portal](https://developer.box.com/) documentation for instructions on creating and configuring custom applications.

### Procedure

1.  Log in to the [Box developer's console](https://app.box.com/developers/console).

2.  Select **Create New App**.

    ![Emphasizes the Create New App button](../image/box-spoke-create-new-app-icon.png)

3.  Select **Custom App**.

    ![Emphasizes the Custom App option](../image/box-spoke-custom-app-button.png)

4.  Complete the form.

<table id="table_am5_5bf_czb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

**App Name**

</td><td>

`Box App`

</td></tr><tr><td>

**Description \(optional\)**

</td><td>

Leave this field empty

</td></tr><tr><td>

**Purpose**

</td><td>

Select**Custom Portal**

</td></tr></tbody>
</table>5.  Select **Next**.

    The Create a Custom App modal appears.

6.  Select **User Authentication \(OAuth 2.0\)**.

7.  To confirm, select **Create App**.

    You are in your application's configuration settings.

8.  In the OAuth 2.0 Credentials section, copy the Client ID and Client Secret.

    You need this information to register the application as a third-party OAuth provider on your ServiceNow instance.

9.  In the Application Scopes section, enable the scope permissions you want to support.

<table id="table_qlp_sqh_gfb"><thead><tr><th>

Application Scopes

</th><th>

Use for

</th></tr></thead><tbody><tr><td>

Read and write all files and folders stored in Box

</td><td>

Document management, document sharing, and folder management actions

</td></tr><tr><td>

Manage users

</td><td>

User management actions

</td></tr><tr><td>

Manage groups

</td><td>

Group management actions

</td></tr><tr><td>

Manage enterprise properties

</td><td>

Document sharing, group management, and user management actions

</td></tr><tr><td>

Manage webhooks

</td><td>

Configuring V2 webhooks

</td></tr><tr><td>

Manage AI

</td><td>

Interact with Box AI actions

</td></tr></tbody>
</table>10. Select **Save Changes**.


## Configure a connection record for the Box spoke

Add and configure a Box connection to authenticate ServiceNow requests in a Box spoke.

### Before you begin

Role required: admin

### Procedure

1.  In your ServiceNow instance, navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Box** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Box spoke, click **View Details**.

        ![View details of the Box connection.](../image/box-conn-view-det.png)

    -   To manage more than one Box spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![Configure the Box connection.](../image/box-conf-connection.png)

5.  On the form, fill these values.

<table id="table_hjv_tsb_h2c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

`Box`.

</td></tr><tr><td>

Connection URL

</td><td>

The instance URL in this format:`<provider-domain-name>.net`.

</td></tr><tr><td>

Credential Name

</td><td>

`Box Upload Credentials`.

</td></tr><tr><td>

OAuth Name

</td><td>

`Box OAuth`.

</td></tr><tr><td>

OAuth Client ID

</td><td>

The application client ID. For more information, see [Create an OAuth application](setup-box-spoke.md#).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

The application client secret. For more information, see [Create an OAuth application](setup-box-spoke.md#).

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The URL in this format: `https://<ServiceNow-instance-name>.service-now.com/oauth_redirect.do`. Replace `<ServiceNow-instance-name>` with your ServiceNow instance name.

</td></tr></tbody>
</table>    ![Configure the Box connection.](../image/box-connection.png)

6.  Click **Configure Connection**.


### Result

The spoke connection is configured and ready to be used.

**Note:** OAuth tokens expire after 30 days. An administrator can regenerate the spoke OAuth token every 30 days.

## Regenerate Box OAuth token

Regenerate the Box OAuth token when it expires. The Box spoke OAuth token expires every thirty days.

### Before you begin

Role required: admin

### Procedure

1.  In your ServiceNow instance, navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Connections** tab.

3.  Search for the **Box** connection alias.

4.  Select **View Details**.

5.  Select **Get OAuth Token** for the connection.


### Result

The Box spoke receives a new OAuth access token. It expires in 30 days.

## Integrate ServiceNow instance with JWT Bearer grant type

Set up an OAuth provider with the JWT Bearer grant type to integrate your ServiceNow instance with Box.

### Before you begin

Role required: admin

### Procedure

1.  Do the steps at the Box end.

    1.  Sign Up for [Box Developer Account](https://developer.box.com).

    2.  On the [Developer Console](https://app.box.com/developers/console), select **Custom App**.

    3.  Confirm that the authentication method is OAuth 2.0 with JWT \(Server Authentication\).

    4.  Enter a unique name for the app and create the app.

    5.  View the app.

    6.  On OAuth 2.0 Credentials, copy the Client ID and Client Secret.

    7.  Create a new keystore and export a public key from that into BOX.

    8.  Note the enterpriseID under the App Settings.

    9.  Navigate to **My apps** &gt; **&lt;App Name&gt;** &gt; **General** &gt; **Submit for Authorization**.

    10. Select your account name on the top of the Admin Console.

    11. In your account, create a folder and upload a text file.

2.  Do the steps at the ServiceNow instance end.

    1.  Navigate to **System Definition** &gt; **Certificates** &gt; **New** &gt; **Type** &gt; **Storepass**.

    2.  Attach the keystore certificate.

    3.  Configure a JWT signing key by navigating to **System OAuth** &gt; **JWT Keys** &gt; **New**.

    4.  Create OAuth application registry entry by navigating to **System OAuth** &gt; **Application Registry** &gt; **New** &gt; **Connect to a third party OAuth Provider** &gt; **Default Grant type \( JWT Bearer\)**.

    5.  Under the OAuth entity profile \(oauth\_entity\_profile\) associate the created 'jwt provider'.

    6.  Create a REST message.

    7.  In the REST Message, select **Get OAuth token** to get the access token.

    8.  Go to the 'Default GET' method and click on 'Test'.

    9.  An the BOX end, share the folder and file.


