---
title: Create a Microsoft SQL Server connection
description: Create a zero-copy connection to Microsoft SQL Server to access relational database data in Zero Copy Connector Hub without moving or duplicating data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/create-sqlserver-connection-zcc.html
release: australia
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 3
keywords: [Microsoft SQL Server connection, zero-copy connector, JDBC connector, data fabric connection, relational database]
breadcrumb: [Microsoft SQL Server, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Microsoft SQL Server connection

Create a zero-copy connection to Microsoft SQL Server to access relational database data in Zero Copy Connector Hub without moving or duplicating data.

## Before you begin

Role required: df\_connection\_admin

## About this task

Table statistics are enabled by default for Microsoft SQL Server connections.

After you create this connection, data stewards can use it to create data fabric tables that map to Microsoft SQL Server data sources. For additional information about connecting, see [Microsoft SQL Server connector documentation](https://trino.io/docs/current/connector/sqlserver.html).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Locate the Microsoft SQL Server connector and select **Connect**.

3.  Complete the connection form.

<table id="table_sqlserver_conn_form"><thead><tr><th>

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

JDBC URL to establish the connection. The `encrypt` and `trustServerCertificate` parameters in the URL are optional; setting SSL in the Connection security configurations section is the recommended approach. If you specify these parameters in the URL, they take precedence over that setting. Azure SQL example:

 `jdbc:sqlserver://<server>.database.windows.net:1433;database=<db>;encrypt=true;trustServerCertificate=false;hostNameInCertificate=*.database.windows.net;loginTimeout=30`

 GCP / on-premises example:

 jdbc:sqlserver://&lt;host&gt;:1433;databaseName=&lt;db&gt;;encrypt=true;trustServerCertificate=true

</td></tr><tr><td>

SSL

</td><td>

Option to enable or disable SSL for the connection. When **Enabled**, additional fields appear based on the selected SSL mode, Server Certificate Source, and Store type. See [Microsoft SQL Server connection security configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/sqlserver-connection-security-fields-zcc.md) for the complete conditional field set.

</td></tr></tbody>
</table>4.  Configure the authentication method that you want to use with Microsoft SQL Server.

<table id="choicetable_sqlserver_auth"><thead><tr><th align="left" id="d143645e265">

Option

</th><th align="left" id="d143645e268">

Description

</th></tr></thead><tbody><tr><td id="d143645e274">

**Basic**

</td><td>

Option to use a Microsoft SQL Server login username and password. Compatible with all Microsoft SQL Server deployments, including Azure SQL, GCP Cloud SQL, AWS RDS, and on-premises.

 1.  Enter the username associated with the source.
2.  Enter the password associated with the username.


</td></tr><tr><td id="d143645e295">

**OAuth**

</td><td>

Option to authenticate using OAuth.

 **Note:** Azure SQL Server supports OAuth for this connector. AWS RDS and GCP Cloud SQL don't support IAM or token-based authentication for Microsoft SQL Server at the platform level, so use Basic authentication for those deployments. This is a cloud-provider limitation, not a limitation of the connector.

 Select the OAuth credential type that you want to use.

 -   **Azure Service Principal**: option to enter OAuth credentials directly from Azure AD \(Entra ID\). See [Microsoft SQL Server authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/sqlserver-authentication-method-fields-zcc.md) for the specific fields \(Azure tenant ID, Azure client ID, Azure client secret, Azure token scope\).
-   **Access Token**: option to use an existing OAuth entity profile, with either a shared \(System\) or per-user \(Personal\) integration type. See [Microsoft SQL Server authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/sqlserver-authentication-method-fields-zcc.md) for the specific fields \(OAuth entity profile, Select OAuth integration type\).


</td></tr></tbody>
</table>5.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

**Related topics**  


[Microsoft SQL Server connection security configuration fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/sqlserver-connection-security-fields-zcc.md)

[Microsoft SQL Server authentication method fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/sqlserver-authentication-method-fields-zcc.md)

