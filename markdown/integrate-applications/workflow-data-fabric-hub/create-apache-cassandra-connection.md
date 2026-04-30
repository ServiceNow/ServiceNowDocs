---
title: Create an Apache Cassandra connection
description: Establish a zero copy connection to an Apache Cassandra database in Workflow Data Fabric Hub.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Apache Cassandra, Community connectors, Manage zero copy connections, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Create an Apache Cassandra connection

Establish a zero copy connection to an Apache Cassandra database in Workflow Data Fabric Hub.

## Before you begin

You can optimize queries to Apache Cassandra by enabling table statistics. Consult your data source admin to confirm whether table statistics are enabled in Apache Cassandra before enabling this option in Workflow Data Fabric Hub.

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Apache Cassandra. For additional information about connecting, refer to the [Cassandra connector documentation](https://trino.io/docs/current/connector/cassandra.html).

**Note:** This connector was developed by the open-source community and made available through the ServiceNow AI Platform for general use. Functionality can vary and might not cover all use cases supported by primary connectors.

## Procedure

1.  Navigate to the available community connectors in Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Community connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Community connectors**.
2.  Find the Apache Cassandra data source and select **Connect**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name and description|
    |Connection label|Unique name for this connection. This helps in identifying the connection within your system.|
    |Connection name|System-generated name based on the Connection label. This field cannot be modified once the connection is established.|
    |Short description|Description of the connection explaining what it is about.|
    |Connection attributes|
    |Connection URL|URL to establish the connection.|
    |Port|Port used in the connection.|
    |Datacenter|Datacenter that you want to connect to.|

4.  Configure secure authentication by uploading a keystore file or by entering the keystore details manually.

<table id="choicetable_rf1_cdk_qfc"><thead><tr><th align="left" id="d524929e240">

Option

</th><th align="left" id="d524929e243">

Description

</th></tr></thead><tbody><tr><td id="d524929e249">

**Upload keystore file**

</td><td>

1.  Select **Attach KeyStore file**.
2.  Browse and select the keystore file.


</td></tr><tr><td id="d524929e270">

**Enter keystore contents manually**

</td><td>

Copy and paste the contents of the keystore file.

</td></tr></tbody>
</table>5.  Enter the keystore password.

6.  Enter the data source username and password.

7.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-wdf.md).

If the connection fails, verify the connection details with your data source administrator and try again.

