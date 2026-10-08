---
title: Set up the Salesforce spoke
description: Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow.Add and configure a Salesforce connection to authenticate ServiceNow requests in Salesforce spoke.Create a connected app in your Salesforce account to enable OAuth 2.0 authentication with the Salesforce spoke.Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow using OAuth authorization template.Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow using JWT signing key.Enable the JSON Web Token \(JWT\) Bearer Grant token authentication by attaching a valid Java KeyStore \(JKS\) certificate to the Salesforce spoke.Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore certificate.Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.Use the information generated during Salesforce connected app configuration to register Salesforce as an OAuth provider and enable the instance to request OAuth 2.0 tokens.Create Credential records for the Salesforce connected app that you created. The Salesforce spoke connection and credential alias use these credentials to authorize actions.Create connection records for your Salesforce account. The Salesforce spoke connection and credential alias use these connections to perform actions in Salesforce.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/setup-sf-spk.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Salesforce Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Salesforce spoke

Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Salesforce spoke
-   Role required: admin.

**Note:** Two spoke setup procedures are outlined here. Perform one of the procedures as per your requirement.

-   To setup the spoke using OAuth authorization template, see [Option 1: Set up the Salesforce spoke using OAuth authorization template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-sf-spk.md).
-   To setup the spoke using JWT signing key, see [Option 2: Set up the Salesforce spoke using JWT signing key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-sf-spk.md).

**Note:** Don't delete the default connection alias record. This can result in an unexpected behavior. Configure your connection using the default connection alias.

## Configure a connection for Salesforce spoke

Add and configure a Salesforce connection to authenticate ServiceNow requests in Salesforce spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Process Automation** &gt; **Workflow Studio**.

2.  Select **Integrations**.

3.  Select the **Connections** tab.

4.  Use the search box to find the **Salesforce** connection alias.

5.  Select **View Details**.\[Omitted image "salesforce-spoke-conn-templt.png"\] Alt text: Connection template for Salesforce spoke

6.  Configure the Salesforce connection.

    1.  Add or edit a connection.

        -   To set up an existing connection, select **Configure** or **Edit**.
        -   To create and configure a new connection, select **Add Connection**.
        **Note:** To support multiple connections through a spoke, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/support-multiple-connections.md).

    2.  On the configuration form, fill in the fields.

<table id="table_salesforce_conn_config"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to uniquely identify the connection. For example, `Salesforce`.

</td></tr><tr><td>

Connection URL \(Instance URL\)

</td><td>

URL to make a connection to Salesforce. Use this format: `https://<organization_name>.my.salesforce.com`.

</td></tr><tr><td>

Grant Type

</td><td>

OAuth grant type for authentication. Select one of the following options: -   **Authorization Code**
-   **Client Credentials**


</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID generated in Salesforce for OAuth authentication.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret generated in Salesforce for OAuth authentication.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL where Salesforce redirects after successful authentication. Use this format: `https://<instance_name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>    3.  Select **Save and Get OAuth Token**.


### Result

The Salesforce spoke connection is configured and ready to be used.

## Create a connected app in Salesforce

Create a connected app in your Salesforce account to enable OAuth 2.0 authentication with the Salesforce spoke.

### Before you begin

-   Salesforce account
-   Role required: Salesforce admin

### About this task

Complete these steps from your Salesforce account. See [Create a Connected App](https://help.salesforce.com/articleView?id=connected_app_create.htm&type=5) in [Salesforce Trailblazer forum](https://success.salesforce.com/) documentation for instructions on creating and configuring connected apps.

### Procedure

1.  From your Salesforce account, create a connected app.

2.  Configure the connected app to enable your Salesforce application to share data with your ServiceNow instance.

    1.  Select **Enable OAuth Settings** and configure the authentication settings.

    2.  If you want to set up the spoke using JWT signing key, select **Use Digital Signatures** and upload a Java KeyStore \(JKS\) certificate.

    3.  Select the OAuth scopes:

<table id="table_bpb_n2q_yhc"><thead><tr><th>

Grant Type

</th><th>

OAuth scopes

</th></tr></thead><tbody><tr><td>

Authorization Code

</td><td>

-   **Access and manage your data \(api\)**
-   **Perform requests on your behalf at any time \(refresh\_token, offline\_access\)**


</td></tr><tr><td>

Client Credentials

</td><td>

**Access and manage your data \(api\)**

</td></tr></tbody>
</table>    4.  Specify ServiceNow instance URL in Callback URL in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`

    5.  After creating the connected app, under **OAuth Policies** on the Edit Policies page, set these values:

        |Field|Value|
        |-----|-----|
        |Permitted Users|Admin approved users are pre-authorized|
        |IP Restrictions|Relax IP Restrictions|

    6.  Configure user provisioning for the connected app as per your requirement.

