---
title: Create a PostgreSQL connection
description: Create a zero-copy connection to PostgreSQL to access relational database data in Zero Copy Connector Hub without moving or duplicating data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-postgresql-connection-zcc.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [PostgreSQL connection, zero-copy connector, JDBC connector, data fabric connection, relational database]
breadcrumb: [PostgreSQL, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a PostgreSQL connection

Create a zero-copy connection to PostgreSQL to access relational database data in Zero Copy Connector Hub without moving or duplicating data.

## Before you begin

Role required: df\_connection\_admin

## About this task

Table statistics are enabled by default for PostgreSQL connections.

After you create this connection, data stewards can use it to create data fabric tables that map to PostgreSQL data sources. For additional information about connecting, see [PostgreSQL connector documentation](https://trino.io/docs/current/connector/postgresql.html).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Locate the PostgreSQL connector and select **Connect**.

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

JDBC URL to establish the connection. For example: `jdbc:postgresql://<host>:<port>/<database>?sslmode=require`

The `sslmode` parameter in the URL is optional. Setting SSL mode in the Connection security configurations section is the recommended approach; if you specify `sslmode` in the URL, it takes precedence over that setting.

</td></tr><tr><td>

SSL

</td><td>

Option to enable or disable SSL for the connection. When **Enabled**, additional fields appear based on the selected SSL mode, Server Certificate Source, and Store type. See [PostgreSQL connection security configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-connection-security-fields-zcc.md) for the complete conditional field set.

</td></tr></tbody>
</table>4.  Configure the authentication method that you want to use with PostgreSQL.

<table id="choicetable_pg_auth"><thead><tr><th align="left" id="d219272e264">

Option

</th><th align="left" id="d219272e267">

Description

</th></tr></thead><tbody><tr><td id="d219272e273">

**Basic**

</td><td>

Option to use a username and password.

 1.  Enter the username associated with the source.
2.  Enter the password associated with the username.


</td></tr><tr><td id="d219272e294">

**AWS IAM**

</td><td>

Option to authenticate using AWS RDS IAM \(temporary STS token-based\) authentication. See [PostgreSQL authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-authentication-method-fields-zcc.md) for the specific fields \(Database user, AWS region, AWS access key ID, AWS secret access key\).

</td></tr><tr><td id="d219272e313">

**GCP IAM**

</td><td>

Option to authenticate using GCP Cloud IAM token-based authentication, with either a service account or user credentials. See [PostgreSQL authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-authentication-method-fields-zcc.md) for the specific fields \(Service account key \(JSON\), Database user, GCP token scope\).

</td></tr><tr><td id="d219272e332">

**OAuth**

</td><td>

Option to authenticate using Azure AD / Entra ID OAuth 2.0 \(Resource Owner Password Credentials flow\). See [PostgreSQL authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-authentication-method-fields-zcc.md) for the specific fields \(OAuth credential type, Database user, Azure tenant ID, Azure client ID, Azure client secret, Azure token scope\).

</td></tr></tbody>
</table>5.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

**Related topics**  


[PostgreSQL connection security configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-connection-security-fields-zcc.md)

[PostgreSQL authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-authentication-method-fields-zcc.md)

