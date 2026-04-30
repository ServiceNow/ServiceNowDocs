---
title: Create a Microsoft OneLake connection
description: Establish a zero copy connection to a Microsoft OneLake system in Workflow Data Fabric Hub.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft OneLake, Primary connectors, Managing zero copy connections in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Create a Microsoft OneLake connection

Establish a zero copy connection to a Microsoft OneLake system in Workflow Data Fabric Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Microsoft OneLake. For additional information about connecting to Microsoft OneLake, refer to the Microsoft OneLake documentation.

## Procedure

1.  Navigate to the available primary connectors in Workflow Data Fabric Hub in one of the following ways:

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

Connection attributes

</td></tr><tr><td>

Connection URL

</td><td>

JDBC URL to establish the connection. For example:`jdbc:microsoftonelake://<host>:<port>;database=<databaseName>`

</td></tr><tr><td class="sub-head" colspan="2">

Authentication methods

</td></tr><tr><td>

Authentication method

</td><td>

Authentication method to use with Microsoft OneLake. Default is Basic Authentication.

</td></tr><tr><td>

Database username

</td><td>

Username associated with the database.

</td></tr><tr><td>

Database password

</td><td>

Password associated with the username.

</td></tr></tbody>
</table>4.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-wdf.md).

If the connection fails, verify the connection details with your data source administrator and try again.

