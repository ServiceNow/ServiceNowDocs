---
title: Set up Adobe Experience Platform spoke
description: Integrate your Adobe Experience Platform account with your ServiceNow instance. Create a custom OAuth application in Adobe Experience Platform and authenticate requests from ServiceNow.Enable the JWT Bearer Grant token authentication by attaching a valid Java KeyStore \(JKS\) certificate to the Adobe Experience Platform spoke.Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore certificate.Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.Use the information generated during Adobe ID account creation and configuration to register Adobe Experience Platform as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create Credential records to the Adobe ID account you created. The Adobe Experience Platform spoke connection and credential alias uses these credentials to authorize actions.Create Connection records to your Adobe ID account. The Adobe Experience Platform spoke connection and credential alias uses these connections to perform actions in Adobe Experience Platform.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Adobe Experience Platform Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Adobe Experience Platform spoke

Integrate your Adobe Experience Platform account with your ServiceNow instance. Create a custom OAuth application in Adobe Experience Platform and authenticate requests from ServiceNow.

## Before you begin

-   Request Integration Hub subscription
-   Activate Adobe Experience Platform spoke
-   Role required: admin

## About this task

The Adobe Experience Platform spoke can also be set up using the Connection &amp; Credential configuration templates. However, using templates, only one set of alias records can be used at a time.

## Attach a Java Key Store certificate to the Adobe Experience Platform spoke

Enable the JWT Bearer Grant token authentication by attaching a valid Java KeyStore \(JKS\) certificate to the Adobe Experience Platform spoke.

### Before you begin

-   Valid Java KeyStore certificate
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `AEP Certificate`.|
    |Expiration notification|Option to send a notification when the certificate is about to expire.|
    |Notify on expiration|Users to be notified when the certificate expires.|
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


### Result

The JKS certificate is created and attached to the Adobe Experience Platform spoke.

## Create a JWT signing key for the Adobe Experience Platform spoke

Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore certificate.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the JWT signing key. For example, `AEP JWT Keys`.|
    |Signing Keystore|Valid JKS certificate attached in the previous task. For example, `AEP Certificate`.|
    |Key Id|Key ID to identify which key is used when multiple keys are used to sign tokens.|
    |Application|Application scope that contains this record. Select Adobe Experience Platform spoke.|
    |Signing Algorithm|Algorithm to sign with the JWT key.|
    |Signing Key Password|Password associated with the signing key.|
    |Active|Option to actively use the certificate.|

4.  Click **Submit**.


### Result

The JWT key is created and assigned to the JKS certificate.

## Create a JWT provider for the Adobe Experience Platform spoke

Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Providers**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Nname to uniquely identify the JWT provider. For example, `AEP JWT Provider`.|
    |Expiry Interval \(sec\)|Number in seconds to set the lifespan of JWT provider tokens.|
    |Signing Configuration|JWT signing key from the previous step. For example, `AEP JWT Keys`.|

4.  Right-click the form header, and click **Save**.

    The Standard Claims and Custom Claims related lists are displayed.

