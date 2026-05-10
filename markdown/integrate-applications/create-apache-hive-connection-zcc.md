---
title: Create an Apache Hive connection
description: Establish a zero copy connection to an Apache Hive data warehouse in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Apache Hive, Community connectors, Zero Copy Connectors, Workflow Data Fabric]
---

# Create an Apache Hive connection

Establish a zero copy connection to an Apache Hive data warehouse in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Apache Hive. For additional information about connecting, refer to the [Hive connector documentation](https://trino.io/docs/current/connector/hive.html).

**Note:** This connector was developed by the open-source community and made available through the ServiceNow AI Platform for general use. Functionality can vary and might not cover all use cases supported by primary connectors.

## Procedure

1.  Navigate to the available community connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Community connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Community connectors**.
2.  Find the Apache Hive connector and select **Connect**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name and description|
    |Connection label|Unique name for this connection. This helps in identifying the connection within your system.|
    |Connection name|System-generated name based on the Connection label. This field cannot be modified once the connection is established.|
    |Short description|Description of the connection explaining what it is about.|
    |Object storage authentication|
    |Object storage system|Storage system used. Default is Amazon S3.|
    |AWS access key|Access key used to access S3.|
    |AWS secret key|Secret key used to access S3.|
    |AWS region|AWS region where your S3 bucket is located.|

4.  Configure the metastore that you want to use with Apache Hive.

<table id="choicetable_xqf_z3l_rfc"><thead><tr><th align="left" id="d575098e243">

Option

</th><th align="left" id="d575098e246">

Description

</th></tr></thead><tbody><tr><td id="d575098e252">

**Hive Thrift**

</td><td>

1.  Attach the truststore file using one of the following options:
    -   Upload the truststore file by selecting **Attach TrustStore file** and selecting the file.
    -   Copy and paste the contents of the truststore file.
2.  Enter the truststore password.
3.  Enter the metastore URI that you want to connect to using the Thrift protocol. For example:

`thrift://<host>:<port>`

</td></tr><tr><td id="d575098e287">

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

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-zcc.md).

If the connection fails, verify the connection details with your data source administrator and try again.

