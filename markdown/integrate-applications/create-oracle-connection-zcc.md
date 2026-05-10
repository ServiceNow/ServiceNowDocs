---
title: Create an Oracle connection
description: Establish a zero copy connection to an external Oracle database in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Oracle, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create an Oracle connection

Establish a zero copy connection to an external Oracle database in Zero Copy Connector Hub.

## Before you begin

You can optimize queries to Oracle by enabling table statistics. Consult your data source admin to confirm whether table statistics are enabled in Oracle before enabling this option in Zero Copy Connector Hub.

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Oracle. For additional information about connecting to Oracle, refer to the [Oracle documentation](https://docs.oracle.com/en/cloud/paas/autonomous-database/serverless/adbsb/connect-jdbc-thin-wallet.html#GUID-BE543CFD-6FB4-4C5B-A2EA-9638EC30900D).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Oracle connector and select **Connect**.

3.  On the form, fill in the fields.

<table id="table_kmx_fw1_2fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Name and description

</td></tr><tr><td>

Connection label

</td><td>

Unique name for this connection. This helps in identifying the connection within your system.

</td></tr><tr><td>

Connection name

</td><td>

System-generated name based on the Connection label. This field cannot be modified once the connection is established.

</td></tr><tr><td>

Short description

</td><td>

Description of the connection explaining what it is about.

</td></tr><tr><td class="sub-head" colspan="2">

Connection attributes

</td></tr><tr><td>

Connection URL

</td><td>

JDBC URL from the tnsnames.ora file in the wallet to establish the connection. For example: `jdbc:oracle:thin:@(description=(address=(protocol=tcps)(port=<port>)(host=<host>))(connect_data=(service_name=<service-name>)))`

</td></tr><tr><td>

Enable table statistics

</td><td>

Option to enable table statistics. Optimize SQL queries using table statistics by selecting this option. Enabling table statistics allows the system to use estimates of stored data such as row count, distinct values, and data size for enhanced query processing.

**Note:** You must ensure that gathering table statistics is enabled in the data source before selecting this option.

</td></tr></tbody>
</table>4.  Configure the authentication method that you want to use with Oracle.

<table id="choicetable_hsy_pmb_2fc"><thead><tr><th align="left" id="d666848e236">

Option

</th><th align="left" id="d666848e239">

Description

</th></tr></thead><tbody><tr><td id="d666848e245">

**Username / Password**

</td><td>

Option to use basic authentication.

 1.  Enter the database username associated with the source.
2.  Enter the database password associated with the username.


</td></tr><tr><td id="d666848e266">

**OAuth**

</td><td>

Option to use OAuth authentication.

 OAuth authentication requires an OAuth entity profile configured in the Application Registries \[oauth\_entity\] table with your Oracle or IdP credentials. Oracle supports only the Access Token credential type.

 This option keeps credentials within the instance and uses the ServiceNow AI Platform OAuth framework for token lifecycle management. For details on creating an OAuth entity profile, see [Use a third-party OAuth provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_UseAThirdPartyOAuthProvider.md). When configuring the profile, select **Client Credentials** as the grant type. If your OAuth provider requires scopes, add them on the OAuth Entity Scopes tab. Consult your data source or identity provider documentation for the required scope values.

 Select the OAuth entity profile for your Oracle or IdP service principal.

</td></tr></tbody>
</table>5.  Configure connection security.

<table id="choicetable_ejt_ldh_b3c"><thead><tr><th align="left" id="d666848e306">

Option

</th><th align="left" id="d666848e309">

Description

</th></tr></thead><tbody><tr><td id="d666848e315">

**Default**

</td><td>

Select this option to use Java security CA certificates to establish a secure connection with the data source.This option uses public certificates that are already available in the Java security truststore.

</td></tr><tr><td id="d666848e326">

**mTLS**

</td><td>

Select this option if your data source requires two-way SSL and uses its own certificates.

</td></tr></tbody>
</table>6.  If you selected mTLS, select a keystore type and configure the required certificates.

<table id="choicetable_zzc_z2h_b3c"><thead><tr><th align="left" id="d666848e345">

Option

</th><th align="left" id="d666848e348">

Description

</th></tr></thead><tbody><tr><td id="d666848e354">

**Keystore - PEM \(secure\)**

</td><td>

1.  Attach the wallet PEM file from the wallet folder using one of the following options:
    -   Upload the wallet PEM file by selecting **Attach PEM file** and selecting the file.
    -   Copy and paste the contents of the PEM file, ensuring the content contains one private key beginning with:

        ```
-----BEGIN ENCRYPTED PRIVATE KEY-----
        ```

and ending with:

        ```
-----END ENCRYPTED PRIVATE KEY-----
        ```

and two certificates, each beginning with:

        ```
-----BEGIN CERTIFICATE-----
        ```

and ending with:

        ```
-----END CERTIFICATE-----
        ```

2.  Enter the PEM file password associated with the wallet.


</td></tr><tr><td id="d666848e394">

**Keystore - JKS \(secure\)**

</td><td>

1.  Attach the Base64-encoded truststore.crt file from the wallet folder using one of the following options:
    -   Upload the truststore file by selecting **Attach TrustStore file** and selecting the file.
    -   Copy and paste the contents of the truststore file, ensuring the content begins with:

        ```
-----BEGIN CERTIFICATE-----
        ```

and ends with:

        ```
-----END CERTIFICATE-----
        ```

2.  Attach the Base64-encoded keystore.crt file from the wallet folder using one of the following options:
    -   Upload the keystore file by selecting **Attach KeyStore file** and selecting the file.
    -   Copy and paste the contents of the keystore file.
3.  Enter the truststore password associated with the wallet.
4.  Enter the keystore password associated with the wallet.


</td></tr></tbody>
</table>7.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

