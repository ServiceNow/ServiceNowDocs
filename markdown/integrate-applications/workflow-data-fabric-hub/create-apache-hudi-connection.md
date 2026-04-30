---
title: Create an Apache Hudi connection
description: Establish a zero copy connection to Apache Hudi in Workflow Data Fabric Hub.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Apache Hudi, Community connectors, Manage zero copy connections, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Create an Apache Hudi connection

Establish a zero copy connection to Apache Hudi in Workflow Data Fabric Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Apache Hudi. For additional information about connecting, refer to the [Hudi connector documentation](https://trino.io/docs/current/connector/hudi.html).

**Note:** This connector was developed by the open-source community and made available through the ServiceNow AI Platform for general use. Functionality can vary and might not cover all use cases supported by primary connectors.

## Procedure

1.  Navigate to the available community connectors in Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Community connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Community connectors**.
2.  Find the Apache Hudi connector and select **Connect**.

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

Object storage authentication

</td></tr><tr><td>

Connection URI

</td><td>

URI to establish the connection. For example:`thrift://<host>:<port>`

</td></tr><tr><td>

Object storage system

</td><td>

Storage system used. Default is Amazon S3.

</td></tr><tr><td>

AWS access key

</td><td>

Access key used to access S3.

</td></tr><tr><td>

AWS secret key

</td><td>

Secret key used to access S3.

</td></tr><tr><td>

AWS region

</td><td>

AWS region where your S3 bucket is located.

</td></tr></tbody>
</table>4.  Configure the metastore that you want to use with Apache Hudi.

<table id="choicetable_xqf_z3l_rfc"><thead><tr><th align="left" id="d360853e256">

Option

</th><th align="left" id="d360853e259">

Description

</th></tr></thead><tbody><tr><td id="d360853e265">

**Hive Thrift**

</td><td>

1.  Attach the truststore file using one of the following options:
    -   Upload the truststore file by selecting **Attach TrustStore certificate** and selecting the file.
    -   Copy and paste the contents of the truststore file.
2.  Enter the metastore URI that you want to connect to using the Thrift protocol. For example:

`thrift://<host>:<port>`

3.  Enter the truststore password.


</td></tr><tr><td id="d360853e300">

**AWS Glue**

</td><td>

1.  Enter the AWS access key to connect to the Glue Catalog.
2.  Enter the AWS secret key to use to connect to the Glue Catalog.
3.  Enter the AWS region of the Glue Catalog.


</td></tr></tbody>
</table>5.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-wdf.md).

If the connection fails, verify the connection details with your data source administrator and try again.

