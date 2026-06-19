---
title: Create a Cloudera Hive connection
description: Establish a zero copy connection to a Cloudera Hive system in Zero Copy Connector Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/create-cloudera-hive-connection.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloudera Hive, Primary connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Cloudera Hive connection

Establish a zero copy connection to a Cloudera Hive system in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Cloudera Hive. For additional information about connecting to Cloudera Hive, refer to the [Cloudera Hive documentation](https://docs.cloudera.com/cdw-runtime/1.5.4/integrating-hive-and-bi/topics/hive_locate_the_jdbc_driver.html).

## Procedure

1.  Navigate to the available primary connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Primary connectors**.
2.  Find the Cloudera Hive connector and select **Connect**.

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

Connection Attributes

</td></tr><tr><td>

Connection URL

</td><td>

JDBC URL to establish the connection. For example:`jdbc:cloudera://<host>:<port>;database=<databaseName>`

</td></tr><tr><td class="sub-head" colspan="2">

Authentication Types

</td></tr><tr><td>

Authentication type

</td><td>

Authentication method to use with Cloudera Hive. Default is Basic Authentication.

</td></tr><tr><td>

UserId

</td><td>

User ID associated with the source.

</td></tr><tr><td>

Password

</td><td>

Password associated with the user ID.

</td></tr></tbody>
</table>4.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See .

If the connection fails, verify the connection details with your data source administrator and try again.

