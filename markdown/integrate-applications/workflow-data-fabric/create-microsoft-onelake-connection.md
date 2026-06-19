---
title: Create a Microsoft OneLake connection
description: Establish a zero copy connection to a Microsoft OneLake system in Zero Copy Connector Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/create-microsoft-onelake-connection.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft OneLake, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Microsoft OneLake connection

Establish a zero copy connection to a Microsoft OneLake system in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Microsoft OneLake. For additional information about connecting to Microsoft OneLake, refer to the Microsoft OneLake documentation.

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Microsoft OneLake connector and select **Connect**.

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

Catalog Configuration

</td></tr><tr><td>

Iceberg REST catalog URI

</td><td>

URI of the Iceberg REST catalog endpoint for Microsoft OneLake. For example: ```
https://onelake.dfs.fabric.microsoft.com/iceberg
```

</td></tr><tr><td>

OAuth client ID

</td><td>

Client ID for authenticating with the Iceberg REST catalog.

</td></tr><tr><td>

OAuth secret

</td><td>

Secret key associated with the client ID.

</td></tr><tr><td>

OAuth Endpoint

</td><td>

Endpoint for the Iceberg REST catalog OAuth2 server URI. For example:```
https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token
```

</td></tr><tr><td>

WareHouse

</td><td>

Iceberg REST catalog warehouse.

</td></tr><tr><td class="sub-head" colspan="2">

Object Storage System configuration

</td></tr><tr><td>

Azure tenant ID

</td><td>

Tenant ID issued by Microsoft OneLake for authentication.

</td></tr><tr><td>

OAuth client ID

</td><td>

Azure issued client ID for authenticating with Microsoft OneLake.

</td></tr><tr><td>

OAuth secret

</td><td>

Secret key associated with the client ID.

</td></tr><tr><td>

OAuth Endpoint

</td><td>

Azure OAuth endpoint for connection. For example:```
https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token
```

</td></tr></tbody>
</table>4.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See .

If the connection fails, verify the connection details with your data source administrator and try again.

