---
title: Set up the Salesforce spoke
description: Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow.Add and configure a Salesforce connection to authenticate ServiceNow requests in Salesforce spoke.Create a connected app in your Salesforce account to enable OAuth 2.0 authentication with the Salesforce spoke.Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow using OAuth authorization template.Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow using JWT signing key.Enable the JSON Web Token \(JWT\) Bearer Grant token authentication by attaching a valid Java KeyStore \(JKS\) certificate to the Salesforce spoke.Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore certificate.Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.Use the information generated during Salesforce connected app configuration to register Salesforce as an OAuth provider and enable the instance to request OAuth 2.0 tokens.Create Credential records for the Salesforce connected app that you created. The Salesforce spoke connection and credential alias use these credentials to authorize actions.Create connection records for your Salesforce account. The Salesforce spoke connection and credential alias use these connections to perform actions in Salesforce.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Salesforce Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Salesforce spoke

Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Salesforce spoke
-   Role required: admin.

**Note:** Two spoke setup procedures are outlined here. Perform one of the procedures as per your requirement.

-   To setup the spoke using OAuth authorization template, see [Option 1: Set up the Salesforce spoke using OAuth authorization template](setup-sf-spk.md#).
-   To setup the spoke using JWT signing key, see [Option 2: Set up the Salesforce spoke using JWT signing key](setup-sf-spk.md#).

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

5.  Select **View Details**.![Connection template for Salesforce spoke](../image/salesforce-spoke-conn-templt.png)

6.  Configure the Salesforce connection.

    1.  Add or edit a connection.

        -   To set up an existing connection, select **Configure** or **Edit**.
        -   To create and configure a new connection, select **Add Connection**.
        **Note:** To support multiple connections through a spoke, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).

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

-   [Create a connected app in Salesforce](setup-sf-spk.md#)
-   Role required: admin

### Procedure

1.  Navigate to **Connection &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the record for**Salesforce**.

3.  Select the **Create New Connection &amp; Credential** related link.

4.  On the form, fill in the fields.

<table id="table_tsx_ytb_xrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection information

</td></tr><tr><td>

Connection name

</td><td>

Name to identify the connection record.

</td></tr><tr><td>

Connection URL \(Instance URL\)

</td><td>

Base URL to connect to your Salesforce instance in this format: `https://<instance-name>.salesforce.com`

</td></tr><tr><td class="sub-head" colspan="2">

Credential information

</td></tr><tr><td>

Grant type

</td><td>

The OAuth 2.0 grant type for your application. Possible values are:-   **Authorization Code**
-   **Client Credentials**


</td></tr><tr><td>

OAuth Client ID

</td><td>

Consumer key that you generated during the Salesforce connected app configuration.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Consumer secret that you generated during the Salesforce connected app configuration.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically.

</td></tr></tbody>
</table>5.  Select **Create and Get OAuth Token**.

    The OAuth2 authentication dialog box is displayed.

6.  Log in to the Salesforce admin account that you used to create your Salesforce application.

    Your ServiceNow instance creates an OAuth token for Salesforce and then automatically returns you to the Integration Profile form.

7.  Select **Publish**.


## Option 2: Set up the Salesforce spoke using JWT signing key

Integrate your Salesforce account with your ServiceNow instance. Create a custom OAuth application in Salesforce and authenticate requests from ServiceNow using JWT signing key.

### Before you begin

-   [Create a connected app in Salesforce](setup-sf-spk.md#)
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

4.  Click the attachments icon \(![Attachments icon](../image/attachments-icon.png)\) and attach a JKS certificate.

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