3.  Record the values of **Consumer Key** and **Consumer Secret**.

    **Note:**

    -   Assign profile and permission set as per your requirement.
    -   In OAuth app IP restrictions, specify OAuth policies to ensure that the connected app works like a default app.

### Result

The connected app is created in Salesforce.

## Option 1: Set up the Salesforce spoke using OAuth authorization template

Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow using OAuth authorization template.

### Before you begin

-   [Create a connected app in Salesforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-sf-spk.md)
-   Role required: admin

### Procedure

1.  Log in to [Salesforce](https://login.salesforce.com/?startURL=%2Fsetup%2Fsecur%2FRemoteAccessAuthorizationPage.apexp%3Fsource%3DCAAAAWd_ycj7ME8wMHkwMDAwMDA4T0k2AAAA2CFKH_C6K2jEXMcAAa95DHha0KQ0IeY1ykrwEVRkz67RUi8i4a0jM7Vp8V21BaS_L33r3duBQbWQwqlyiK2ggRW4EpVHap4wptWMLW6rSLEX9sFPr9tx-KL10Co6XYnGi6obC4k1a5vaO0N2nCjm2hZZ9ncAxKjFL7Dg5Yn93smtqoQquTJlPn85UW8f4CtFFRxNmMkvCs8fsBriDWCmolMpA7RSre5FgwDVuhOsLTVi7WcOvYa9KQof9RQDptCwsh3emhXvc0b4eIr_mTHD1q-yCB8LCgtH3PZLh7NlpywhUjvaEcqLC1LIaM-s7zxbvNdJnNiYx7ZBVMgvLc7KuHqTrJqnKEHVqRUAQjDbpNHV7IIsiviaGhEnY1uwJM84XtO2z2NYSjT-ANIriMblKQXaVGMucWCSZjvvT-XzrgEUPQCK6ZloS4-icbOjf7dNOIWxBR_Ps6Ux3mmvZE8wsABMyFuPAa0lJr9JLsS1EYT_LXBJSWGZ8GajEk55_zQzkxZzWRX5H5nkqxXu6xIVqNVUdS6DkiK4SSJ0nkLEFyQ3HoAVdWxegmYkcqVgy0KupBs-i2KSW47vgr6D3dU0pWhPaLkf10V3m1kd_C3ZL6ic8MS4_lUtsoyR7T9NbpRdeQ1gERuDu-tRSVgdcPkVi9Kxn9DUvhuFiQx1Cs8F2tcqE417kbJqONd7_2M1UL9b5Wy3s_T5SD1tbjsi9hwvEK1hfIe-JmxykwGgIZRT5Q4rQ-GlkJWxSiIxZOJrWI5ZoNbZX7_GIcC01InFN8OMveE1EAvO4JuC3KZ8Yxwypmr5jUYqzQLOLWhDB5mjoEwdFbns1PQtgwwkFjRnfEI90yysbVMQwMq2X8rp75vc-KDMrqTWyALTkVDbxsyuMWfLqUZ5NFaHggbtwQO7fK9o3ZESzswI6YBZWnzbEmHYaOPjbSIulXe7XjbLVLEMEXyLyr3V7PAPtGv_t3Y0mEG0NeenO_pi3NfUFxgvTZo571hgbEVqSvEdgtJWzTLYN0VxKIf7iYcJwO_zRRPCEA4vpJqha-ppCesm1EwjzdQPj7g0lh7G4faQ4916YDLiJCH2MFPTzyz4z4ib0Zg4ejnPPt3v7xWDenkSL6SiD8PgYSA7zPiTZSuMbXt0TOVXyIhg-RsVaDx9Nlv1Jz5NdDWXUWsxk_vI6LJv63Ib_Ky-X6yalB2bY-Y5GyuthFOpIgEjv1P-NurpdZkHdfKR3EdxgBzpnl35XW2M_7oyz9M0CK1MbxaYlgS6t0LVKkXJC21oMaMnykekz7coxVVZxg94Y28J_zZ0Hk75Xj4yuwRc04XSWvwhyDvaYGV5cR7zXeimrMmMylEBYQOxr7-UBSzxoSuLIJWuDxW2qaIwwW8s134O1U62SPYe-l6m1vzq3AZ6vlYpkngznqLjS6iVruD2qbw%253D&sdtd=1).

    You can also switch from the Lightning UI.

2.  Select the setup icon \[Omitted image "gear-icon.png"\] Alt text: Gear icon and then select **Setup**.

3.  Search for and select  **OAuth and OpenID Connect Settings**  in the setup page search bar.

4.  Enable **Allow Authorization Code and Credentials Flows**.

5.  Search for and select **App Manager** in the setup page search bar.

6.  On the App Manager page, select **New External Client App** to create an external client application.

7.  On the form, fill in the fields.

<table id="table_rwk_qrt_5kc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Basic Information

</td></tr><tr><td>

External Client App Name

</td><td>

Name of your application.

</td></tr><tr><td>

API Name

</td><td>

Name of the API. This field is automatically populated.

</td></tr><tr><td>

Contact Email

</td><td>

The email address that you want to associate with the application.

</td></tr><tr><td>

Distribution State

</td><td>

The scope of distribution of the application.Select **Local** as the distribution state.

</td></tr><tr><td>

Contact Phone

</td><td>

The phone number that you want to associate with the application.

</td></tr><tr><td>

Info URL

</td><td>

The URL of the web page with more information about your application.

</td></tr><tr><td>

Logo URL

</td><td>

The URL of your logo image that is displayed with the connected application.

</td></tr><tr><td>

Icon URL

</td><td>

The URL of the icon for the connected application.

</td></tr><tr><td>

Description

</td><td>

Description of the application.

</td></tr><tr><td class="sub-head" colspan="2">

API \(Enable OAuth Settings\)

</td></tr><tr><td>

Enable OAuth

</td><td>

Option to enable OAuth settings.Select this option to enable the OAuth settings.

</td></tr><tr><td>

Callback URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

</td></tr><tr><td>

OAuth Scopes

</td><td>

OAuth scopes that determine the amount of access that is granted to an access token. When the grant type is **Authorization Code**, use:

-   **Manage user data via APIs \(api\)**
-   **Perform requests at any time \(refresh\_token, offline\_access\)**
When the grant type is **Client Credentials**, use **Manage user data via APIs \(api\)**.

</td></tr><tr><td class="sub-head" colspan="2">

Flow Enablement

</td></tr><tr><td>

Enable Client Credentials Flow

</td><td>

Select this option when the grant type is **Client Credentials**.

</td></tr><tr><td class="sub-head" colspan="2">

Security

</td></tr><tr><td>

Require Secret for Web Server Flow

</td><td>

The option to implement the Require Secret for Web Server Flow in your external client app or connected app settings.-   If the grant type is **Authorization Code**, select this option.
-   If the grant type is **Client Credentials**, clear this option.


</td></tr><tr><td>

Require Secret for Refresh Token Flow

</td><td>

The option in your external client app or connected app while implementing the refresh token flow using a server-side callback handler.-   If the grant type is **Authorization Code**, select this option.
-   If the grant type is **Client Credentials**, clear this option.


</td></tr><tr><td>

Require Proof Key for Code Exchange \(PKCE\) Extension for Supported Authorization Flows

</td><td>

If this field is selected by default, clear the **Require Secret for Web Server Flow** and **Require Secret for Refresh Token Flow** options.**Note:** Enable **Require Proof Key for Code Exchange \(PKCE\) Extension for Supported Authorization Flows**.

</td></tr></tbody>
</table>8.  Select **Create**.

    The application registration is complete and you're redirected to the Manage External Client Apps page.

9.  Verify and edit the policies for the registered application by selecting **Edit**.

10. In the OAuth Policies section, verify that the **Permitted Users** field is set to **Admin approved users are pre-authorized** for the ServiceNow application.

    **Note:** Admin-approved users who are preauthorized enable any users with the corresponding profile or permission set to access the application without prior authorization. For more information, see [Pre-Authorize User App Access Through Connected App Policies](https://help.salesforce.com/s/articleView?id=xcloud.branded_apps_allow_deny_con_app.htm&type=5).

11. In the App Policies section, select either the profile of the integration user or the profile of the user that you want to use for the integration.

12. If you have selected the **Enable Client Credentials Flow** option, then in the OAuth Flows and External Client App Enhancements section, select **Enable Client Credentials Flow** and enter either the username or email address of the integration user that you want to use for the integration profile.

13. In the App Authorization section, verify that the **Refresh token policy** field is set to **Refresh token is valid until revoked** and the **IP Relaxation** field is set to **Relax IP restrictions**.

14. Select **Save**.

15. Retrieve OAuth credentials.

    1.  Navigate to **Settings** &gt; **OAuth Settings** and then select **Consumer Key and Secret**.

        The Salesforce login page opens in a new window.

    2.  Enter your credentials to log in to Salesforce.

    3.  Copy the **Consumer Key** and **Consumer Secret** and save them in a secure location for later use.


## Option 2: Set up the Salesforce spoke using JWT signing key

Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow using JWT signing key.

### Before you begin

-   [Create a connected app in Salesforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-sf-spk.md)
-   Role required: admin

### Attach a Java Key Store certificate to the Salesforce spoke

Enable the JSON Web Token \(JWT\) Bearer Grant token authentication by attaching a valid Java KeyStore \(JKS\) certificate to the Salesforce spoke.

#### Before you begin

-   Valid Java KeyStore certificate
-   Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Salesforce Certificate`.|
    |Expiration notification|Option to send a notification when the certificate is about to expire.|
    |Notify on expiration|Users that are notified when the certificate expires.|
    |Warn in days to expire|Number of days to send a notification before the certificate expires.|
    |Active|Option to actively use the certificate.|
    |Format|Certificate format. The instance supports the PEM and DER formats.|
    |Type|Type of certificate. Select **Java Key Store**.|
    |Valid from|Date from which the certificate is valid.|
    |Expires|Date on which the certificate expires.|
    |Expires in days|Number of days until the certificate expires.|
    |Key store password|Password associated with the certificate.|
    |Short description|Summary about the certificate.|
    |PEM Certificate|Contents of the X509 certificate.|

4.  Click the attachments icon \(\[Omitted image "attachments-icon.png"\] Alt text: Attachments icon\) and attach a JKS certificate.

5.  Click **Validate Stores/Certificates**.


#### Result

The JKS certificate is created and attached to the Salesforce spoke.

### Create a JWT signing key for the Salesforce spoke

Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore certificate.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the JWT signing key. For example, `Salesforce JWT Keys`.|
    |Signing Keystore|Valid JKS certificate attached in the previous task. For example, `Salesforce Certificate`.|
    |Key Id|Key ID to identify which key is used when multiple keys are used to sign tokens.|
    |Application|Application scope that contains this record. Select Salesforce spoke.|
    |Signing Algorithm|Algorithm to sign with the JWT key.|
    |Signing Key Password|Password associated with the signing key.|
    |Active|Option to actively use the certificate.|

4.  Click **Submit**.


#### Result

The JWT key is created and assigned to the JKS certificate.

### Create a JWT provider for the Salesforce spoke

Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Providers**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the JWT provider. For example, `Salesforce JWT Provider`.|
    |Expiry Interval \(sec\)|Number, in seconds, to set the lifespan of JWT provider tokens.|
    |Signing Configuration|JWT signing key from the previous step. For example, `Salesforce JWT Keys`.|

4.  Right-click the form header, and click **Save**.

    The Standard Claims and Custom Claims related lists are displayed.

5.  In the **Standard Claims** related list, enter values for **iss**, **sub**, and **aud**.

    See [OAuth 2.0 JWT Bearer Flow for Server-to-Server Integration](https://help.salesforce.com/articleView?id=remoteaccess_oauth_jwt_flow.htm&type=5) in [Salesforce Trailblazer forum](https://success.salesforce.com/) documentation for instructions.

6.  Click **Update**.


#### Result

The JWT provider is added to your ServiceNow instance.

### Register Salesforce as an OAuth Provider

Use the information generated during Salesforce connected app configuration to register Salesforce as an OAuth provider and enable the instance to request OAuth 2.0 tokens.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message `What kind of OAuth application?`

3.  Select **Connect to a third party OAuth Provider**.

    The system displays a blank Application Registries form.

4.  On the form, fill in the fields.

<table id="table_alw_kq3_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter `Salesforce OAuth`.

</td></tr><tr><td>

Client ID

</td><td>

Consumer key that you generated during the Salesforce connected app configuration.

</td></tr><tr><td>

Client Secret

</td><td>

Consumer secret that you generated during the Salesforce connected app configuration.

</td></tr><tr><td>

OAuth API Script

</td><td>

Optional script to customize the request and response.

</td></tr><tr><td>

Default Grant type

</td><td>

Grant type used to establish the token. Select **JWT Bearer**.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

Time, in seconds, that the refresh token is valid. The default time is 8,640,0000 seconds.

</td></tr><tr><td>

PKCE required

</td><td>

Option to enable public clients to require PKCE for an authorization.**Note:** You can use only **Authorization Code** as the **Default Grant type** when **PKCE** is enabled.

</td></tr><tr><td>

Application

</td><td>

Application scope that contains this record. Select Salesforce.

</td></tr><tr><td>

Accessible from

</td><td>

Application scope that this registry is accessible from.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the application registry.

</td></tr><tr><td>

Authorization URL

</td><td>

This field should be left blank.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint.-   For production instance, enter `https://login.salesforce.com/services/oauth2/token`.
-   For sandbox instance, enter `https://test.salesforce.com/services/oauth2/token`


</td></tr><tr><td>

Token Revocation URL

</td><td>

This field should be left blank.

</td></tr><tr><td>

Redirect URL

</td><td>

This field should be left blank.

</td></tr></tbody>
</table>5.  Right-click the form header, and click **Save**.

    -   The system validates the OAuth credentials and populates the **Redirect URL** field.
    -   The system populates **OAuth Entity Profile** with **Grant Type** as **JWT Bearer**. For example, **OAuth Entity Profile** is created with default **Name**, **Salesforce JWT provider default\_profile** .
6.  Copy the value from the **Redirect URL** field.

7.  Click **Update**.

8.  Log in to your Salesforce account to edit the configuration of your connected app.

    See the [Salesforce Trailblazer forum](https://success.salesforce.com/) documentation for instructions.

9.  Paste the Redirect URL value into the Callback URL of your Salesforce connected app.

    For example, paste `https://<instance-name>.service-now.com/oauth_redirect.do`.


#### Result

The instance can request OAuth 2.0 tokens for the Salesforce spoke.

**Note:** When an OAuth token expires, the spoke automatically regenerates a new token in most cases. If a token expires and is not regenerated, a user with the admin role can regenerate the spoke OAuth token.

### Create credential records for the Salesforce spoke

Create Credential records for the Salesforce connected app that you created. The Salesforce spoke connection and credential alias use these credentials to authorize actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?` .

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays a blank OAuth 2.0 Credentials form.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, enter `Salesforce Credentials`.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile that you created when you registered the Salesforce connected app as an OAuth provider. For example, select **Salesforce OAuth default\_profile**.|
    |Applies to|MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Order to apply this credential. For example, enter `100`.|

5.  Save the record.

6.  Click the **Get OAuth Token** related link to generate the OAuth token.


#### Result

The credential record for the Salesforce spoke is created.

### Create connection records for the Salesforce spoke

Create connection records for your Salesforce account. The Salesforce spoke connection and credential alias use these connections to perform actions in Salesforce.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **Salesforce**.

3.  On the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  Enter these values.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the connection record. For example, enter `Salesforce Connection`.

</td></tr><tr><td>

Credential

</td><td>

Credential record you that created for Salesforce. For example, select **Salesforce Credentials**.

</td></tr><tr><td>

Connection alias

</td><td>

Alias record associated with this connection.

</td></tr><tr><td>

URL builder

</td><td>

**Note:** Do not select the check box.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to your Salesforce instance. For example, `https://<instance-name>.salesforce.com`.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server. If you select this check box, define the fields in the Advanced MID Server Configuration related list.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr></tbody>
</table>5.  Right-click the form header and click **Save**.

6.  Ensure that **api\_version** is set `v48.0` in the Attributes related list.


#### Result

The Salesforce spoke is set up and integrated with the ServiceNow instance.

