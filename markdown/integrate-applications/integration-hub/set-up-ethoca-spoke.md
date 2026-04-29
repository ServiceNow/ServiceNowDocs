---
title: Set up Ethoca spoke
description: Integrate the ServiceNow instance with the Ethoca account using the using the OAuth protocol \(version 1.0a\) for the Consumer Clairty category and using Basic Auth credentials for the Issuers Alert Management category to authenticate ServiceNow requests.Integrate the ServiceNow instance with the Ethoca account in the Consumer Clarity category using the OAuth protocol \(version 1.0a\) to securely authorize and authenticate ServiceNow requests.Use the certificate generated during the Ethoca account configuration to sign the request and payloads.Create a credential record for your Ethoca account. The Ethoca spoke connection and credential alias uses these credentials to authorize actions.Create a connection record for your Ethoca account. The Ethoca spoke connection and credential aliases use these connections to perform actions in Ethoca.Integrate the ServiceNow instance with the Ethoca account in the Issuer Alerts Management category using Basic Auth credentials to authenticate ServiceNow requests.Create credentials to access a ServiceNow instance.Create a connection record for your Ethoca account. The Ethoca spoke connection and credential aliases use these connections to perform actions in Ethoca Alerts.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Ethoca spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Ethoca spoke

Integrate the ServiceNow instance with the Ethoca account using the using the OAuth protocol \(version 1.0a\) for the Consumer Clairty category and using Basic Auth credentials for the Issuers Alert Management category to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Ethoca spoke.
-   Role required: admin.

## For the Consumer Clarity category

Integrate the ServiceNow instance with the Ethoca account in the Consumer Clarity category using the OAuth protocol \(version 1.0a\) to securely authorize and authenticate ServiceNow requests.

Follow these steps:

-   [Attach a Ethoca certificate](set-up-ethoca-spoke.md#)
-   [Create credential records](set-up-ethoca-spoke.md#)
-   [Create connection records](set-up-ethoca-spoke.md#)

### Attach a Ethoca certificate

Use the certificate generated during the Ethoca account configuration to sign the request and payloads.

#### Before you begin

-   Valid Ethoca certificate
-   Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Click **New**.

3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name to identify the certificate.|
    |Type|Type of the certificate. Select `PKCS12 Key Store`.|
    |Notify on expiration|Select the list of users to be notified when the certificate expires.|
    |Warn in days to expire|Enter the number of days when a notification is sent to users before a certificate expires.|
    |Key store password|Password to access the certificate. Use the destination keystore password specified when creating the certificate.|
    |Active|Option to make the client certificate active.|
    |Short description|Short description of the user client certificate.|

4.  Click the manage attachments icon \(![Manage attachments icon.](../image/attachments-icon.png)\) and attach a Ethoca certificate.

5.  Click **Validate Stores/Certificates** to validate the certificate.

6.  Click **Submit**.


### Create credential records

Create a credential record for your Ethoca account. The Ethoca spoke connection and credential alias uses these credentials to authorize actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **Ethoca Credential**.

    A blank Ethoca Credential form displays.

4.  Enter these values.

<table id="table_fvk_jds_xyb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record. For example, `Ethoca Credentials`.

</td></tr><tr><td>

Active

</td><td>

Enable

</td></tr><tr><td>

Key alias

</td><td>

Key alias associated with the Ethoca account.

</td></tr><tr><td>

Keystore password

</td><td>

Password associated with the certificate.

</td></tr><tr><td>

Consumer key

</td><td>

Consumer key that you generated during the Ethoca configuration.

</td></tr><tr><td>

Certificate

</td><td>

Select the newly created Ethoca certificate.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **Ethoca**.**Note:** Users are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>5.  Click **Submit**.


### Create connection records

Create a connection record for your Ethoca account. The Ethoca spoke connection and credential aliases use these connections to perform actions in Ethoca.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open for the record for **Ethoca**.

3.  On the **Connections** tab, click **New**.

4.  On the form, fill these values.

    |Field|Value required|
    |-----|--------------|
    |Connection URL|Base URL to connect to your Ethoca instance. Enter: `https://sandbox.api.ethocaweb.com/ethoca`.|
    |Credential|Credential record that you created for Ethoca. For example, `Ethoca Credentials`.|

5.  Right-click the form header and click **Save**.


## For the Issuer Alerts Management category

Integrate the ServiceNow instance with the Ethoca account in the Issuer Alerts Management category using Basic Auth credentials to authenticate ServiceNow requests.

Follow these steps:

-   [Create basic auth credentials](set-up-ethoca-spoke.md#)
-   [Create connection records](set-up-ethoca-spoke.md#)

### Create basic auth credentials

Create credentials to access a ServiceNow instance.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select **Basic Auth Credentials**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the credential record. For example, `Ethoca Alerts Credentials`|
    |User name|Name to identify the user.|
    |Password|Password to use this credential.|
    |Active|Option to actively use the credential record. Select the option.|
    |Order|The order \(sequence\) in which the platform tries this credential while it attempts to log in to devices. Default value: `100`.|

5.  Select **Submit**.


### Create connection records

Create a connection record for your Ethoca account. The Ethoca spoke connection and credential aliases use these connections to perform actions in Ethoca Alerts.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open for the record for **Ethoca Alerts**.

3.  On the **Connections** tab, click **New**.

4.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection established with the Ethoca instance. The first connection's default name is automatically assigned to match the name specified in the Connections and Credentials form on the Connection &amp; Credential Aliases page.|
    |Credential|Credential record you that created for Ethoca Alerts. For example, `Ethoca Alerts Credentials`.|
    |Connection URL|Base URL to connect to your Ethoca instance. Enter: `https://sandbox.ethocaweb.com/ethoca-rest`.|

5.  Right-click the form header and click **Save**.


