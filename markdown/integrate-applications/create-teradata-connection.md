---
title: Create a Teradata connection
description: Establish a zero copy connection to a Teradata system in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Teradata, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Teradata connection

Establish a zero copy connection to a Teradata system in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Teradata. For additional information about connecting to Teradata, refer to the [Teradata documentation](https://github.com/Teradata/trino/blob/teradata-connector/docs/src/main/sphinx/connector/teradata.md) and [Teradata JDBC Driver](https://teradata-docs.s3.amazonaws.com/doc/connectivity/jdbc/reference/current/jdbcug_chapter_2.html).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Teradata connector and select **Connect**.

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

JDBC URL to establish the connection. For example:`jdbc:teradata://<host>:<port>;database=<databaseName>`

</td></tr><tr><td class="sub-head" colspan="2">

Authentication methods

</td></tr><tr><td>

Authentication method

</td><td>

Authentication method to use with Teradata. The available options are:

-   Basic Authentication \(the default\)
-   Bearer Token
-   OAuth


</td></tr><tr><td class="sub-head" colspan="2">

Basic Authentication

</td></tr><tr><td>

Database username

</td><td>

User name associated with the database.

</td></tr><tr><td>

Database password

</td><td>

Password associated with the user name.

</td></tr><tr><td class="sub-head" colspan="2">

Bearer Token

</td></tr><tr><td>

Private Key

</td><td>

Private key used to sign the JWT bearer token for client authentication.

</td></tr><tr><td>

JWS Certificate

</td><td>

X.509 certificate PEM file containing the public key corresponding to the private key. Required by identity providers that need an x5t header thumbprint for JWT signature verification.

</td></tr><tr><td>

Client Id

</td><td>

Client identifier registered with the identity provider.

</td></tr><tr><td class="sub-head" colspan="2">

OAuth

</td></tr><tr><td colspan="2">

**Note:** The OAuth authentication method supports two credential types, each corresponding to a login mechanism configured on the Teradata side. Confirm the configured mechanism before selecting an option.

</td></tr><tr><td>

OAuth credential type

</td><td>

OAuth credential type to use with Teradata. -   Teradata Service Principal: Used for a secret-based login mechanism.
-   Access Token: Used for a JWT-based login mechanism.


</td></tr><tr><td colspan="2">

Teradata Service Principal fields

</td></tr><tr><td>

Client Id

</td><td>

Client identifier registered with the identity provider.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret associated with the service principal.

</td></tr><tr><td colspan="2">

Access Token field

</td></tr><tr><td>

OAuth entity profile

</td><td>

OAuth entity profile associated with the application registry \(oauth\_entity table\) created using the data source or IdP credentials. Token management is handled by the platform's OAuth framework.

</td></tr></tbody>
</table>4.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

