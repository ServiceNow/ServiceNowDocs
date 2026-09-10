---
title: Create a MySQL connection
description: Create a zero-copy connection to MySQL to access relational database data in Zero Copy Connector Hub without moving or duplicating data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-mysql-connection-zcc.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [MySQL connection, zero-copy connector, JDBC connector, data fabric connection, relational database]
breadcrumb: [MySQL, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a MySQL connection

Create a zero-copy connection to MySQL to access relational database data in Zero Copy Connector Hub without moving or duplicating data.

## Before you begin

Role required: df\_connection\_admin

## About this task

Table statistics are enabled by default for MySQL connections.

After you create this connection, data stewards can use it to create data fabric tables that map to MySQL data sources. For additional information about connecting, see the [MySQL connector documentation](https://trino.io/docs/current/connector/mysql.html).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Locate the MySQL connector and select **Connect**.

3.  Complete the connection form.

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

JDBC URL to establish the connection. For example: `jdbc:mysql://<host>:<port>?sslMode=REQUIRED`

The `sslMode` parameter in the URL is optional. Setting SSL mode in the Connection security configurations section is the recommended approach. If you specify `sslMode` in the URL, it takes precedence over that setting.

</td></tr><tr><td>

SSL

</td><td>

Option to enable or disable SSL for the connection. When enabled, additional fields appear based on the selected SSL mode, Server Certificate Source, and Store type. See [MySQL connection security configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-connection-security-fields-zcc.md) for the complete conditional field set.

</td></tr></tbody>
</table>4.  Configure the authentication method that you want to use with MySQL.

<table id="choicetable_mysql_auth"><thead><tr><th align="left" id="d630051e251">

Option

</th><th align="left" id="d630051e254">

Description

</th></tr></thead><tbody><tr><td id="d630051e260">

**Basic**

</td><td>

Option to use a username and password.

 1.  Enter the username associated with the source.
2.  Enter the password associated with the username.


</td></tr><tr><td id="d630051e281">

**AWS IAM**

</td><td>

Option to authenticate using AWS IAM token-based authentication. See [MySQL authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-authentication-method-fields-zcc.md) for the specific fields \(Database user, AWS region, AWS access key ID, AWS secret access key\).

</td></tr><tr><td id="d630051e300">

**GCP IAM**

</td><td>

Option to authenticate using GCP Cloud IAM token-based authentication. See [MySQL authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-authentication-method-fields-zcc.md) for the specific fields \(Service account key \(JSON\), Database user, GCP token scope\).

</td></tr><tr><td id="d630051e319">

**OAuth**

</td><td>

Option to authenticate using Azure AD/Entra ID OAuth 2.0. See [MySQL authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-authentication-method-fields-zcc.md) for the specific fields \(OAuth credential type, Azure tenant ID, Azure client ID, Azure client secret, and Azure token scope\).

</td></tr></tbody>
</table>5.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

**Related topics**  


[MySQL connection security configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-connection-security-fields-zcc.md)

[MySQL authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-authentication-method-fields-zcc.md)

