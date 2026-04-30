---
title: Set up Mastercard spoke
description: Integrate the ServiceNow instance with the Mastercard account using the OAuth protocol \(version 1.0a\) for secure authorization to authenticate ServiceNow requests.Use the certificate generated during the Mastercard account configuration to sign the request and payloads.Create a connection record for your Mastercard account configuration. The Mastercard spoke connection and credential aliases use these connections to perform actions in Mastercard.Create a credential record for your Mastercard account configuration. The Mastercard spoke connection and the credential alias uses these credentials to authorize actions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mastercard spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up Mastercard spoke

Integrate the ServiceNow instance with the Mastercard account using the OAuth protocol \(version 1.0a\) for secure authorization to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Mastercard spoke.
-   Role required: admin

## Attach a Mastercard certificate

Use the certificate generated during the Mastercard account configuration to sign the request and payloads.

### Before you begin

-   Valid Mastercard certificate
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Select **New**.

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

4.  Select the manage attachments icon \(![Manage attachments icon.](../image/attachments-icon.png)\) and attach a Mastercard certificate.

5.  Select **Validate Stores/Certificates** to validate the certificate.

6.  Select **Submit**.


## Create a connection record for Mastercard spoke

Create a connection record for your Mastercard account configuration. The Mastercard spoke connection and credential aliases use these connections to perform actions in Mastercard.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open for the record for **Mastercard**.

3.  On the **Connections** tab, select **New**.

4.  On the form, fill these values.

    |Field|Value required|
    |-----|--------------|
    |Connection URL|Base URL to connect to your Mastercard instance. For example, `https://sandbox.api.mastercard.com`.|
    |Credential|Credential record you that created for Mastercard.|

5.  Right-click the form header and select **Save**.

6.  Ensure that **api\_version** is set `V6` in the Attributes related list.


## Create a credential record for Mastercard spoke

Create a credential record for your Mastercard account configuration. The Mastercard spoke connection and the credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **Mastercard Credential**.

    A Mastercard Credential form displays.

4.  Enter these values.

<table id="table_fvk_jds_xyb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record. For example, `Mastercard Credentials`.

</td></tr><tr><td>

Active

</td><td>

Enable

</td></tr><tr><td>

Key alias

</td><td>

Key alias associated with the Mastercard account.

</td></tr><tr><td>

Keystore password

</td><td>

The password associated with the certificate.

</td></tr><tr><td>

Consumer key

</td><td>

Consumer key that you generated during the Mastercard configuration.

</td></tr><tr><td>

Certificate

</td><td>

Select the newly created Mastercard certificate.

</td></tr><tr><td>

Authentication Algorithm

</td><td>

Custom authentication algorithm for outbound signing requests. Select **Mastercard**.**Note:** You are cautioned against directly modifying the default authentication algorithm.

</td></tr></tbody>
</table>5.  Select **Submit**.


