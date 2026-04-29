---
title: Set up Docusign eSignature spoke using JWT grant
description: Integrate the ServiceNow instance and Docusign by using JWT grant to authenticate ServiceNow requests.Create a custom OAuth application from your Docusign account to enable OAuth 2.0 authentication with the Docusign eSignature spoke.Generate a JKS certificate for the JWT authentication of the Docusign eSignature spoke.Enable the JWT Bearer Grant token authentication by attaching a valid Java KeyStore \(JKS\) certificate to the Docusign eSignature spoke.Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore certificate.Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.Use the information generated during Docusign account configuration to register Docusign as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Obtain explicit consent for the ServiceNow application from Docusign.Create Credential records to the Docusign custom OAuth application you created during Docusign account configuration. The Docusign spoke connection and credential alias uses these credentials to authorize actions.Create Connection records to your Docusign account. The Docusign spoke connection and credential alias uses these connections to perform actions in DocuSsign.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Docusign eSignature Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Docusign eSignature spoke using JWT grant

Integrate the ServiceNow instance and Docusign by using JWT grant to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Docusign eSignature spoke.
-   Role required: admin.

**Important:** If you are setting up Docusign eSignature spoke using JWT grant, you need not set up the spoke using authorization code grant.

## Configure Docusign account

Create a custom OAuth application from your Docusign account to enable OAuth 2.0 authentication with the Docusign eSignature spoke.

### Before you begin

Docusign requirements:

-   Docusign account
-   Docusign app configured to integrate with ServiceNow
-   Role required: Docusign administrator

### About this task