5.  Enter values for **iss**, **sub**, and **aud** in the Standard Claims related list.

    See the [Adobe Experience Platform](https://www.adobe.io/apis/experienceplatform/home.html) documentation for instructions.

6.  Enter these values in the Custom Claims related list.

    |Field|Value|
    |-----|-----|
    |Claim Name|https://ims-na1.adobelogin com/s/entdataservices\_sdk|
    |Claim Value Type|true\|false|
    |Claim Value|true|

7.  Click **Update**.


### Result

The JWT provider is added to your ServiceNow instance.

## Register Adobe Experience Platform as OAuth Provider

Use the information generated during Adobe ID account creation and configuration to register Adobe Experience Platform as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message **What kind of OAuth application?**

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

Name to uniquely identify the record. For example, enter `AEP OAuth`.

</td></tr><tr><td>

Client ID

</td><td>

Consumer key you generated during the Adobe ID account configuration.

</td></tr><tr><td>

Client Secret

</td><td>

Consumer secret you generated during the Adobe ID account configuration.

</td></tr><tr><td>

OAuth API Script

</td><td>

Script to customize the request and response. Select **OAuthUtilAEP**.

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

Application scope that contains this record. Select Adobe Experience Platform.

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

OAuth server token endpoint. Enter `https://ims-na1.adobelogin.com/ims/exchange/jwt/`.

</td></tr><tr><td>

Token Revocation URL

</td><td>

This field should be left blank.

</td></tr><tr><td>

Redirect URL

</td><td>

This field should be left blank.

</td></tr><tr><td>

Use mutual authentication

</td><td>

Option to use mutual authentication for token request and revocation. This option requires a mutual authentication profile to be specified.

</td></tr><tr><td>

Send Credentials

</td><td>

Client credentials in the request.

</td></tr></tbody>
</table>5.  Right-click the form header, and click **Save**.

    -   The system validates the OAuth credentials and populates the **Redirect URL**.
    -   The system populates **OAuth Entity Profile** with **Grant Type** as **JWT Bearer**. For example, **OAuth Entity Profile** is created with default **Name**, **AEP default\_profile**
6.  Open the record of OAuth Entity Profile.

7.  Select the JWT Provider record for **JWT Provider**, for example, `AEP JWT Provider`.

8.  Click **Update**.


### Result

The instance can request OAuth 2.0 tokens for the spoke.

**Note:** When an OAuth token expires, the spoke automatically regenerates a new token in most cases. If a token expires and is not regenerated, an administrator can regenerate the spoke OAuth token.

## Create Credential records for the Adobe Experience Platform

Create Credential records to the Adobe ID account you created. The Adobe Experience Platform spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

### About this task

You must create two credential records; one for data inlet management and batch ingestion, and other for data collection.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays a blank OAuth 2.0 Credentials form.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, enter `AEP` for data inlet management and batch ingestion, and `AEP_Ingestion` for data collection.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile you created when you registered the Salesforce connected app as an OAuth provider. For example, select **AEP OAuth default\_profile**.|
    |Applies to|This field isn't applicable.|
    |Order|Order to apply this credential. For example, enter `100`.|

5.  Save the record.

6.  Click the **Get OAuth Token** related link to generate the OAuth token.


### Result

The credential records for the Adobe Experience Platform spoke is created.

## Create Connection records for the Adobe Experience Platform spoke

Create Connection records to your Adobe ID account. The Adobe Experience Platform spoke connection and credential alias uses these connections to perform actions in Adobe Experience Platform.

### Before you begin

Role required: admin

### About this task

Two connection and credential alias records are available by default; one for data inlet management and batch ingestion, and other for data collection. Perform these steps to associate each alias with the respective Adobe Experience Platform API.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the required Adobe Experience Platform spoke record.

    **Note:** There are two connection and credential records; **AEP** and **AEP\_Ingestion**. The **AEP** record is for data inlet management and batch ingestion, and **AEP\_Ingestion** is for data collection.

3.  From the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  Enter these values.

<table id="table_any_shp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the connection record. For example, enter `AEP Platform` for data inlet management and batch ingestion, and `AEP dcs` for data collection.

</td></tr><tr><td>

Credential

</td><td>

Credential record you created for Adobe Experience Platform. For example, select **AEP** and **AEP\_Ingestion**.

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

Base URL to connect to Adobe Experience Platform.-   If the connection record is for data inlet management and batch ingestion, enter `https://platform.adobe.io/`.
-   If the connection record is for data collection, enter `https://dcs.adobedc.net`.


</td></tr><tr><td>

Use MID server

</td><td>

This field isn't applicable.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that the action or activity runs in.

</td></tr></tbody>
</table>5.  In the**Attributes** tab enter these values.

    -   Internal name of the sandbox in **Sandbox**.

        **Note:** Ensure that you provide the internal name of the required sandbox and not its label in **Sandbox**. To obtain the internal name of the required sandbox, use the Get All Sandboxes action.

    -   If the connection record is for data inlet management and batch ingestion, enter **API Key** and **Organization ID**.
    -   If the connection record is for streaming ingestion, enter **Organization ID**.
6.  Right-click the form header and click **Save**.


### Result

The Adobe Experience Platform spoke is set up and integrated with the ServiceNow instance.

