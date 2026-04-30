---
title: Configure the Oracle HCM Cloud spoke connection record
description: Set up an outbound integration between the ServiceNow instance and the Oracle HCM instances by creating connection and credential records.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up the Oracle HCM Cloud spoke, Oracle HCM Cloud Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure the Oracle HCM Cloud spoke connection record

Set up an outbound integration between the ServiceNow instance and the Oracle HCM instances by creating connection and credential records.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Oracle HCM Cloud spoke plugin on the ServiceNow instance.
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Set the connection and credential for the Oracle Cloud HCM instance.

    1.  Select Connections.

    2.  Turn on the Outbound tab.

    3.  In the Search all connections field, enter `Oracle HCM`.

    4.  On the OracleCloudHCM tile, select **View Details**.

    5.  Select **Configure**.

    6.  Fill the form.

<table id="table_unm_twb_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection.**Note:** For the first connection, the default name is OracleCloudHCM that is read-only. However, for all the connection records you set up after the first record, you can provide a custom name.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to the Oracle HCM tenant.

</td></tr><tr><td>

Version

</td><td>

Version of the Oracle API.

</td></tr><tr><td>

JWT Provider Name

</td><td>

Name of the JWT provider.

</td></tr><tr><td>

JWT Keys Name

</td><td>

Name of the JWT key.

</td></tr><tr><td>

Signing Keystore

</td><td>

Name of the key store that you had created. To learn how to create a key store, see [Upload Java KeyStore certificate to ServiceNow instance](upload-java-keystore-certificate-to-servicenow-instance.md).

</td></tr><tr><td>

Signing Key Password

</td><td>

Password that you had created while creating the Java KeyStore file.

</td></tr><tr><td>

Issuer \(iss\) Claim value

</td><td>

The value that you had configured while creating a trusted issuer. For more information, see [Create a trusted issuer](upload-public-certificate-to-oracle-hcm-tenant.md).

</td></tr><tr><td>

Subject \(sub\) Claim value

</td><td>

User name that has access to the REST API endpoint.

</td></tr><tr><td>

Fingerprint/x5t value

</td><td>

Base 64 value that you had obtained while generating the fingerprint.

</td></tr></tbody>
</table>    7.  Select **Configure Connection**.

    **Note:** To update the default expiry time of a token, do the steps.

    1.  In the filter field of your instance, enter `sys_properties.LIST` and press **Enter**.
    2.  In the Name field of the System Properties page, enter `jwt.provider.expiry.interval.limit and` and press **Enter**.
    3.  On the jwt.provider.expiry.interval.limit page, update the value in the Value field.
    4.  Navigate to **All** &gt; **JWT Providers**.
    5.  Set the same expiry value in seconds in the field Expiry Interval \(sec\).
3.  Set the connection and credential for the Oracle Cloud HCM Reports instance.

    1.  On the OracleCloudHCMReports tile, select **View Details**.

    2.  Select **Configure**.![Configure button for Oracle HCM Cloud Report connection record.](../image/oracle-hcm-reports-click-configure.png)

    3.  In the form, fill the details.

<table id="table_bpm_2yb_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection.**Note:** For the first connection, the default name is OracleCloudHCMReports that is read-only. However, for all the connection records you set up after the first record, you can provide a custom name.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to the Oracle HCM Cloud Reports instance. The format is `https://<provider-domain-name>.com`

</td></tr><tr><td>

User name

</td><td>

User name to log in to your target host on which Oracle Cloud HCM Reports is installed.

</td></tr><tr><td>

Password

</td><td>

Password to authenticate and log in to your target host on which Oracle Cloud HCM Reports is installed.

</td></tr></tbody>
</table>    4.  Select **Configure Connection**.