Complete these steps from your Docusign account. See the [Docusign Developer Center](https://developers.docusign.com/) documentation for instructions on creating and configuring custom applications. Docusign uses a scripted webhook to send signed document data to ServiceNow instance. This enables flow designers to pause a flow until a document is signed, and use document data in the flow.

### Procedure

1.  From your Docusign account, register your application.

2.  Generate an integrator key and secret key.

3.  Record the values of integrator key and secret key to register the app as a third-party OAuth provider on your ServiceNow instance.

    You need these values when you [Register Docusign as OAuth Provider](setup-docusign-jwt.md#)

4.  Click **ADD RSA KEYPAIR** and record the **Keypair ID**, **Public Key**, and **Private Key**.

5.  Add the ServiceNow OAuth Redirect URL in your Docusign account.

    1.  Navigate to **Integrations** &gt; **App and Keys**.

    2.  Under **Apps and Integration Keys**,find the required app.

    3.  For the required app, click the **Actions** drop-down list and click **Edit**.

    4.  Under **Additional settings**, click **Add URI** and add the OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`.

        ![Add Redirect URI in Docusign account.](../image/docusign-add-redirect-uri.png)

6.  Obtain the value of **Account Base URI** from the Docusign account.

    1.  Navigate to **Integrations** &gt; **App and Keys**.

    2.  Under **My Account Information**, you can find the value of the **Account Base URI**.

        ![Account Base URI.](../image/docusign-acct-base-uri.png)

    3.  Copy and record this value for later use.


## Generate the JKS certificate

Generate a JKS certificate for the JWT authentication of the Docusign eSignature spoke.

### Before you begin

Role required: admin

### Procedure

1.  Open the text editor for code such as, Sublime Text.

2.  Create a new file.

3.  Paste the Private Key you had earlier generated from your Docusign integrator app.

    For more information, see [Configure Docusign account](setup-docusign-jwt.md#).

    **Note:** Ensure that you include both beginning and ending of the private key.

4.  Save the file with the .key extension, for example, `privatekey.key`.

5.  Open terminal and navigate to the directory where you saved the file with the `.key` extension.

6.  Create a CA signed certificate using your private key by executing the command:

    ```
    openssl req -new -x509 -key <file-name>.key -out <certificate-name>.pem -days 1095
    ```

    System prompts you to provide required details such as Country Name, Province Name and so on.

7.  Enter the required details.

8.  Create PKCS 12 file using your private key and CA signed certificate by executing the command:

    ```
    openssl pkcs12 -export -in <certificate-name>.pem -inkey <file-name>.key -certfile <certificate-name>.pem -out <PKCS-12-file-name>.p12 
    ```

    System prompts you to provide a password.

9.  Provide the export password.

10. Create the JKS file by executing this command:

    ```
    keytool -importkeystore -srckeystore <PKCS-12-file-name>.p12 -srcstoretype pkcs12 -destkeystore <JKS-certificate-filename>.jks -deststoretype JKS
    ```

    System prompts you to provide a password.

11. Provide the destination and source keystore passwords.


## Attach a Java Key Store certificate to the Docusign eSignature spoke

Enable the JWT Bearer Grant token authentication by attaching a valid Java KeyStore \(JKS\) certificate to the Docusign eSignature spoke.

### Before you begin

-   Ensure the availability of a valid Java KeyStore certificate
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name to uniquely identify the record. For example, `Docusign Certificate`.|
    |Notify on expiration|Define users to be notified when the certificate expires.|
    |Warn in days to expire|Enter the number of days to send a notification before the certificate expires.|
    |Active|Enable|
    |Type|Select **Java Key Store**.|
    |Expires in days|Enter the number of days until the certificate expires.|
    |Key store password|Enter a password associated with the certificate.|
    |Short description|Enter a summary about the certificate.|

4.  Click the attachments icon \(![Attachments icon](../image/attachments-icon.png)\) and attach a JKS certificate.

5.  Click **Validate Stores/Certificates**.


## Create a JWT signing key for the Docusign eSignature spoke

Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore certificate.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name to uniquely identify the JWT signing key. For example, `Docusign JWT Keys`.|
    |Signing Keystore|Select the valid JKS certificate attached in the previous task. For example, `Docusign Certificate`.|
    |Key Id|Enter a key Id to identify which key is used when multiple keys are used to sign tokens.|
    |Signing Algorithm|Select an algorithm to sign with the JWT key.|
    |Signing Key Password|Enter a password associated with the signing key.|
    |Active|Enable.|

4.  Click **Submit**.


## Create a JWT provider for the Docusign eSignature spoke

Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Providers**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name to uniquely identify the JWT provider. For example, `Docusign JWT Provider`.|
    |Expiry Interval \(sec\)|Enter a number in seconds to set the lifespan of JWT provider tokens.|
    |Signing Configuration|Select a JWT signing key. For example, `Docusign JWT Keys`.|

4.  Right-click the form header, and click **Save**.

    The Standard Claims and Custom Claims related lists display.

5.  On the same page of the JWT provider record, enter values for **iss**, **sub**, and **aud** in the **Standard Claims** related list.

    |Claim|Value|
    |-----|-----|
    |iss|`<your_integration_key>`|
    |sub|`<your_user_ID>`|
    |aud|`account-d.docusign.com`|

    For more information, see [How to get an access token with JWT Grant](https://developers.docusign.com/platform/auth/jwt-get-token/) in [Docusign Developer Center](https://developers.docusign.com/).

6.  Insert a record in the **Custom Claims** related list and complete the form.

    |Field|Value|
    |-----|-----|
    |Claim Name|scope|
    |Claim Value Type|string|
    |Claim Value|signature impersonation|

7.  Click **Update**.


## Register Docusign as OAuth Provider

Use the information generated during Docusign account configuration to register Docusign as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message **What kind of OAuth application?**

3.  Select **Connect to a third party OAuth Provider**.

    The system displays a blank Application Registries form.

4.  Complete the form.

<table id="table_alw_kq3_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record. For example, enter `Docusign OAuth`.

</td></tr><tr><td>

Client ID

</td><td>

Enter the integrator key you generated during the Docusign account configuration.

</td></tr><tr><td>

Client Secret

</td><td>

Enter the client secret you generated during the Docusign account configuration.

</td></tr><tr><td>

Default Grant type

</td><td>

Select **JWT Bearer**.

</td></tr><tr><td>

Authorization URL

</td><td>

-   For developer sandbox environment, enter `https://account-d.docusign.com/oauth/auth`.
-   For live production system, enter `https://account.docusign.com/oauth/auth`.


</td></tr><tr><td>

Token URL

</td><td>

-   For developer sandbox environment, enter `https://account-d.docusign.com/oauth/token`.
-   For live production system, enter `https://account.docusign.com/oauth/token`. For more information see, [Post Go-Live](https://developers.docusign.com/esign-rest-api/guides/post-go-live) and [User Info Endpoint Reference](https://developers.docusign.com/esign-rest-api/guides/authentication/user-info-endpoints) in the [Docusign Developer Center](https://developers.docusign.com/) documentation.


</td></tr></tbody>
</table>5.  Right-click the form header, and click **Save**.

    -   The system validates the OAuth credentials and populates the **Redirect URL**.
    -   The system populates **OAuth Entity Profile** with **Grant Type** as **JWT Bearer**. For example, **OAuth Entity Profile** is created with default **Name**, **Docusign OAuth default\_profile**
6.  Insert a record in the **OAuth Entity Scopes** related list and fill the values.

    |Field|Value|
    |-----|-----|
    |Name|scope|
    |OAuth Scope|signature impersonation|

7.  Copy the value from **Redirect URL**.

8.  Click **Update**.

9.  Login to your Docusign account to edit the configuration of your custom Docusign application.

    See the [Docusign Developer Center](https://developers.docusign.com/) for instructions.

10. Paste the Redirect URL value into the Redirect URI for your custom Docusign application.

    For example, paste `https://instance.service-now.com/oauth_redirect.do`


### Result

The instance can request OAuth 2.0 tokens for the spoke.

**Note:** When an OAuth token expires, the spoke automatically regenerates a new token in most cases. If a token expires and is not regenerated, an administrator can regenerate the spoke OAuth token.

## Obtain consent

Obtain explicit consent for the ServiceNow application from Docusign.

Role required: admin

### Obtain consent for an organization administrator

See [Docusign Developer documentation \(Admin consent for internal applications\)](https://developers.docusign.com/esign-rest-api/guides/authentication/obtaining-consent#admin-consent-for-internal-applications) for instructions to obtain consent for an organization administrator.

## Create Credential records for the Docusign eSignature spoke

Create Credential records to the Docusign custom OAuth application you created during Docusign account configuration. The Docusign spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays a blank OAuth 2.0 Credentials form.

4.  Fill these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `Docusign Credentials`.|
    |Active|Enable|
    |OAuth Entity Profile|Select the OAuth profile you created when you registered the custom Docusign application as an OAuth provider. For example, select **Docusign OAuth default\_profile**.|
    |Applies to|Select the MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Save the record.

6.  Click the **Get OAuth Token** related link to generate the OAuth token.


## Create Connection records for the Docusign eSignature spoke

Create Connection records to your Docusign account. The Docusign spoke connection and credential alias uses these connections to perform actions in DocuSsign.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **Docusign**.

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

Enter any name to uniquely identify the connection record. For example, enter `Docusign Connection`.

</td></tr><tr><td>

Credential

</td><td>

Select the Credential record you created for Docusign. For example, select **Docusign Credentials**.

</td></tr><tr><td>

Connection URL

</td><td>

-   For demo environment, enter `https://demo.docusign.net`.
-   For live production system, enter the Base URI such as `na2.docusign.net` or `eu.docusign.net`. For instructions on obtaining the base URI, see [Post Go-Live](https://developers.docusign.com/esign-rest-api/guides/post-go-live) and [User Info Endpoint Reference](https://developers.docusign.com/esign-rest-api/guides/authentication/user-info-endpoints) in the [Docusign Developer Center](https://developers.docusign.com/) documentation.


</td></tr></tbody>
</table>5.  Click **Submit**.


### What to do next

Synchronize ServiceNow with Docusign to access Docusign accounts, templates, and envelopes from the Docusign spoke. See [Synchronize Docusign with ServiceNow](sync-docusign-servicenow.md).

