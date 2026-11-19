---
title: Create a Snowflake connection
description: Establish a zero copy connection to an external Snowflake account in Zero Copy Connector Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-snowflake-connection-zcc.html
release: brazil
topic_type: task
last_updated: "2026-11-12"
reading_time_minutes: 3
breadcrumb: [Snowflake, Primary connectors, Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Snowflake connection

Establish a zero copy connection to an external Snowflake account in Zero Copy Connector Hub.

## Before you begin

You can optimize queries to Snowflake by enabling table statistics. Consult your data source admin to confirm whether table statistics are enabled in Snowflake before enabling this option in Zero Copy Connector Hub.

Role required: df\_connection\_admin

## About this task

This connector supports personal authentication. For more information, see [Personal authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/personal-auth-zcc.md).

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

<table id="choicetable_ckm_bgh_b3c"><thead><tr><th align="left" id="d142546e268">

Option

</th><th align="left" id="d142546e271">

Description

</th></tr></thead><tbody><tr><td id="d142546e277">

**JWT**

</td><td>

Option to use key pair authentication. See [Snowflake authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/snowflake-authentication-method-fields-zcc.md) for the specific fields \(private key, connection user, passphrase, role\).

</td></tr><tr><td id="d142546e296">

**OAuth**

</td><td>

Option to use OAuth authentication. Select the OAuth credential type that you want to use.

 -   **Client credentials**: option to enter OAuth credentials directly from your identity provider. See [Snowflake authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/snowflake-authentication-method-fields-zcc.md) for the specific fields \(client ID, client secret, token request URL, scope\).
-   **Access Token**: option to use a pre-configured OAuth entity profile, with either a shared \(**System**\) or per-user \(**Personal**\) integration type. See [Snowflake authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/snowflake-authentication-method-fields-zcc.md) for the specific fields \(OAuth entity profile, OAuth integration type\).


</td></tr></tbody>
</table>5.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

**Related topics**  


[Snowflake authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/snowflake-authentication-method-fields-zcc.md)

