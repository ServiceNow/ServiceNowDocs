---
title: Set up the SuccessFactors spoke v4.x.x
description: Integrate the ServiceNow instance with your SuccessFactors instance using OAuth client application and API key.Enable client certificate authentication for the outbound communication by generating the keystore.jks and keystore.cer files.Enable client certificate authentication for the outbound communication by uploading the JKS certificate in your ServiceNow instance.Use the API key generated during the client application configuration to register the application as an OAuth provider.Create a SAML2 assertion record to generate the SAML2 assertion and exchange the assertion for the access tokens with the provider.Create Credential record for the OData APIs in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these credentials to authorize actions using the OData API.Create Credential record for the SOAP APIs in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these credentials to authorize actions using the SOAP APIs.Create a Connection record for the OData API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.Create a Connection record for the SOAP API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.Customise the sample flows as per your requirement to synchronize data between your SuccessFactors and ServiceNow instances.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [SuccessFactors Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SuccessFactors spoke v4.x.x

Integrate the ServiceNow instance with your SuccessFactors instance using OAuth client application and API key.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SuccessFactors spoke.
-   Enable these system properties:
    -   **glide.pf.rest.response\_payload\_max\_size**: The maximum value is, `10240`.
    -   **com.snc.process\_flow.reporting.serialized.val\_size\_limit**: The maximum value is, `16384`.
    -   **com.glide.transform.json.max-partial-length**: The maximum value is, `65536`.
-   Role required: admin.

**Note:** This procedure is applicable if you are setting up the SuccessFactors spoke v4.10.1 for the first time. If you are using an earlier version of the SuccessFactors spoke, see [Migrate to SuccessFactors spoke v4.10.1](migrate-successfactors.md) for the migration procedure.

For more information about setting up the spoke, see [SAP SuccessFactors Spoke - OAuth Setup &amp; Migration - Pre-Tokyo, Tokyo and beyond](https://www.servicenow.com/community/knowledge-managers/sap-successfactors-spoke-oauth-setup-amp-migration-pre-tokyo/ta-p/2468046) in [ServiceNow Community](https://www.servicenow.com/community/).

## Register OAuth client application in SuccessFactors

Enable client certificate authentication for the outbound communication by generating the keystore.jks and keystore.cer files.

### Before you begin

-   Generate a valid JKS certificate. For information about creating a JKS certificate, see [Creating Java Keystore\(JKS\) with Private Key and Certificate Chain](https://help.sap.com/docs/SAP_Cloud_Platform_Master_Data_for_Business_Partners/246fb358c1c7413289c03b8c72734209/18f5bae37a664396b2ebbc1b3c384c53.html) in [SAP Help Portal](https://help.sap.com/docs/), or, do the steps.
    1.  Use the command `openssl genrsa -out private.key 2048` to generate the private.key file.
    2.  Use the private.key to create x.509 certificate \(.cer file\) that contains your public key.

        Use the command `openssl req -new -x509 -key private.key -out publickey.cer -days 365`

-   Convert the public and private key to a .p12 file.

    Use the command to do the above step `openssl pkcs12 -export -in publickey.cer -inkey private.key -out successfactors.p12 -name "<provide custom name>".`

-   Convert the .p12 file to .jks

    Use the command to do the above step `keytool -importkeystore -srckeystore successfactors.p12 -srcstoretype pkcs12 -destkeystore successfactors.jks`.

-   Role required: admin.

### Procedure

1.  Log in to the SuccessFactors account as an admin.

2.  Navigate to **Admin Centre** and click **Company Settings**.

3.  Click **Manage OAuth2 Client Applications**.

4.  Click **Register Client Application**.

    ![Register a client application.](../image/sapsf-oauth-app.png)

5.  Provide the required details on the form.

    In the **X.509 Certificate** field, provide contents of the cert.pem file \(public key\) without the headers.

6.  Click **Submit**.

    **API Key** is generated and displayed. Copy and record the value for later use.


## Upload the JKS certificate in your ServiceNow instance

Enable client certificate authentication for the outbound communication by uploading the JKS certificate in your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Upload the JKS certificate to your ServiceNow instance.

    For instructions to upload the JKS certificate, see [Upload a certificate to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_UploadACertificateToAnInstance.md) .

    ![Upload JKS certificate.](../image/sapsf-cert.png)


## Register SuccessFactors as an OAuth provider

Use the API key generated during the client application configuration to register the application as an OAuth provider.

### Before you begin

Role required: admin

### Procedure

1.  In your ServiceNow instance, navigate to **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

3.  In the form, fill in these fields.

<table id="table_yb3_bwh_dwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name to identify the certificate. For example, `SuccessFactors SAML`.

</td></tr><tr><td>

Client ID

</td><td>

Value of the API key you had copied after registering the OAuth client application in SuccessFactors.

</td></tr><tr><td>

Client Secret

</td><td>

**Note:** Client secret is not needed to register the application as an OAuth provider. You can provide any value for this field.

</td></tr><tr><td>

OAuth API Script

</td><td>

Name of the OAuth API script. Search for `OAuthUtilSuccessFactors` and select it from the list.

</td></tr><tr><td>

Default Grant Type

</td><td>

Default grant type used to establish the token. Select **SAML2 Bearer**.

</td></tr><tr><td>

Token URL

</td><td>

SuccessFactors OAuth server endpoint URL that includes the Company ID in this format: `https://<SuccessFactors_Instance_Name>/oauth/token?company_id=<Company_ID>`. For example, `https://example.successfactors.eu/oauth/token?company_id=SFCPART123456`.

</td></tr></tbody>
</table>    ![Application registry record.](../image/sapsf-app-reg.png)

4.  Click **Submit**.


## Create the SAML2 assertion producer record

Create a SAML2 assertion record to generate the SAML2 assertion and exchange the assertion for the access tokens with the provider.

### Before you begin

Role required: admin

### Procedure

1.  Create a SAML2 assertion producer record in your ServiceNow instance.

    1.  Navigate to **All** &gt; **System OAuth** &gt; **SAML2 Assertion Producers**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name to identify the SAML2 assertion producer record. For example, `Successfactor SAML OAuth`.|
        |Issuer|Unique identifier for the assertion issuing entity. Provide the ServiceNow instance URL.|
        |Subject NameID|User name to log in to the SuccessFactors instance. For example, `sfadmin`.|
        |Audience|Intended audience for the assertion. Enter the value, `www.successfactors.com`.|
        |Recipient|Intended recipient for the assertion. Enter URL in this format, `https://<SuccessFactors-Instance-Name>/oauth/token`.|

        ![SAML2 assertion producer record.](../image/successfactors-saml2-assertion-prod.png)

    4.  Right-click the form header and click **Save**.

    5.  Under the **SAML2 Assertion Keystores** tab, click **New**.

    6.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name to identify the SAML2 assertion keystore record. For example, `sap_successfactor`.|
        |Signing Key Alias|Alias of key entry stored in the Keystore used to sign the assertion. For example, `1`.|
        |Signing Key Password|Password of the key entry stored in the keystore used to sign the assertion.|
        |Signing Keystore|Required X.509 certificate record. Select the X.509 certificate record that you had earlier created. For more information, see [Upload the JKS certificate in your ServiceNow instance](setup-successfactors.md#).|

        ![SAML2 assertion keystore record.](../image/sapsf-assertion-ks.png)

    7.  Click **Submit**.

    8.  Navigate to **All** &gt; **System OAuth** &gt; **SAML2 Assertion Producers**.

    9.  Open the SAML2 assertion producer record that you had created.

        For example, **Successfactor SAML OAuth**.

    10. Under the **SAML2 Assertion Attributes** tab, click **New**.

    11. On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the SAML2 assertion attribute record. Enter `api_key`.|
        |Type|Type of the **Value** field. Select **String**.|
        |Value|API key generated after the OAuth client application is created in SuccessFactors.|

        ![SAML2 assertion attribute record.](../image/sapsf-assertion-attribute.png)

    12. Click **Submit**.

2.  Associate the SAML2 assertion producer with the application registry record.

    1.  Navigate to **System OAuth** &gt; **Application Registry**.

    2.  Open the application registry record that you had created.

        For example, **SuccessFactors OAuth Reg**. For more information about creating the application registry, see [Register SuccessFactors as an OAuth provider](setup-successfactors.md#).

    3.  Under the **OAuth Entity Profiles** tab, open the default OAuth entity profile record.

        For example, **Successfactor SAML default\_profile**.

    4.  For the **Assertion Producer** field, select the SAML2 assertion producer record you had created.

        For example, **Successfactor SAML OAuth**.

        ![OAuth entiy profile record.](../image/sapsf-assertion-oauth.png)

    5.  Click **Update**.


## Create Credential record for the OData API

Create Credential record for the OData APIs in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these credentials to authorize actions using the OData API.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    An empty OAuth 2.0 Credentials form is displayed.

4.  On the form, fill these values.

<table id="table_twl_mk2_5kb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter `SAML_SuccessFactors_OData_Cred`.

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

OAuth entity profile record that is associated with the OAuth application registry you had created. For example, `Successfactor SAML default_profile`.For more information about creating the application registry, see [Register SuccessFactors as an OAuth provider](setup-successfactors.md#).

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Order

</td><td>

Order to apply this credential. For example, enter `100`.

</td></tr></tbody>
</table>    ![OData credential record.](../image/sapsf-odata-cred.png)

5.  Click **Submit**.


### Result

The credential record to authorize actions using the OData API is created.

## Create Credential record for the SOAP API

Create Credential record for the SOAP APIs in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these credentials to authorize actions using the SOAP APIs.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    An empty OAuth 2.0 Credentials form is displayed.

4.  On the form, fill these values.

<table id="table_twl_mk2_5kb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter `SAML_SuccessFactors_SOAP_Cred`.

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

OAuth entity profile record associated with the OAuth application registry you had created. For example, `Successfactor SAML default_profile`.For more information about creating the application registry, see [Register SuccessFactors as an OAuth provider](setup-successfactors.md#).

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Order

</td><td>

Order to apply this credential. For example, enter `100`.

</td></tr></tbody>
</table>    ![SOAP credential record.](../image/sapsf-soap-cred.png)

5.  Click **Submit**.


### Result

The credential record to authorize actions using the SOAP API is created.

## Create Connection record for the OData API

Create a Connection record for the OData API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **SuccessFactors OData**.

    For example, **SuccessFactors\_OData**.

3.  From the **Connections** tab, click **New**.

    The system displays an empty HTTP\(s\) Connection form.

4.  On the form, fill these values.

<table id="table_ol3_3nt_wkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `SAML_SuccessFactors_OData_Conn`.

</td></tr><tr><td>

Credential

</td><td>

Credential record you created for the REST API. For example, `SAML_SuccessFactors_OData_Cred`.

</td></tr><tr><td>

Connection URL

</td><td>

SuccessFactors service root URL in this format: `https://<SuccessFactors_Instance_Name>/odata/v2`. For example, `https://example.successfactors.eu/odata/v2`.**Note:** If you are using an SAP Cloud account, see [List of SAP SuccessFactors API Servers](https://help.sap.com/docs/SAP_SUCCESSFACTORS_PLATFORM/93f95815070049ebaaff042d8322d518/af2b8d5437494b12be88fe374eba75b6.html) in [SAP Help Portal](https://help.sap.com/docs/) to select the correct endpoint that is needed to target the API server.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection record.

</td></tr></tbody>
</table>    ![OData connection record.](../image/sapsf-odata-conn.png)

5.  Click **Submit**.


### Result

The connection record for the REST API in SuccessFactors is created.

## Create Connection record for the SOAP API

Create a Connection record for the SOAP API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **SuccessFactors SOAP API**.

    For example, **SuccessFactors\_Comp\_Emp**.

3.  From the **Connections** tab, click **New**.

    The system displays an empty HTTP\(s\) Connection form.

4.  On the form, fill these values.

<table id="table_ol3_3nt_wkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `SAML_SuccessFactors_SOAP_Conn`.

</td></tr><tr><td>

Credential

</td><td>

Credential record you created for the SOAP API. For example, `SAML_SuccessFactors_SOAP_Cred`.

</td></tr><tr><td>

Connection URL

</td><td>

SuccessFactors connection URL. For example, `https://<SuccessFactors_Instance_Name>/sfapi/v1/soap`. For example, `https://example.successfactors.eu/sfapi/v1/soap`.**Note:** If you are using an SAP Cloud account, see [List of SAP SuccessFactors API Servers](https://help.sap.com/docs/SAP_SUCCESSFACTORS_PLATFORM/93f95815070049ebaaff042d8322d518/af2b8d5437494b12be88fe374eba75b6.html) in [SAP Help Portal](https://help.sap.com/docs/) to select the correct endpoint that is needed to target the API server.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection record.

</td></tr></tbody>
</table>5.  In the **Attributes** tab, provide these fields.

    |Field|Description|
    |-----|-----------|
    |Company Id|Immutable Company ID of your SuccessFactors instance.|
    |Flow Timeout \(seconds\)|Maximum time in seconds up to which data can be received from SuccessFactors during the flow execution. If the time taken to retrieve data from SuccessFactors exceeds the timeout duration, the flow or subflow is cancelled. Default value is, `30`.|

    ![SOAP connection record.](../image/sapsf-soap-conn.png)

6.  Click **Submit**.


### Result

The connection record for the SOAP API in SuccessFactors is created.

## Synchronize data between SuccessFactors and ServiceNow

Customise the sample flows as per your requirement to synchronize data between your SuccessFactors and ServiceNow instances.

### Todo entity

The SuccessFactors spoke provides sample flows to synchronize data bi-directionally for the todo entity. The sample flow, Run SuccessFactors Integration Flow can customised to retrieve data from SuccessFactors, while the Create Todo and Update Todo flows creates or updates the todo records in SuccessFactors when events occur in ServiceNow. While customising the sample flows, ensure that you provide appropriate triggers to retrieve and save future updates using transform maps.

### Other default entities

For these entities, the sample flow, Run SuccessFactors Integration Flow, can be customised to retrieve data from SuccessFactors:

-   Department
-   Location
-   Job Profile
-   Workers Profile
-   Effective Workers Profile
-   Job History Including Secondary Assignments

To create or update records in SuccessFactors for these entities when events occur in ServiceNow:

-   Create flows or subflows as per your choice or customise the sample flows and subflows.
-   Use Metadata Retrieval and Record Management actions in your flows.
-   Ensure that you provide appropriate triggers to retrieve and save future updates using transform maps.

### Other SuccessFactors entities

Depending on the SuccessFactors permissions and configurations, you can also synchronize data of other entities as per your requirement.

