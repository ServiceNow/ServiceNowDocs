---
title: Set up Visa Spoke
description: Integrate the ServiceNow instance and Visa Spoke using basic authentication to authenticate ServiceNow requests.Upload the client certificate to your ServiceNow instance to enable the creation of connections and credentials.Generate a certificate for the Visa Resolve Online \(VROL\) endpoint and upload it to your ServiceNow instance as a TrustCertificate. By uploading the trusted server certificate, you ensure that your instance is connecting to a valid and secure service.You can create a custom HTTPS protocol profile to specify the credentials and certificates used for outbound web services. For example, you can create a custom HTTPS protocol profile to enable mutual authentication.Create credentials to access a ServiceNow instance.Create a custom credential record for the Visa Spoke account. The Visa Spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Visa Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Visa Spoke

Integrate the ServiceNow instance and Visa Spoke using basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Visa Spoke.
-   Role required: admin.

## Upload client certificate to your instance

Upload the client certificate to your ServiceNow instance to enable the creation of connections and credentials.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System LDAP** &gt; **Certificates**.

2.  Click **New**.

3.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name to uniquely identify the record. For example, `Visa Client Certificate`.|
    |Type|Select **PKCS12 Key Store**.|
    |Notify on expiration|Define users to be notified when the certificate expires.|
    |Warn in days to expire|Enter the number of days to send a notification before the certificate expires.|
    |Active|Enable|
    |Expires in days|Enter the number of days until the certificate expires.|
    |Key store password|Enter a password associated with the certificate.|
    |Short description|Enter a summary about the certificate.|

4.  Click the attachments icon and attach a client certificate\(.p12\) file.

5.  Click **Validate Stores/Certificates** to check if the certificate is correct.

    If the instance encounters any errors with the certificate or keystore, it displays an error message.


## Upload a trusted server certificate

Generate a certificate for the Visa Resolve Online \(VROL\) endpoint and upload it to your ServiceNow instance as a TrustCertificate. By uploading the trusted server certificate, you ensure that your instance is connecting to a valid and secure service.

### Before you begin

Role required: admin

### About this task

The instance validates outbound Web Service calls by using the certificate provided by the service provider.

### Procedure

1.  Create a new Certificate record with the format **PEM** and type **Trust Store Cert**.

2.  Do one of the following actions:

    -   Attach the service provider's DER formatted certificate.
    -   Copy and paste the service provider's PEM format certificate into the **PEM Certificate** field.

## Create a protocol profile

You can create a custom HTTPS protocol profile to specify the credentials and certificates used for outbound web services. For example, you can create a custom HTTPS protocol profile to enable mutual authentication.

### Before you begin

-   Role required: admin
-   [Upload client certificate to your instance](set-up-visa-spoke.md#) to authenticate the client certificate of the instance.
-   [Upload a trusted server certificate](set-up-visa-spoke.md#) to authenticate the server certificate of the web service provider.

### Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Protocol Profiles**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_jxy_gsm_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Protocol

</td><td>

Enter a unique name to identify this HTTPS protocol, such as `visahttps`. The protocol name allows you to differentiate between normal HTTPS connections and HTTPS connections that use this protocol profile. The name you enter becomes the protocol name in the URL. For example, `visahttps://endpoint.service.com`**Note:** You cannot create a custom protocol whose name matches as an existing protocol name such as HTTPS.

</td></tr><tr><td>

Keystore

</td><td>

Select the Keystore certificate that you had created when uploading a client certificate. For example `Visa Client Certificate`

</td></tr><tr><td>

Default port

</td><td>

Enter the port number for connections that use this protocol.

</td></tr></tbody>
</table>
## Create basic auth server credentials

Create credentials to access a ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  Select **Basic Auth Credential**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique and descriptive name for this credential.|
    |User name|Name to identify the user.|
    |Password|Password to use this credential.|
    |Active|Option to enable the use of this credential.|
    |Order|The order \(sequence\) in which the platform tries this credential while it attempts to log in to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order. Default value: `100`|

5.  Select **Submit**.


## Create a Connection &amp; Credential alias for Visa

Create a custom credential record for the Visa Spoke account. The Visa Spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Connections**, click **New**, and select **HTTP\(s\) Connection**.

2.  Add the following connection information and click **Submit**:

<table id="table_cpw_z5c_zpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of this HTTP\(s\) connection.

</td></tr><tr><td>

Credential

</td><td>

Select the credential record used to authorize the connection.

</td></tr><tr><td>

Connection Alias

</td><td>

Select the alias record to associate with this connection. Using an alias enables you to update the connection record without having to reconfigure any actions or activities that use the alias.

</td></tr><tr><td>

URL builder

</td><td>

Either manually enter the connection URL or use system to build the URL based on the inputs. Default is unchecked. If checked, the connection URL is calculated from the following fields: -   Mutual authentication — Check box if mutual authentication is used.
-   Protocol profile — Select the protocol created. For example, `visahttps`.
-   Host - Enter the Visa Endpoint. For example, `xxx.visa.com`
-   Base path — Path of the connection string.
 **Note:** If mutual authentication is checked, connection URL is built: Protocol + :// + host:port +URL. If mutual authentication is unchecked, connection URL is built: Protocol profile + :// + host:port +URL

</td></tr><tr><td>

Connection URL

</td><td>

If URL builder is unchecked, enter the connection URL into this field.**Note:** If mutual authentication is checked, connection URL is built: Protocol + :// + host:port +URL. If mutual authentication is unchecked, connection URL is built: Protocol profile + :// + host:port +URL

</td></tr><tr><td>

Active

</td><td>

Check the box to make this connection active.

</td></tr><tr><td>

Domain

</td><td>

Determine the domain the action or activity runs in.

</td></tr></tbody>
</table>3.  Click **Submit**.

    You are ready to create a custom HTTP\(s\) action or activity.


