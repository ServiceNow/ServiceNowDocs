---
title: Create a Snowflake connection
description: Establish a zero copy connection to an external Snowflake account in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Snowflake, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Snowflake connection

Establish a zero copy connection to an external Snowflake account in Zero Copy Connector Hub.

## Before you begin

You can optimize queries to Snowflake by enabling table statistics. Consult your data source admin to confirm whether table statistics are enabled in Snowflake before enabling this option in Zero Copy Connector Hub.

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Snowflake. For additional information about connecting to Snowflake, refer to the [Snowflake documentation](https://docs.snowflake.com/en/user-guide/key-pair-auth).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Snowflake connector and select **Connect**.

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

JDBC URL to establish the connection. For example: `jdbc:snowflake://<account>.snowflakecomputing.com`

</td></tr><tr><td>

Database

</td><td>

Name of the database that you want to connect to.

</td></tr><tr><td>

Warehouse

</td><td>

Name of the warehouse that you want to connect to.

</td></tr><tr><td>

Enable table statistics

</td><td>

Option to enable table statistics. Optimize SQL queries using table statistics by selecting this option. Enabling table statistics allows the system to use estimates of stored data such as row count, distinct values, and data size for enhanced query processing.

**Note:** You must ensure that gathering table statistics is enabled in the data source before selecting this option.

</td></tr></tbody>
</table>4.  Configure the authentication method that you want to use with Snowflake.

<table id="choicetable_ckm_bgh_b3c"><thead><tr><th align="left" id="d146111e254">

Option

</th><th align="left" id="d146111e257">

Description

</th></tr></thead><tbody><tr><td id="d146111e263">

**JWT**

</td><td>

Option to use key pair authentication.

 1.  Attach the private key using one of the following options:
    -   Upload the private key file by selecting **Attach PEM file** and selecting the file.
    -   Copy and paste the contents of the PEM file, ensuring the content begins with:

        ```
-----BEGIN PRIVATE KEY-----
        ```

and ends with:

        ```
-----END PRIVATE KEY-----
        ```

2.  Enter the connection user to connect to Snowflake.
3.  Enter the passphrase if the private key is secured with a password.
4.  Enter the role that determines your permissions within Snowflake.


</td></tr><tr><td id="d146111e306">

**OAuth**

</td><td>

Option to use OAuth authentication.

 Select the OAuth credential type that you want to use.

 -   **Client credentials**

Select this option to enter OAuth credentials directly from your identity provider.

    1.  Enter the client ID from your OAuth identity provider.
    2.  Enter the client secret from your OAuth identity provider.
    3.  Enter the token request URL from your OAuth identity provider.
    4.  Enter the scope from your OAuth identity provider.
-   **Access Token**

Select this option if you created a record in the Application Registries \[oauth\_entity\] table with a Snowflake or IdP service principal for authentication.

This option keeps credentials within the instance and uses the ServiceNow AI Platform OAuth framework for token lifecycle management. For details on creating an OAuth entity profile, see [Use a third-party OAuth provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_UseAThirdPartyOAuthProvider.md). When configuring the profile, select **Client Credentials** as the grant type. If your OAuth provider requires scopes, add them on the OAuth Entity Scopes tab. Consult your data source or identity provider documentation for the required scope values.

Select the OAuth entity profile for your Snowflake or IdP service principal.

</td></tr></tbody>
</table>5.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

